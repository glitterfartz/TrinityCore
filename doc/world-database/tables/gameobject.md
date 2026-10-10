# gameobject

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Persistent gameobject spawns and their placements, rotations, phases, and difficulty settings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Gameobject System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Persistent spawn ID; separate from gameobject_template.entry. |
| 2 | `id` | `int unsigned` | NO | `0` | — | — | Gameobject template entry referenced by this spawn. |
| 3 | `map` | `smallint unsigned` | NO | `0` | — | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 4 | `zoneId` | `smallint unsigned` | NO | `0` | — | — | Zone AreaTable identifier. |
| 5 | `areaId` | `smallint unsigned` | NO | `0` | — | — | AreaTable identifier. |
| 6 | `spawnDifficulties` | `varchar(100)` | NO | `0` | — | — | Comma-separated difficulty IDs; this is not the older spawnMask bit field. |
| 7 | `phaseUseFlags` | `tinyint unsigned` | NO | `0` | — | — | Phase interpretation flags; see phase enums and the spawn loader. |
| 8 | `PhaseId` | `int` | YES | `0` | — | — | Phase identifier used for visibility; examine phaseUseFlags and PhaseGroup together. |
| 9 | `PhaseGroup` | `int` | YES | `0` | — | — | Client phase-group identifier; do not confuse with an individual phase ID. |
| 10 | `terrainSwapMap` | `int` | NO | `-1` | — | — | Terrain replacement map selector; negative sentinel values are loader-specific. |
| 11 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 12 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 13 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 14 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 15 | `rotation0` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `rotation1` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 17 | `rotation2` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `rotation3` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 19 | `spawntimesecs` | `int` | NO | `0` | — | — | Respawn delay in seconds; actual timing is also affected by spawn groups, instances, events, and linked respawns. |
| 20 | `animprogress` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 21 | `state` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 22 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 23 | `StringId` | `varchar(64)` | YES | NULL / absent; see conventions | — | — | Author-defined string identifier used by object lookup and string-ID conditions. |
| 24 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gameobject](gameobject.md).`id` → [gameobject_template](gameobject_template.md).`entry`: Template identity shared by gameobject spawns.
- [gameobject_addon](gameobject_addon.md).`guid` → [gameobject](gameobject.md).`guid`: Per-spawn addon.
- [game_event_gameobject](game_event_gameobject.md).`guid` → [gameobject](gameobject.md).`guid`: Event-controlled object spawn.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2485](../../../src/server/game/Globals/ObjectMgr.cpp#L2485)
- [src/server/game/Globals/ObjectMgr.cpp:7357](../../../src/server/game/Globals/ObjectMgr.cpp#L7357)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:31](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L31)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:68](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L68)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:73](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L73)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:78](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L78)
- [src/server/scripts/Commands/cs_gobject.cpp:190](../../../src/server/scripts/Commands/cs_gobject.cpp#L190)
- [src/server/scripts/Commands/cs_gobject.cpp:198](../../../src/server/scripts/Commands/cs_gobject.cpp#L198)
- [src/server/scripts/Commands/cs_gobject.cpp:225](../../../src/server/scripts/Commands/cs_gobject.cpp#L225)
- [src/server/scripts/Commands/cs_list.cpp:363](../../../src/server/scripts/Commands/cs_list.cpp#L363)

Additional source references exist; search the repository for the exact table name.

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `guid` | `ObjectGuid::LowType guid = fields[0].GetUInt64()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L382) |
| `id` | `uint32 entry        = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2513) |
| `map` | `data.mapId          = fields[2].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2545) |
| `spawnDifficulties` | `data.spawnDifficulties      = ParseSpawnDifficulties(fields[14].GetStringView(), "gameobject", guid, data.mapId, spawnMasks[data.mapId])` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2598) |
| `phaseUseFlags` | `data.phaseUseFlags  = fields[17].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2607) |
| `terrainSwapMap` | `data.terrainSwapMap = fields[20].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2648) |
| `position_x` | `float x         = fields[1].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L383) |
| `position_y` | `float y         = fields[2].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L384) |
| `position_z` | `float z         = fields[3].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L385) |
| `orientation` | `data.spawnPoint.Relocate(fields[3].GetFloat(), fields[4].GetFloat(), fields[5].GetFloat(), fields[6].GetFloat())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2546) |
| `rotation0` | `data.rotation.x     = fields[7].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2547) |
| `rotation1` | `data.rotation.y     = fields[8].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2548) |
| `rotation2` | `data.rotation.z     = fields[9].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2549) |
| `rotation3` | `data.rotation.w     = fields[10].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2550) |
| `spawntimesecs` | `data.spawntimesecs  = fields[11].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2551) |
| `animprogress` | `data.animprogress   = fields[12].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2584) |
| `state` | `uint32 go_state     = fields[13].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2587) |
| `ScriptName` | `data.scriptId = GetScriptId(fields[21].GetStringView())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2664) |
| `StringId` | `data.StringId = fields[22].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2665) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gameobject` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gameobject) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
