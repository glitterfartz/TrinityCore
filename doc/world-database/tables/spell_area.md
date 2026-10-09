# spell_area

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Area, quest, race, gender, and aura requirements for applying spells.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `spell` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `area` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `quest_start` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `quest_end` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `aura_spell` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `racemask` | `bigint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `gender` | `tinyint unsigned` | NO | `2` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `flags` | `tinyint unsigned` | NO | `3` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `quest_start_status` | `int` | NO | `64` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `quest_end_status` | `int` | NO | `11` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `spell`, `area`, `quest_start`, `aura_spell`, `racemask`, `gender` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:2307](../../../src/server/game/Spells/SpellMgr.cpp#L2307)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spell` | `uint32 spell = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2320) |
| `area` | `spellArea.areaId              = fields[1].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2323) |
| `quest_start` | `spellArea.questStart          = fields[2].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2324) |
| `quest_end` | `spellArea.questEnd            = fields[5].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2327) |
| `aura_spell` | `spellArea.auraSpell           = fields[6].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2328) |
| `racemask` | `spellArea.raceMask            = { fields[7].GetUInt64() }` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2329) |
| `gender` | `spellArea.gender              = Gender(fields[8].GetUInt8())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2330) |
| `flags` | `spellArea.flags               = fields[9].GetUInt8()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2331) |
| `quest_start_status` | `spellArea.questStartStatus    = fields[3].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2325) |
| `quest_end_status` | `spellArea.questEndStatus      = fields[4].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2326) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_area` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_area) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
