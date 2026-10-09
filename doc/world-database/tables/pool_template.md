# pool_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spawn-pool definitions and maximum active member counts.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Database comment: Pool entry |
| 2 | `max_limit` | `int unsigned` | NO | `0` | — | — | Database comment: Max number of objects (0) is no limit |
| 3 | `description` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Description text; its runtime role depends on the owning table. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [pool_members](pool_members.md).`poolSpawnId` → [pool_template](pool_template.md).`entry`: Parent pool; member spawnId is typed.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:897](../../../src/server/game/Events/GameEventMgr.cpp#L897)
- [src/server/game/Pools/PoolMgr.cpp:419](../../../src/server/game/Pools/PoolMgr.cpp#L419)
- [src/server/game/Pools/PoolMgr.cpp:696](../../../src/server/game/Pools/PoolMgr.cpp#L696)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 pool_id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Pools/PoolMgr.cpp#L432) |
| `max_limit` | `pPoolTemplate.MaxLimit  = fields[1].GetUInt32()` | [loader](../../../src/server/game/Pools/PoolMgr.cpp#L435) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `pool_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/pool_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
