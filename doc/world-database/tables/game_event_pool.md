# game_event_pool

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spawn pools controlled by world events.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint` | NO | NULL / absent; see conventions | — | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `pool_entry` | `int unsigned` | NO | `0` | PRI | — | Database comment: Id of the pool |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `pool_entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_pool](game_event_pool.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:897](../../../src/server/game/Events/GameEventMgr.cpp#L897)
- [src/server/game/Pools/PoolMgr.cpp:696](../../../src/server/game/Pools/PoolMgr.cpp#L696)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_pool` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_pool) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
