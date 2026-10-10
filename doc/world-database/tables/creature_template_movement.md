# creature_template_movement

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Template-level movement capabilities.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureId` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Template extension. |
| 2 | `HoverInitiallyEnabled` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `Chase` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `Random` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `InteractionPauseTimer` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Database comment: Time (in milliseconds) during which creature will not move after interaction with player |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_movement](creature_template_movement.md).`CreatureId` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1545](../../../src/server/game/Globals/ObjectMgr.cpp#L1545)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:66](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L66)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template_movement` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template_movement) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
