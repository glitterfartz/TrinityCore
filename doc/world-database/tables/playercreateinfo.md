# playercreateinfo

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Starting map and position by race and class.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `race` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `class` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `map` | `smallint unsigned` | NO | `0` | — | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 4 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 5 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 6 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 7 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 8 | `npe_map` | `int unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `npe_position_x` | `float` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `npe_position_y` | `float` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 11 | `npe_position_z` | `float` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 12 | `npe_orientation` | `float` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `npe_transport_guid` | `bigint unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `intro_movie_id` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `intro_scene_id` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `npe_intro_scene_id` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `race`, `class` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:3820](../../../src/server/game/Globals/ObjectMgr.cpp#L3820)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `race` | `uint32 current_race  = fields[0].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3835) |
| `class` | `uint32 current_class = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3836) |
| `map` | `uint32 mapId         = fields[2].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3837) |
| `position_x` | `float  positionX     = fields[3].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3838) |
| `position_y` | `float  positionY     = fields[4].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3839) |
| `position_z` | `float  positionZ     = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3840) |
| `orientation` | `float  orientation   = fields[6].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3841) |
| `npe_orientation` | `info->createPositionNPE->Loc.WorldRelocate(fields[7].GetUInt32(), fields[8].GetFloat(), fields[9].GetFloat(), fields[10].GetFloat(), fields[11].GetFloat())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3887) |
| `npe_transport_guid` | `info->createPositionNPE->TransportGuid = fields[12].GetUInt64OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3888) |
| `intro_movie_id` | `info->introMovieId = fields[13].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3905) |
| `intro_scene_id` | `info->introSceneId = fields[14].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3913) |
| `npe_intro_scene_id` | `info->introSceneIdNPE = fields[15].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3921) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `playercreateinfo` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/playercreateinfo) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
