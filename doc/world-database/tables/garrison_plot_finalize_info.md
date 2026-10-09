# garrison_plot_finalize_info

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Faction-specific plot completion positions and animations.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `garrPlotInstanceId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `hordeGameObjectId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `hordeX` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `hordeY` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `hordeZ` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `hordeO` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `hordeAnimKitId` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `allianceGameObjectId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `allianceX` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `allianceY` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 11 | `allianceZ` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 12 | `allianceO` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `allianceAnimKitId` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `garrPlotInstanceId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Garrison/GarrisonMgr.cpp:344](../../../src/server/game/Garrison/GarrisonMgr.cpp#L344)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `garrPlotInstanceId` | `uint32 garrPlotInstanceId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L357) |
| `hordeGameObjectId` | `uint32 hordeGameObjectId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L358) |
| `hordeO` | `info.FactionInfo[GARRISON_FACTION_INDEX_HORDE].Pos.Relocate(fields[2].GetFloat(), fields[3].GetFloat(), fields[4].GetFloat(), fields[5].GetFloat())` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L415) |
| `hordeAnimKitId` | `uint16 hordeAnimKitId = fields[6].GetUInt16()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L360) |
| `allianceGameObjectId` | `uint32 allianceGameObjectId = fields[7].GetUInt32()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L359) |
| `allianceO` | `info.FactionInfo[GARRISON_FACTION_INDEX_ALLIANCE].Pos.Relocate(fields[8].GetFloat(), fields[9].GetFloat(), fields[10].GetFloat(), fields[11].GetFloat())` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L419) |
| `allianceAnimKitId` | `uint16 allianceAnimKitId = fields[12].GetUInt16()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L361) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `garrison_plot_finalize_info` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/garrison_plot_finalize_info) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
