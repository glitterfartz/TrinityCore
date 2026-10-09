# spawn_group_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spawn-group names and behavior flags.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `groupId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `groupName` | `varchar(100)` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `groupFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `groupId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [spawn_group](spawn_group.md).`groupId` → [spawn_group_template](spawn_group_template.md).`groupId`: Group definition.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2732](../../../src/server/game/Globals/ObjectMgr.cpp#L2732)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `groupId` | `uint32 groupId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2739) |
| `groupName` | `group.name = fields[1].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2742) |
| `groupFlags` | `uint32 flags = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2744) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spawn_group_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spawn_group_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
