# criteria_data

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Additional typed requirements for achievement criteria.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Achievment system

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `criteria_id` | `int` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `type` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `value1` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `value2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `criteria_id`, `type` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Achievements/CriteriaHandler.cpp:4878](../../../src/server/game/Achievements/CriteriaHandler.cpp#L4878)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `criteria_id` | `uint32 criteria_id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Achievements/CriteriaHandler.cpp#L4891) |
| `type` | `uint32 dataType = fields[1].GetUInt8()` | [loader](../../../src/server/game/Achievements/CriteriaHandler.cpp#L4901) |
| `value2` | `CriteriaData data(dataType, fields[2].GetUInt32(), fields[3].GetUInt32(), scriptId)` | [loader](../../../src/server/game/Achievements/CriteriaHandler.cpp#L4912) |
| `ScriptName` | `std::string_view scriptName = fields[4].GetStringView()` | [loader](../../../src/server/game/Achievements/CriteriaHandler.cpp#L4902) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `criteria_data` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/criteria_data) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
