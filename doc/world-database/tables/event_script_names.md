# event_script_names

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Compiled script bindings for game event identifiers.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `ScriptName` | `varchar(64)` | NO | NULL / absent; see conventions | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:5946](../../../src/server/game/Globals/ObjectMgr.cpp#L5946)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `uint32 eventId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5957) |
| `ScriptName` | `std::string_view scriptName = fields[1].GetStringView()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5958) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `event_script_names` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/event_script_names) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
