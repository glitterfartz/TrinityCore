# AGENTS.md — src/server/game

Guidance for AI coding agents working on the TrinityCore game engine. This is the largest module (~452k LOC, 743 files). It owns the server runtime, world state, entities, maps, combat, spells, quests, and the hook points that content scripts plug into. Script authoring itself is covered in [`../scripts/AGENTS.md`](../scripts/AGENTS.md); build/test commands and database rules are in the root [`AGENTS.md`](../../../AGENTS.md) and [`sql/AGENTS.md`](../../../sql/AGENTS.md).

## Startup

Entry point is `src/server/worldserver/Main.cpp:main()` — there is **no `Master.cpp`**. Order:

1. Config (`sConfigMgr`), logging, SSL, signal handler, shared `Asio::IoContext` + thread pool.
2. `StartDB()` creates `LoginDatabase`, `CharacterDatabase`, `WorldDatabase`, `HotfixDatabase` pools; each pool opens, populates, updates, then prepares statements.
3. `sScriptMgr->SetScriptLoader(AddScripts)` is called here, but the loader executes later.
4. `World::SetInitialWorldSettings()` (`World/World.cpp`) loads config, GUIDs, pools, DB2/hotfix stores, vmap/mmap managers, spell data, creature/GO/item/quest templates, then calls `sScriptMgr->Initialize()`, then `sMapMgr->Initialize()`, game events, `opcodeTable.Initialize()`, battleground/outdoor PvP/battlefield managers.
5. Network starts (`WorldSocketMgr::StartNetwork`), realm goes online, `WorldUpdateLoop()` runs.

`bnetserver` is separate (`src/server/bnetserver/Main.cpp`): only `LoginDatabase`, no `World`/`MapManager`/scripts, TLS Battle.net socket service plus an HTTPS login REST service.

## Tick and threading

`WorldUpdateLoop()` computes a millisecond `diff` and calls `World::Update(diff)`. Its order matters:

1. Game time/shutdown countdown, periodic world timers, who-list, channel save, resets.
2. Auctions, black market, AHBot.
3. `sScriptMgr->SyncScripts()`, hot-swap check.
4. `UpdateSessions(diff)` — drains the session queues, runs `PROCESS_THREADUNSAFE` opcodes, removes dead sessions.
5. `sMapMgr->Update(diff)` — each map is submitted to `MapUpdater` worker threads; the world thread blocks in `wait()`, then runs `Map::DelayedUpdate` for every map serially.
6. Battlegrounds, OutdoorPvP, Battlefields, groups, LFG.
7. `ProcessQueryCallbacks()`, corpse cleanup, game events, DB keepalive, guild save, world states, CLI commands.
8. `sScriptMgr->OnWorldUpdate(diff)`, metrics.

Thread-affinity rules (the biggest source of bugs):

- **World thread:** global managers, session lifecycle, map scheduling, `Map::DelayedUpdate`, `PROCESS_THREADUNSAFE` handlers.
- **Map worker threads:** `Map::Update`, object `Update(diff)`, creature AI, `InstanceScript::Update`, `PROCESS_THREADSAFE` handlers. Never touch another map, the global player registry, or world-level containers here.
- **Network threads:** protocol handshake, encryption/compression, socket read/write, packet queueing. No gameplay state.
- **DB threads:** run queries only. Async callbacks execute on the thread that calls `ProcessReadyCallbacks` (world, session/map, or network), not the DB thread.
- `MapUpdate.Threads` defaults to 1 but is clamped to ≥1, so map updates always run on worker threads.
- `Map::DelayedUpdate` (grid state, queued removals, respawns) runs on the world thread after all map threads finish.

## Object model (`Entities/`)

```
BaseEntity                    guid, in-world flag, update fields, dirty bits
└── Object                    update-field blocks, AddToWorld/RemoveFromWorld
    ├── WorldObject           map position, phase, visibility, grid activation
    │   ├── Unit              health, auras, spells, movement, AI, combat
    │   │   ├── Player        (also GridObject<Player>)
    │   │   └── Creature      (GridObject<Creature>, MapObject)
    │   │       └── TempSummon → Minion → Guardian → Pet
    │   │           └── Totem
    │   ├── GameObject        (GridObject, MapObject) → Transport
    │   ├── DynamicObject
    │   ├── AreaTrigger
    │   ├── Conversation
    │   ├── SceneObject
    │   └── Corpse
    └── Item                  (not a WorldObject; lives in bags/inventory)
```

Update flow: `Map::AddToMap` → `AddToGrid` → `obj->AddToWorld()` → `UpdateObjectVisibilityOnCreate` → optionally `AddToActive`. `Map::Update` calls `Player::Update` directly and uses `ObjectUpdater` grid visitors for nearby creatures/GOs/triggers. `WorldObject::Update` processes `m_Events` and heartbeat; `Unit::Update` handles spells/auras/combat/attack timers/motion/AI; `Creature::Update` handles death state, AI, regen.

Update-field changes only mark the object dirty (`SetUpdateFieldValue`). `Map::SendObjectUpdates` builds and sends the packets once per map tick, so changes made late in a tick go out next tick.

Removal: call `Map::AddObjectToRemoveList`; actual deletion happens in `DelayedUpdate`. `BaseEntity::~BaseEntity` aborts if the object is still in world/update lists.

## Maps and grids (`Maps/`, `Grids/`)

- `MapManager` owns `std::map<(mapId, instanceId), Map>` behind a shared mutex. `FindMap` takes the lock; the world-thread update/destroy loop deliberately does not.
- `Map::EnsureGridCreated` allocates a grid and loads terrain/vmap/mmap; `EnsureGridLoaded` then loads DB creatures/GOs/triggers/corpses. A grid can exist unloaded — check `IsGridLoaded`.
- Grid lifecycle is `Invalid → Active → Idle → Removal`, driven by `Map::DelayedUpdate`; BG/arena maps skip idle unloading.
- Overworld maps never unload. Instances arm `m_unloadTimer` when the last player leaves and are destroyed on the world thread.
- Collision: `.map` terrain (`TerrainInfo`), vmaps for line-of-sight, mmaps/Recast-Detour navmesh via `PathGenerator`. A dynamic collision tree handles temporary obstacles.
- `InstanceMap::Update` runs `Map::Update` then `InstanceScript::Update` and scenario updates. `InstanceMap::CreateInstanceData` resolves the DB `instance_template` script id.

## Sessions, packets, opcodes (`Server/`, `Handlers/`)

- `WorldSocket` frames/decrypts on the network thread and pushes packets into a per-session queue. Auth, ping, and keepalive are handled inline; everything else is queued.
- `WorldSession::Update(diff, filter)` is called **twice per tick**:
  - `MapSessionFilter` in `Map::Update` processes `PROCESS_THREADSAFE` (and `PROCESS_INPLACE`) packets on the map worker.
  - `WorldSessionFilter` in `World::UpdateSessions` processes `PROCESS_THREADUNSAFE` (and `PROCESS_INPLACE`, plus everything for sessions without an in-world player) on the world thread. Logout/kick/socket cleanup only happen here.
- Opcodes are declared in `Server/Protocol/Opcodes.cpp`; each has a `PacketProcessing` mode and a handler that calls a `WorldSession::Handle*` method. Declarations live in `Server/WorldSession.h`; implementations in `Handlers/*.cpp`.
- `WorldSession::SendPacket` rejects invalid server opcodes, unhandled opcodes, and wrong connection types unless forced.
- Async DB work on a session is drained by the session's `QueryCallbackProcessor` in `WorldSession::ProcessQueryCallbacks`, i.e. on that session's update thread.

## Managers and singletons

Convention: `#define sX X::instance()` backed by a function-local static (`sWorld`, `sObjectMgr`, `sMapMgr`, `sScriptMgr`, `sConfigMgr`, `sLog`, `sDB2Manager`, `sSpellMgr`, `sConditionMgr`, `sPoolMgr`, `sGameEventMgr`, `sBattlegroundMgr`, `sLFGMgr`, `sGuildMgr`, …). DB pools are plain globals: `WorldDatabase`, `CharacterDatabase`, `LoginDatabase`, `HotfixDatabase`.

- `ObjectMgr` caches world-DB templates (creatures, GOs, items, quests, pages, gossip, instance templates, event scripts). Treat as read-only after startup.
- `ObjectAccessor` holds the global player registry. `FindPlayer*` is only safe from the world thread; `GetPlayer(map, guid)` is the map-scoped form.
- `sDB2Manager` and DB2 storage globals are read-only after startup and safe to query from map threads.
- Most managers are global, not per-map; a mutation is visible to every map thread.

## Content hook points

- AI: `UnitAI → CreatureAI → ScriptedAI / BossAI / SmartAI`, `GameObjectAI`, `PlayerAI`. Creature AI is selected by DB `ScriptName` first, then `AIName`; assigned in `Creature::AddToWorld`/`AIM_Initialize`.
- `InstanceScript` + `BossAI` own encounter state, doors, minions, and journal credit. `BossAI` maps a creature to its instance script; use it for real encounters and `ScriptedAI` for adds/trash.
- Spells: `Spell`/`Aura`/`AuraEffect` runtime, `SpellMgr`/`SpellInfo` static data, `SpellEffects.cpp` effect handler table. Script hooks fire throughout the cast pipeline and can suppress default effects.
- Conditions: `ConditionMgr` loads the `conditions` table, distributes rows per source type, and answers `IsObjectMeetToConditions`.
- Quests: `Quest` templates in `ObjectMgr`, runtime progress on `Player`, `QuestScript` hooks for status/objective changes.
- Battlegrounds/OutdoorPvP/Battlefields/Scenarios are `ZoneScript`-derived managers; map logic lives in `BattlegroundScript`, `OutdoorPvPScript`, `BattlefieldScript`. Scenarios are data-driven.

## Gotchas

1. Map updates never run on the world thread; code that assumes otherwise will race.
2. `PROCESS_THREADSAFE` handlers may only touch their own map. Cross-map or global access is unsafe.
3. Session removal/logout is only valid in the world-thread pass.
4. Don't delete map objects directly — queue them.
5. Objects in inactive grids don't tick; use `setActive(true)` for always-running NPCs/objects.
6. `AddToWorld`/`RemoveFromWorld` and `AddToMap`/`RemoveFromMap` are not symmetric across subclasses; keep them balanced.
7. Player world membership is separate from `ObjectAccessor` membership; login adds the player to the accessor explicitly.
8. Async DB callbacks may run on any thread that pumps them; capture GUIDs, not raw pointers, and don't block.
9. `getMSTime()` is 32-bit and wraps; use `getMSTimeDiff`.
10. Assertions abort in normal builds; they are not exceptions.
11. Config reload is partial — non-reloadable settings keep their old values.
12. Instances unload themselves when empty; don't hold raw pointers to their objects across ticks.
13. `World::StopNow` only sets an atomic; graceful shutdown goes through `ShutdownServ` and the shutdown timer.
14. MapManager map iteration is world-thread-only; use `FindMap`/`DoForAllMaps` elsewhere.

## Key files

`World/World.cpp` (settings and tick), `Maps/MapManager.cpp`, `Maps/Map.cpp`, `Maps/MapUpdater.cpp`, `Maps/GridStates.cpp`, `Entities/Object/Object.cpp`, `Entities/Unit/Unit.cpp`, `Entities/Creature/Creature.cpp`, `Server/WorldSession.cpp`, `Server/Protocol/Opcodes.cpp`, `Handlers/CharacterHandler.cpp`, `Scripting/ScriptMgr.cpp`, `AI/CreatureAI.cpp` + `AI/ScriptedAI/ScriptedCreature.cpp`, `Instances/InstanceScript.cpp`, `Spells/Spell.cpp` + `Spells/SpellEffects.cpp`, `Conditions/ConditionMgr.cpp`.
