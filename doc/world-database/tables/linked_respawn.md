# linked_respawn

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed dependencies between creature and gameobject respawn schedules.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature Respawn Link System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `linkedGuid` | `bigint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `linkType` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid`, `linkType` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1770](../../../src/server/game/Globals/ObjectMgr.cpp#L1770)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:26](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L26)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:27](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L27)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `guid` | `ObjectGuid::LowType guidLow = fields[0].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1782) |
| `linkedGuid` | `ObjectGuid::LowType linkedGuidLow = fields[1].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1783) |
| `linkType` | `uint8 linkType = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1784) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `linked_respawn` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/linked_respawn) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
