# skill_perfect_item_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Perfect-result crafting substitutions and probabilities.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Crafting Perfection System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `spellId` | `int unsigned` | NO | `0` | PRI | — | Database comment: SpellId of the item creation spell |
| 2 | `requiredSpecialization` | `int unsigned` | NO | `0` | — | — | Database comment: Specialization spell id |
| 3 | `perfectCreateChance` | `float` | NO | `0` | — | — | Database comment: chance to create the perfect item instead |
| 4 | `perfectItemType` | `int unsigned` | NO | `0` | — | — | Database comment: perfect item type to create instead |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `spellId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Skills/SkillExtraItems.cpp:58](../../../src/server/game/Skills/SkillExtraItems.cpp#L58)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spellId` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Skills/SkillExtraItems.cpp#L72) |
| `requiredSpecialization` | `uint32 requiredSpecialization = fields[1].GetUInt32()` | [loader](../../../src/server/game/Skills/SkillExtraItems.cpp#L80) |
| `perfectCreateChance` | `float perfectCreateChance = fields[2].GetFloat()` | [loader](../../../src/server/game/Skills/SkillExtraItems.cpp#L87) |
| `perfectItemType` | `uint32 perfectItemType = fields[3].GetUInt32()` | [loader](../../../src/server/game/Skills/SkillExtraItems.cpp#L94) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `skill_perfect_item_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/skill_perfect_item_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
