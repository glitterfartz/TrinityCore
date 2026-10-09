# spell_custom_attr

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server-specific spell attribute masks.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: SpellInfo custom attributes

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Database comment: spell id |
| 2 | `attributes` | `int unsigned` | NO | `0` | — | — | Database comment: SpellCustomAttributes |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:2986](../../../src/server/game/Spells/SpellMgr.cpp#L2986)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2997) |
| `attributes` | `uint32 attributes = fields[1].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2998) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_custom_attr` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_custom_attr) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
