# spawn_group

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Associates typed spawn IDs with spawn-group templates.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `groupId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [spawn_group_template.groupId](spawn_group_template.md). Group definition. |
| 2 | `spawnType` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `spawnId` | `bigint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `groupId`, `spawnType`, `spawnId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [spawn_group](spawn_group.md).`groupId` → [spawn_group_template](spawn_group_template.md).`groupId`: Group definition.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2791](../../../src/server/game/Globals/ObjectMgr.cpp#L2791)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:79](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L79)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `groupId` | `uint32 groupId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2803) |
| `spawnType` | `SpawnObjectType spawnType = SpawnObjectType(fields[1].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2804) |
| `spawnId` | `ObjectGuid::LowType spawnId = fields[2].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2810) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spawn_group` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spawn_group) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
