# areatrigger

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Persistent area-trigger spawn placements.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpawnId` | `bigint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `AreaTriggerCreatePropertiesId` | `int unsigned` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `IsCustom` | `tinyint unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `MapId` | `int unsigned` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `SpawnDifficulties` | `varchar(100)` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `PosX` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `PosY` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `PosZ` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `Orientation` | `float` | NO | NULL / absent; see conventions | — | — | Facing angle in radians; NULL may leave orientation unspecified according to the loader. |
| 10 | `PhaseUseFlags` | `tinyint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `PhaseId` | `int unsigned` | YES | `0` | — | — | Phase identifier used for visibility; examine phaseUseFlags and PhaseGroup together. |
| 12 | `PhaseGroup` | `int unsigned` | YES | `0` | — | — | Client phase-group identifier; do not confuse with an individual phase ID. |
| 13 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 14 | `Comment` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |
| 15 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpawnId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/AreaTriggerDataStore.cpp:407](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L407)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpawnId` | `ObjectGuid::LowType spawnId = fields[0].GetUInt64()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L413) |
| `IsCustom` | `AreaTriggerCreatePropertiesId createPropertiesId = { fields[1].GetUInt32(), fields[2].GetBool() }` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L414) |
| `SpawnDifficulties` | `std::vector<Difficulty> difficulties = sObjectMgr->ParseSpawnDifficulties(fields[4].GetStringView(), "areatrigger", spawnId, location.GetMapId(), spawnMasks[location.GetMapId()])` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L472) |
| `Orientation` | `WorldLocation location(fields[3].GetUInt32(), fields[5].GetFloat(), fields[6].GetFloat(), fields[7].GetFloat(), fields[8].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L415) |
| `PhaseUseFlags` | `spawn.phaseUseFlags = fields[9].GetUInt8()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L485) |
| `PhaseId` | `spawn.phaseId = fields[10].GetUInt32()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L486) |
| `PhaseGroup` | `spawn.phaseGroup = fields[11].GetUInt32()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L487) |
| `ScriptName` | `spawn.scriptId = sObjectMgr->GetScriptId(fields[12].GetStringView())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L489) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `areatrigger` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/areatrigger) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
