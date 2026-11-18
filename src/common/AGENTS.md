# AGENTS.md — src/common and shared infrastructure

Guidance for AI coding agents working on TrinityCore's shared infrastructure. This covers `src/common/` plus the closely coupled database/networking layers in `src/server/database/`, `src/server/shared/`, `src/server/bnetserver/`, and `src/server/proto/`. Build commands are in the root [`AGENTS.md`](../../AGENTS.md).

## Module map (`src/common/`)

| Module | Responsibility |
|---|---|
| `Asio/` | Thin, forward-declarable wrappers over Boost.Asio: `IoContext`, `Strand`, `DeadlineTimer`, completion handlers, `AsioHacksFwd`. |
| `Collision/` | Bounding interval hierarchy, `DynamicTree`, `RegularGrid`, VMap definitions for map/VMAP geometry. |
| `Configuration/` | `ConfigMgr` INI loader with env overrides; `BuiltInConfig` compile-time paths. |
| `Containers/` | `FlatSet` (sorted-vector set). |
| `Cryptography/` | AES, ARC4, Argon2, BigNumber, RSA, Ed25519, TOTP, hash/HMAC, SRP auth, `CryptoRandom`, session keys, `WorldPacketCrypt`. |
| `DataStores/` | DB2 client-file binary loader and metadata (`DB2FileLoader`, `DB2Meta`). |
| `Debugging/` | `WPAssert`/`ASSERT`/`ABORT`, abort handler, Windows crash reporter. |
| `Encoding/` | Base32/Base64. |
| `Logging/` | `Log` singleton, `Logger`, console/file appenders, async logging. |
| `Metric/` | InfluxDB line-protocol metrics, MPSC queue, Asio timers. |
| `mmaps_common/` | Recast/Detour navmesh management and generator (separate library). |
| `network/` | `Socket`, `NetworkThread`, `SocketMgr`, `AsyncAcceptor`, resolver, IP address, SSL stream, HTTP (Boost.Beast). |
| `Platform/` | Windows service support only. |
| `Threading/` | Boost thread pool wrapper, MPSC/locked/producer-consumer queues, process priority. |
| `Time/` | `Timer`/`IntervalTimer`/`PeriodicTimer`, timezone helpers. |
| `Utilities/` | `TaskScheduler`/`TaskContext`, `EventMap`/`EventProcessor`, `AsyncCallbackProcessor`, random, string formatting, `MessageBuffer`, `Util`, duration, optional, hash, `StartProcess`. |

`common` aggregates most of these; `Platform`, `mmaps_common`, and `network` are separate libraries. `database`, `shared`, `proto`, `game`, and `scripts` are separate targets.

## Configuration

- Access via `sConfigMgr` and `GetStringDefault` / `GetBoolDefault` / `GetIntDefault` / `GetInt64Default` / `GetFloatDefault`. Missing keys log a warning and fall back to the code default unless `quiet=true`.
- `.conf` files are INI parsed by Boost.PropertyTree. Only the first section is used; its children become the root.
- `LoadInitial` reads the main file; `LoadAdditionalFile` deep-merges and optionally registers for reload; `LoadAdditionalDir` recursively loads every `*.conf` in a directory (missing dir is not an error, order is filesystem order).
- Compile-time defaults: `<prefix>/etc/worldserver.conf` + `worldserver.conf.d/`, and the same for bnetserver. CLI: `-c/--config`, `-cd/--config-dir`, `-u/--update-databases-only`.
- Every key can be overridden by `TC_<UPPER_SNAKE_CASE>` env vars (dots/spaces/dashes → `_`, case/number boundaries split). Applied at startup and lazily for absent keys.
- `COPY_CONF=1` copies `.conf.dist` files next to the build output; it does **not** create the live `.conf`. Use `contrib/conf_merge` to merge new dists into an existing config.
- `sWorld->getIntConfig` / `getBoolConfig` are runtime setting IDs (a different mechanism from file-key macros); `CONFIG_*` macros are legacy and almost gone.
- Reload re-reads the main file plus registered additional files, then env overrides, then reloads logging and metrics config. Non-reloadable world options keep their old values and log an error.

## Logging

- Levels: 0 disabled, 1 trace, 2 debug, 3 info, 4 warn, 5 error, 6 fatal. Appender types: 1 console, 2 file, 3 db.
- `Appender.<Name>=type,level,flags,opt1,opt2,opt3`; `Logger.<name>=level,Appender1 Appender2`. Logger lookup is hierarchical by dotted name and falls back to `root`.
- Macros: `TC_LOG_TRACE/DEBUG/INFO/WARN/ERROR/FATAL(filter, fmt, ...)`. `PERFORMANCE_PROFILING` compiles them out. Use `sLog->OutCommand` for command output and `OutCharDump` for character dumps.
- Async logging (`Log.Async.Enable=1`) posts `LogOperation`s onto the main io_context; the loop must be running or messages stay queued. worldserver uses async when enabled; bnetserver is always synchronous. `SetSynchronous()` is only safe after worker threads have joined.

## Threading and io_context

- `Trinity::ThreadPool` wraps `boost::asio::thread_pool` (`PostWork`, `Join`, `Stop`); the servers use a shared `Asio::IoContext` for their main async work.
- `TaskScheduler`/`TaskContext` (steady-clock multiset) handles delayed/repeating game work: `Schedule`, `ScheduleAt`, `Async`, repeat/cancel/reschedule. There is no `DelayedExecutor`.
- `Trinity::Asio::DeadlineTimer` is used by network threads (1 ms update tick) and metrics.
- DB pools and network threads each own their io_context/threads.
- **DB → game handoff:** async DB work posts to the DB pool; completion callbacks are stored in an `AsyncCallbackProcessor` and only run when the owning loop calls `ProcessReadyCallbacks`. That caller may be the world thread, a session/map update, or a network thread — decide which state the callback touches and use the matching processor. Capture GUIDs, not raw object pointers.
- **Network → game handoff:** the network thread only parses and enqueues (`WorldSession::QueuePacket`); gameplay runs on the world/map thread. Outbound packets go to `Socket::QueuePacket` and are drained by the owning network thread.

## Database layer (`src/server/database/`)

- Globals: `WorldDatabase`, `CharacterDatabase`, `LoginDatabase`, `HotfixDatabase` — all `DatabaseWorkerPool<T>`.
- Each pool has async and sync connection groups. API rules:
  - Fire-and-forget async: `Execute`, `PExecute`, `Execute(PreparedStatement*)` — statement must be `CONNECTION_ASYNC`.
  - Blocking fire-and-forget: `DirectExecute` — `CONNECTION_SYNCH`.
  - Blocking query: `Query`, `PQuery`, `Query(PreparedStatement*)` — `CONNECTION_SYNCH`; never call from network/map/world threads.
  - Async query: `AsyncQuery` returns a `QueryCallback`/`std::future`; process with `QueryCallbackProcessor`.
  - Batched: `DelayQueryHolder`.
  - Transactions: `BeginTransaction`, `CommitTransaction`, `AsyncCommitTransaction`, `DirectCommitTransaction`, `ExecuteOrAppend`. Uncommitted transactions roll back.
- Prepared statements: declare the enum in `Database/Implementation/<Db>Database.h` and prepare in the **same order** in `DoPrepareStatements` (`<Db>Database.cpp`); `m_stmts.resize(MAX_<DB>DATABASE_STATEMENTS)` must stay correct. Setters are 0-based. The connection flag must match the API used or the statement is absent on that pool half.
- Results are `shared_ptr` (`QueryResult`, `PreparedQueryResult`); `Field*` is only valid until `NextRow()` or result destruction.
- Startup: `DatabaseLoader` opens → populates base schema → applies updates → prepares statements. `Updates.EnableDatabases` is a bitmask (LOGIN 1, CHARACTER 2, WORLD 4, HOTFIX 8; default 15). world/hotfix base data comes from downloaded TDB full dumps; auth/characters base dumps are in `sql/base/`. See [`sql/AGENTS.md`](../../sql/AGENTS.md).

## Networking

- `Socket<Stream>` owns a read buffer and a write queue; `AsyncRead` loops, `QueuePacket` is the thread-safe producer, `Update` drains writes on the owning thread. Windows uses IOCP; other platforms use writable readiness + `write_some`.
- `NetworkThread` owns one io_context and a 1 ms `DeadlineTimer` that adopts/erases sockets. `SocketMgr` creates the acceptor and N threads, assigns each new socket to the least-loaded thread.
- `WorldSocket`: plain TCP with a custom connection handshake line, AES-256 `WorldPacketCrypt` per direction, 12-byte tags, 4–0x10000 packet size validation, zlib compression above 0x400 for encrypted packets. Authentication (`CMSG_AUTH_SESSION`) is async (`WaitingForQuery`) so the network thread never blocks.
- BNet (`src/server/bnetserver/`): TLS always. Framing is a 2-byte big-endian length, then a protobuf `bgs.protocol.Header`, then payload. `service_id=0xFE` marks a response. Services are dispatched by hash via `ServiceDispatcher`. The login REST service is Boost.Beast HTTPS on `LoginREST.Port` (8081); BNet sockets use `BattlenetPort` (1119). bnetserver needs its PEM cert/key, copied next to the binary at build time.
- Protobuf: checked-in generated `*.pb.{h,cc}` under `src/server/proto/`; only a few `.proto` sources are in-tree. `contrib/protoc-bnet` builds the `protoc-gen-bnet` plugin but is **not** wired into the root CMake build — proto changes require manual regeneration.

## Metrics

- `sMetric`, InfluxDB line protocol over TCP, lock-free `MPSCQueue<MetricData>`, Asio timers. Config: `Metric.Enable`, `Metric.Interval`, `Metric.ConnectionInfo` (`host;port;db`), `Metric.OverallStatusInterval`, `Metric.Threshold.<name>`.
- Macros: `TC_METRIC_EVENT`, `TC_METRIC_VALUE`, `TC_METRIC_TIMER`, `TC_METRIC_DETAILED_EVENT`, `TC_METRIC_DETAILED_TIMER`, `TC_METRIC_DETAILED_NO_THRESHOLD_TIMER`.
- `WITHOUT_METRICS` and `PERFORMANCE_PROFILING` compile metrics out; `WITH_DETAILED_METRICS` gates detailed timers. Detailed timers also need a matching `Metric.Threshold.*` entry or they emit nothing.

## Gotchas

1. Async DB callbacks run on the thread that pumps them, not the DB thread — match the processor to the state you touch.
2. Never block (sync `Query`, `DirectExecute`, `DirectCommitTransaction`) on network, map, or world threads.
3. Prepared-statement enum order and prepare order must stay in lockstep; add new statements at the end of both.
4. `CONNECTION_ASYNC` vs `CONNECTION_SYNCH` mismatch makes a statement silently absent on that connection half.
5. `COPY_CONF` copies `.dist`, not a live `.conf`; `CONF_DIR` is the runtime path.
6. Env overrides use `TC_` + upper-snake key; `GetStringDefault` strips all `"` characters.
7. Async logging needs the io_context loop to keep running; otherwise messages queue.
8. BNet header length is a 16-bit big-endian prefix; response packets need `service_id=0xFE`.
9. `src/common/Time` uses a 32-bit wrapping millisecond clock — use `getMSTimeDiff`.
10. Syscall/network callbacks must not touch map/player state; enqueue instead.
