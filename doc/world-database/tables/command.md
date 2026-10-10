# command

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Database overrides for chat-command help text. This table contains name and help; command permissions are not stored here.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Chat System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `name` | `varchar(50)` | NO | `''` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `help` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `name` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Chat/ChatCommands/ChatCommand.cpp:92](../../../src/server/game/Chat/ChatCommands/ChatCommand.cpp#L92)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:65](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L65)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `name` | `std::string_view const name = fields[0].GetStringView()` | [loader](../../../src/server/game/Chat/ChatCommands/ChatCommand.cpp#L97) |
| `help` | `std::string_view const help = fields[1].GetStringView()` | [loader](../../../src/server/game/Chat/ChatCommands/ChatCommand.cpp#L98) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `command` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/command) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
