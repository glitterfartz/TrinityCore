# skill_discovery_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Random recipe discovery chances during crafting.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Skill Discovery System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `spellId` | `int unsigned` | NO | `0` | PRI | — | Database comment: SpellId of the discoverable spell |
| 2 | `reqSpell` | `int unsigned` | NO | `0` | PRI | — | Database comment: spell requirement |
| 3 | `reqSkillValue` | `smallint unsigned` | NO | `0` | — | — | Database comment: skill points requirement |
| 4 | `chance` | `float` | NO | `0` | — | — | Database comment: chance to discover |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `spellId`, `reqSpell` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Skills/SkillDiscovery.cpp:55](../../../src/server/game/Skills/SkillDiscovery.cpp#L55)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spellId` | `uint32 spellId         = fields[0].GetUInt32()` | [loader](../../../src/server/game/Skills/SkillDiscovery.cpp#L72) |
| `reqSpell` | `int32  reqSkillOrSpell = fields[1].GetInt32()` | [loader](../../../src/server/game/Skills/SkillDiscovery.cpp#L73) |
| `reqSkillValue` | `uint32 reqSkillValue   = fields[2].GetUInt16()` | [loader](../../../src/server/game/Skills/SkillDiscovery.cpp#L74) |
| `chance` | `float  chance          = fields[3].GetFloat()` | [loader](../../../src/server/game/Skills/SkillDiscovery.cpp#L75) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `skill_discovery_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/skill_discovery_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
