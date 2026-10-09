# scenario_poi_points

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ordered coordinates composing scenario POI blobs.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CriteriaTreeID` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Idx1` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Idx2` | `int` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `X` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Y` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Z` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CriteriaTreeID`, `Idx1`, `Idx2` | BTREE |
| `questId_id` | No | `CriteriaTreeID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Scenarios/ScenarioMgr.cpp:168](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L168)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `CriteriaTreeID` | `int32 CriteriaTreeID = fields[0].GetInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L180) |
| `Idx1` | `int32 Idx1 = fields[1].GetInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L181) |
| `X` | `int32 X = fields[2].GetInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L182) |
| `Y` | `int32 Y = fields[3].GetInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L183) |
| `Z` | `int32 Z = fields[4].GetInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L184) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `scenario_poi_points` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/scenario_poi_points) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
