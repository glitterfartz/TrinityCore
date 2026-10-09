# pet_name_generation

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Name fragments used to generate pet names.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Row identity within this table; use the complete primary key when selecting or editing. |
| 2 | `word` | `text` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `entry` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `half` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:7970](../../../src/server/game/Globals/ObjectMgr.cpp#L7970)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `word` | `std::string word = fields[0].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7983) |
| `entry` | `uint32 entry     = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7984) |
| `half` | `bool   half      = fields[2].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7985) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `pet_name_generation` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/pet_name_generation) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
