# disables

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed switches disabling specific content or map-processing features.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `sourceType` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `flags` | `smallint` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `params_0` | `varchar(255)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `params_1` | `varchar(255)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `comment` | `varchar(255)` | NO | `''` | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `sourceType`, `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Conditions/DisableMgr.cpp:71](../../../src/server/game/Conditions/DisableMgr.cpp#L71)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:74](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L74)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:75](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L75)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:76](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L76)
- [src/server/scripts/Commands/cs_disable.cpp:191](../../../src/server/scripts/Commands/cs_disable.cpp#L191)
- [src/server/scripts/Commands/cs_disable.cpp:290](../../../src/server/scripts/Commands/cs_disable.cpp#L290)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `sourceType` | `uint32 type = fields[0].GetUInt32()` | [loader](../../../src/server/game/Conditions/DisableMgr.cpp#L85) |
| `entry` | `uint32 entry = fields[1].GetUInt32()` | [loader](../../../src/server/game/Conditions/DisableMgr.cpp#L92) |
| `flags` | `uint16 flags = fields[2].GetUInt16()` | [loader](../../../src/server/game/Conditions/DisableMgr.cpp#L93) |
| `params_0` | `std::string params_0 = fields[3].GetString()` | [loader](../../../src/server/game/Conditions/DisableMgr.cpp#L94) |
| `params_1` | `std::string params_1 = fields[4].GetString()` | [loader](../../../src/server/game/Conditions/DisableMgr.cpp#L95) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `disables` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/disables) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
