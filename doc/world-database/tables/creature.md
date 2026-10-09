# creature

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Persistent NPC spawns: template, placement, phase, difficulty, and per-spawn overrides.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Persistent spawn ID; separate from creature_template.entry and the runtime object GUID. |
| 2 | `id` | `int unsigned` | NO | `0` | MUL | — | Creature template entry referenced by this spawn. |
| 3 | `map` | `smallint unsigned` | NO | `0` | MUL | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 4 | `zoneId` | `smallint unsigned` | NO | `0` | — | — | Zone AreaTable identifier. |
| 5 | `areaId` | `smallint unsigned` | NO | `0` | — | — | AreaTable identifier. |
| 6 | `spawnDifficulties` | `varchar(100)` | NO | `0` | — | — | Comma-separated difficulty IDs; this is not the older spawnMask bit field. |
| 7 | `phaseUseFlags` | `tinyint unsigned` | NO | `0` | — | — | Phase interpretation flags; see phase enums and the spawn loader. |
| 8 | `PhaseId` | `int` | YES | `0` | — | — | Phase identifier used for visibility; examine phaseUseFlags and PhaseGroup together. |
| 9 | `PhaseGroup` | `int` | YES | `0` | — | — | Client phase-group identifier; do not confuse with an individual phase ID. |
| 10 | `terrainSwapMap` | `int` | NO | `-1` | — | — | Terrain replacement map selector; negative sentinel values are loader-specific. |
| 11 | `modelid` | `int unsigned` | NO | `0` | — | — | Optional spawn display-model override. |
| 12 | `equipment_id` | `tinyint` | NO | `0` | — | — | Equipment-set selector; signed sentinel values are interpreted by the spawn/equipment loaders. |
| 13 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 14 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 15 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 16 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 17 | `spawntimesecs` | `int unsigned` | NO | `120` | — | — | Respawn delay in seconds; actual timing is also affected by spawn groups, instances, events, and linked respawns. |
| 18 | `wander_distance` | `float` | NO | `0` | — | — | Random movement radius around the spawn location. |
| 19 | `currentwaypoint` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 20 | `curHealthPct` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Optional starting health percentage override. |
| 21 | `MovementType` | `tinyint unsigned` | NO | `0` | — | — | Default movement generator type; see MovementGeneratorType. |
| 22 | `npcflag` | `bigint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 23 | `unit_flags` | `int unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 24 | `unit_flags2` | `int unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 25 | `unit_flags3` | `int unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 26 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 27 | `StringId` | `varchar(64)` | YES | NULL / absent; see conventions | — | — | Author-defined string identifier used by object lookup and string-ID conditions. |
| 28 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `idx_id` | No | `id` | BTREE |
| `idx_map` | No | `map` | BTREE |
| `PRIMARY` | Yes | `guid` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature](creature.md).`id` → [creature_template](creature_template.md).`entry`: Template identity shared by NPC spawns.
- [creature_addon](creature_addon.md).`guid` → [creature](creature.md).`guid`: Per-spawn addon; template addon provides defaults.
- [creature_movement_override](creature_movement_override.md).`SpawnId` → [creature](creature.md).`guid`: Per-spawn movement settings.
- [game_event_creature](game_event_creature.md).`guid` → [creature](creature.md).`guid`: Event-controlled NPC spawn.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:501](../../../src/server/game/Events/GameEventMgr.cpp#L501)
- [src/server/game/Globals/ObjectMgr.cpp:1545](../../../src/server/game/Globals/ObjectMgr.cpp#L1545)
- [src/server/game/Globals/ObjectMgr.cpp:2125](../../../src/server/game/Globals/ObjectMgr.cpp#L2125)
- [src/server/game/Globals/ObjectMgr.cpp:7353](../../../src/server/game/Globals/ObjectMgr.cpp#L7353)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:40](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L40)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:43](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L43)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:44](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L44)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:45](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L45)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:64](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L64)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:67](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L67)

Additional source references exist; search the repository for the exact table name.

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `guid` | `ObjectGuid::LowType guid = fields[0].GetUInt64()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L114) |
| `id` | `uint32 entry        = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2154) |
| `map` | `data.mapId          = fields[2].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2166) |
| `spawnDifficulties` | `data.spawnDifficulties = ParseSpawnDifficulties(fields[14].GetStringView(), "creature", guid, data.mapId, spawnMasks[data.mapId])` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2176) |
| `equipment_id` | `data.equipmentId    = fields[8].GetInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2170) |
| `position_x` | `float x         = fields[1].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L115) |
| `position_y` | `float y         = fields[2].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L116) |
| `position_z` | `float z         = fields[3].GetFloat()` | [loader](../../../src/server/scripts/Commands/cs_list.cpp#L117) |
| `orientation` | `data.spawnPoint.Relocate(fields[3].GetFloat(), fields[4].GetFloat(), fields[5].GetFloat(), fields[6].GetFloat())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2167) |
| `spawntimesecs` | `data.spawntimesecs  = fields[9].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2171) |
| `wander_distance` | `data.wander_distance = fields[10].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2172) |
| `currentwaypoint` | `data.currentwaypoint = fields[11].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2173) |
| `curHealthPct` | `data.curHealthPct   = fields[12].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2174) |
| `MovementType` | `data.movementType   = fields[13].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2175) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
