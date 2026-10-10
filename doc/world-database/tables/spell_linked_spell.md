# spell_linked_spell

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed cast/hit/aura links between spells, including signed removal semantics.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Spell System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `spell_trigger` | `int` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `spell_effect` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `type` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `comment` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `trigger_effect_type` | Yes | `spell_trigger`, `spell_effect`, `type` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:2081](../../../src/server/game/Spells/SpellMgr.cpp#L2081)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spell_trigger` | `int32 trigger = fields[0].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2093) |
| `spell_effect` | `int32 effect = fields[1].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2094) |
| `type` | `SpellLinkedType type = SpellLinkedType(fields[2].GetUInt8())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2095) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_linked_spell` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_linked_spell) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
