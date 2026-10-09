# spell_group

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spells and nested groups used for aura stacking rules.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Spell System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | `0` | PRI | — | Row identity within this table; use the complete primary key when selecting or editing. |
| 2 | `spell_id` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id`, `spell_id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [spell_group_stack_rules](spell_group_stack_rules.md).`group_id` → [spell_group](spell_group.md).`id`: Stacking rule for group.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:1274](../../../src/server/game/Spells/SpellMgr.cpp#L1274)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `id` | `uint32 group_id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1287) |
| `spell_id` | `int32 spell_id = fields[1].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1293) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_group` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_group) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
