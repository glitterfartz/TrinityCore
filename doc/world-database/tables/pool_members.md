# pool_members

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed creature, gameobject, or child-pool membership and selection chances.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `type` | `smallint unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 2 | `spawnId` | `bigint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `poolSpawnId` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Logical reference to [pool_template.entry](pool_template.md). Parent pool; member spawnId is typed. |
| 4 | `chance` | `float` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `description` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Description text; its runtime role depends on the owning table. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `type`, `spawnId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [pool_members](pool_members.md).`poolSpawnId` → [pool_template](pool_template.md).`entry`: Parent pool; member spawnId is typed.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2125](../../../src/server/game/Globals/ObjectMgr.cpp#L2125)
- [src/server/game/Globals/ObjectMgr.cpp:2485](../../../src/server/game/Globals/ObjectMgr.cpp#L2485)
- [src/server/game/Pools/PoolMgr.cpp:452](../../../src/server/game/Pools/PoolMgr.cpp#L452)
- [src/server/game/Pools/PoolMgr.cpp:518](../../../src/server/game/Pools/PoolMgr.cpp#L518)
- [src/server/game/Pools/PoolMgr.cpp:587](../../../src/server/game/Pools/PoolMgr.cpp#L587)
- [src/server/game/Pools/PoolMgr.cpp:696](../../../src/server/game/Pools/PoolMgr.cpp#L696)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spawnId` | `uint64 guid = fields[0].GetUInt64()` | [loader](../../../src/server/game/Pools/PoolMgr.cpp#L465) |
| `poolSpawnId` | `uint32 pool_id = fields[1].GetUInt32()` | [loader](../../../src/server/game/Pools/PoolMgr.cpp#L466) |
| `chance` | `float chance   = fields[2].GetFloat()` | [loader](../../../src/server/game/Pools/PoolMgr.cpp#L467) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `pool_members` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/pool_members) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
