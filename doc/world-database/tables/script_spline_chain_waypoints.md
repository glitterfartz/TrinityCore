# script_spline_chain_waypoints

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ordered coordinates for scripted spline chains.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Record identifier; consult the complete primary key and relationships before treating it as a template ID. |
| 2 | `chainId` | `smallint unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `splineId` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `wpId` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `x` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `y` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `z` | `float` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry`, `chainId`, `splineId`, `wpId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Scripting/ScriptSystem.cpp:44](../../../src/server/game/Scripting/ScriptSystem.cpp#L44)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `script_spline_chain_waypoints` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/script_spline_chain_waypoints) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
