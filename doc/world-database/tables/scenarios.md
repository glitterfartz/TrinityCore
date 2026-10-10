# scenarios

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Map/difficulty scenario assignments.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `map` | `int unsigned` | NO | `0` | PRI | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 2 | `difficulty` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `scenario_A` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `scenario_H` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `map`, `difficulty` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Scenarios/ScenarioMgr.cpp:77](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L77)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `map` | `uint32 mapId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L89) |
| `difficulty` | `Difficulty difficulty = Difficulty(fields[1].GetInt32())` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L90) |
| `scenario_A` | `uint32 scenarioAllianceId = fields[2].GetUInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L92) |
| `scenario_H` | `uint32 scenarioHordeId = fields[3].GetUInt32()` | [loader](../../../src/server/game/Scenarios/ScenarioMgr.cpp#L99) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `scenarios` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/scenarios) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
