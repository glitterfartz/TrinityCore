# creature_movement_override

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Per-spawn overrides of creature movement capabilities.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpawnId` | `bigint unsigned` | NO | `0` | PRI | — | Logical reference to [creature.guid](creature.md). Per-spawn movement settings. |
| 2 | `HoverInitiallyEnabled` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `Chase` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `Random` | `tinyint unsigned` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `InteractionPauseTimer` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Database comment: Time (in milliseconds) during which creature will not move after interaction with player |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpawnId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_movement_override](creature_movement_override.md).`SpawnId` → [creature](creature.md).`guid`: Per-spawn movement settings.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1545](../../../src/server/game/Globals/ObjectMgr.cpp#L1545)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_movement_override` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_movement_override) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
