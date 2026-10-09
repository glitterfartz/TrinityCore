# quest_pool_members

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Quest membership in rotating quest pools.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `questId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Quest selected by pool.; Logical reference to [quest_template.ID](quest_template.md). Parent quest. |
| 2 | `poolId` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Logical reference to [quest_pool_template.poolId](quest_pool_template.md). Rotating quest pool. |
| 3 | `poolIndex` | `tinyint unsigned` | NO | NULL / absent; see conventions | — | — | Database comment: Multiple quests with the same index will always spawn together! |
| 4 | `description` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Description text; its runtime role depends on the owning table. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `questId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_pool_members](quest_pool_members.md).`poolId` → [quest_pool_template](quest_pool_template.md).`poolId`: Rotating quest pool.
- [quest_pool_members](quest_pool_members.md).`questId` → [quest_template](quest_template.md).`ID`: Quest selected by pool.
- [quest_pool_members](quest_pool_members.md).`questId` → [quest_template](quest_template.md).`ID`: Parent quest.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Pools/QuestPools.cpp:80](../../../src/server/game/Pools/QuestPools.cpp#L80)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_pool_members` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_pool_members) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
