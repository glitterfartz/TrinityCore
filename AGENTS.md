# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Codex, etc.) when working with code in this repository.

TrinityCore is an open-source World of Warcraft server emulator. This checkout is branch `master` (12.x / TDB 1210.26091), C++20, built with CMake (this checkout uses Ninja). Two server binaries: **`worldserver`** (the game world) and **`bnetserver`** (Battle.net/auth + REST login). There is no `authserver` in this branch.

## Where to read next

This root file gives the big picture. Module-specific guidance lives in nested files:

- [`src/server/scripts/AGENTS.md`](src/server/scripts/AGENTS.md) — **script content and scripting API** (registration model, every script type, dungeon wiring, DB bindings, commands, spells). Read this before touching content.
- [`src/server/game/AGENTS.md`](src/server/game/AGENTS.md) — engine runtime: startup, world/map tick, threading, object model, grids/collision, session/opcode flow.
- [`sql/AGENTS.md`](sql/AGENTS.md) — the four schemas (especially the `world` vs `hotfixes` split), table taxonomy, update workflow, query recipes.
- [`src/common/AGENTS.md`](src/common/AGENTS.md) — shared infrastructure: config, logging, threading, database pools, networking, metrics.

## Repository layout

| Path | Role | Scale |
|---|---|---|
| `src/server/game/` | Game engine: entities, maps, AI, spells, quests, instances, handlers | ~452k LOC, 743 files |
| `src/server/scripts/` | Content scripts (bosses, dungeons, zones, spells, commands) | ~406k LOC, 842 cpp |
| `src/common/` | Shared utilities: Asio, networking, config, logging, crypto, collision, DB2 file parsing | ~31k LOC |
| `src/server/database/` | Database worker pools, prepared statements, DB updater | ~12k LOC |
| `src/server/shared/` | Packet serialization, realm list | |
| `src/server/bnetserver/` | Battle.net + HTTPS login REST server | |
| `src/server/proto/` | Checked-in protobuf `.pb.*` for BNet | |
| `src/tools/` | Map/vmap/mmap extractors and assemblers | |
| `dep/` | Vendored third-party libraries | |
| `sql/` | Schema, TDB data notes, updates, historical archive | `sql/old` is 4+ GB |
| `tests/` | Catch2 tests | |

Build outputs live under `build/bin/<Config>/bin/` (UNIX), *not* directly in `build/bin/`.

## Build

This working copy already has a Ninja + Clang **Debug** build in `build/`. For incremental work:

```bash
cd /home/tanner/Development/private-servers/servers/TrinityCore/trinitycore-master
cmake --build build --target worldserver
cmake --build build --target bnetserver
cmake --build build --target mapextractor vmap4extractor vmap4assembler mmaps_generator
# or run the whole build: ninja -C build
```

The CMake target names are the executable names; the actual binaries land at `build/bin/Debug/bin/`.

Fresh configure (out-of-source is mandatory; the build directory cannot be the source directory):

```bash
cmake -S . -B build -G Ninja \
  -DCMAKE_BUILD_TYPE=RelWithDebInfo \
  -DCMAKE_INSTALL_PREFIX="$PWD/install" \
  -DSERVERS=1 -DSCRIPTS=static -DTOOLS=1 -DBUILD_TESTING=0
cmake --build build --parallel "$(nproc)"
```

Key options and defaults (`cmake/options.cmake`): `SERVERS=1`, `SCRIPTS=static` (`none|static|dynamic|minimal-static|minimal-dynamic`), `TOOLS=1`, `USE_COREPCH=1`, `USE_SCRIPTPCH=1`, `WITH_DYNAMIC_LINKING=0`, `WITH_WARNINGS=0`, `WITH_WARNINGS_AS_ERRORS=0`, `WITH_COREDEBUG=0`, `WITHOUT_METRICS=0`, `COPY_CONF=1`, `BUILD_TESTING=0`. Never enable `WITH_COREDEBUG` for crash logs — use `RelWithDebInfo`. Per-module script overrides: `-DSCRIPTS_<UPPERDIR>=default|disabled|static|dynamic`; `minimal-*` enables only `Commands` and `Spells`, disabling `Custom` and every expansion.

Installed layout (UNIX): executables → `<prefix>/bin`, configs → `<prefix>/etc`, dynamic script modules → `<prefix>/bin/scripts`. Because `COPY_CONF=1`, `.conf.dist` copies appear in `build/bin/<Config>/etc/`; they are *dist* files, not live configs.

Running from the build tree:

```bash
cd build/bin/Debug/bin
./worldserver -c ../etc/worldserver.conf     # copy/rename the .dist to .conf first
```

`worldserver` also needs runtime data (`dbc/`, `maps/`, `vmaps/`, `mmaps/`) in `DataDir` (defaults to `.`). Use `-u` / `--update-databases-only` to run only the DB updater.

## Tests

Tests are off in the current build. Enable once, then build and run:

```bash
cmake -S . -B build -DBUILD_TESTING=ON
cmake --build build --target tests --parallel "$(nproc)"
ctest --test-dir build --output-on-failure
ctest --test-dir build -R "Insertion"                  # one test by name
./build/bin/Debug/bin/tests "[EventMap]"               # run by Catch2 tag
./build/bin/Debug/bin/tests --list-tests
```

Framework is Catch2 v3 (fetched at configure time, so `BUILD_TESTING=ON` needs network). Tests live in `tests/common/` and `tests/game/`; a new `.cpp` there is globbed automatically, but re-run CMake. CI also runs `cmake --build <dir> --target test`.

## Architecture at a glance

**Libraries.** `common` → `database` / `shared` / `proto` → `game` → `scripts`, linked into `worldserver`. `bnetserver` links `common`, `database`, `shared`, `proto` only.

**Startup (worldserver).** `src/server/worldserver/Main.cpp:main()` loads config, initializes logging/SSL, starts DB pools (`Login`, `Character`, `World`, `Hotfix`), then `World::SetInitialWorldSettings()` loads all templates/DB2 data, calls `ScriptMgr::Initialize()`, initializes the opcode table and map manager, starts the network, and enters `WorldUpdateLoop()`. There is no `Master.cpp`.

**Tick.** `WorldUpdateLoop()` computes a millisecond `diff`, sleeps to `MinWorldUpdateTime`, and calls `World::Update(diff)`. `World::Update` drains sessions, submits every map to `MapUpdater` worker threads and waits, then runs `Map::DelayedUpdate` on the world thread. `Map::Update` ticks players plus active-cell objects, flushes object-update packets, and runs map scripts. Gameplay time is always milliseconds (`getMSTimeDiff`, `IntervalTimer`); use `GameTime` for persisted time.

**Threading model (the rule that causes the most bugs).**
- World thread: sessions, global managers, map scheduling, `Map::DelayedUpdate`, `PROCESS_THREADUNSAFE` opcodes.
- Map worker threads: `Map::Update`, creature AI, `InstanceScript::Update`, `PROCESS_THREADSAFE` opcodes. Never touch another map or the global player registry from here.
- Network threads: handshake, encryption, framing, send queues only. Never gameplay state.
- DB threads: execute queries; **callbacks run on whichever thread calls `ProcessReadyCallbacks`** (world, session/map, or network), not on the DB thread.
- Scripts: registration timing is `ScriptMgr::Initialize()`; scripts are not static-initializer registered.

**Scripts.** Every directory under `src/server/scripts/` is a module with a hand-maintained `<module>_script_loader.cpp` exporting `Add<Module>Scripts()`. CMake generates `ScriptLoader.cpp`, and `ScriptMgr::Initialize()` invokes `AddScripts()`. DB `ScriptName` strings are matched exactly (case-sensitive) against the C++ constructor/macro name. See the scripts guide for the full API.

**Interfaces.** Client opcodes are declared in `src/server/game/Server/Protocol/Opcodes.cpp` and handled by `WorldSession::Handle*` methods in `src/server/game/Handlers/`. Each opcode carries a `PacketProcessing` mode (`PROCESS_INPLACE`, `PROCESS_THREADSAFE`, `PROCESS_THREADUNSAFE`) that decides which pass processes it.

## Data and databases

Four schemas: `world` (authoring content), `hotfixes` (sparse client-DB2 overlay; there is **no `item_template`**), `auth` (accounts/RBAC/realm list), `characters` (character state and instance saves). Base schemas for auth/characters are in `sql/base/`; world/hotfixes are populated from downloaded TDB full dumps (`TDB_full_world_1210.26091_2026_09_09.sql`, `TDB_full_hotfixes_...`) by the startup updater (`Updates.AutoSetup=1`). Do not import `sql/base/dev/*` — they are developer dumps.

Content changes ship as `sql/updates/{world,hotfixes,auth,characters}/master/YYYY_MM_DD_NN_<db>.sql`, applied in filename order and tracked in each schema's `updates` / `updates_include` tables. Never edit an applied update; use idempotent DELETE-then-INSERT. See [`sql/AGENTS.md`](sql/AGENTS.md) for the schema map, join keys, and query recipes.

**Database research:** check for the local MariaDB MCP server with live `world` / `auth` / `characters` / `hotfixes` connections before searching through SQL files. The SQL files are history, not current state. Do not use the unrelated `acore_*` / `acworld` schemas on that server, and never put DB passwords in commands, files, or replies.

## Tools (runtime data extraction)

`mapextractor` → `vmap4extractor` → `vmap4assembler Buildings vmaps` → `mmaps_generator`, run against a WoW client. Results go to the server's `DataDir` as `dbc/`, `maps/`, `vmaps/`, `mmaps/` (and `cameras/`, `gt/`). `mmaps_generator` in a Debug build refuses to run without `--allowDebug`. `contrib/extractor.sh` wraps the whole sequence.

## Code conventions and gotchas

- **Out-of-source only.** `cmake .` in the repo is rejected.
- **Style:** 4 spaces, no tabs, no trailing whitespace, no 3+ consecutive blank lines, max line 160; C/C++ files use latin1 in `.editorconfig`. `contrib/check_codestyle.sh` enforces the whitespace/tab rules over `src/` (plus "no `TC_LOG_*.GetCounter`"). There is no `.clang-format`/`.clang-tidy`.
- **PCH:** `USE_COREPCH` / `USE_SCRIPTPCH` force-include the PCH via CMake. Do not `#include` the PCH from a `.cpp`, but do include what you use so `-DUSE_SCRIPTPCH=0` compiles. `ScriptPCH.h` is at `src/server/scripts/ScriptPCH.h`.
- **Time:** use `getMSTimeDiff`, not raw timestamp subtraction (32-bit wrapping clock).
- **Object lifetime:** queue removals with `Map::AddObjectToRemoveList`; never delete map objects directly. `AddToWorld` / `RemoveFromWorld` are subclass-specific and must stay balanced.
- **Active objects only tick near players.** Use `setActive(true)` for creatures/objects that must always update.
- **Async DB:** capture stable keys (`ObjectGuid`), not raw pointers, in callbacks; the object may be gone.
- **Assertions are live** in normal builds (`ASSERT` aborts, it does not throw). They only disappear under `PERFORMANCE_PROFILING`.
- **`item_template` does not exist** in this branch. Item definitions are `hotfixes.item` / `hotfixes.item_sparse`.
- **Stale docs:** `doc/HowToScript.txt` and several `doc/*.dox` pages describe removed files/APIs (`scripts_STAT_SRCS`, `RegisterAuraScript`). Trust the source and CMake.
- Builds are heavy (~445 MB Debug `worldserver`); prefer Ninja + parallel and touching an existing build rather than reconfiguring.
