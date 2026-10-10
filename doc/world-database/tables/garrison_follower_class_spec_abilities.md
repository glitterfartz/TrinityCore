# garrison_follower_class_spec_abilities

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ability choices for garrison follower class specializations.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `classSpecId` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `abilityId` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `classSpecId`, `abilityId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Garrison/GarrisonMgr.cpp:429](../../../src/server/game/Garrison/GarrisonMgr.cpp#L429)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `classSpecId` | `uint32 classSpecId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L441) |
| `abilityId` | `uint32 abilityId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Garrison/GarrisonMgr.cpp#L442) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `garrison_follower_class_spec_abilities` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/garrison_follower_class_spec_abilities) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
