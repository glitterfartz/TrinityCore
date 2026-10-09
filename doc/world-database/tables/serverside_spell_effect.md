# serverside_spell_effect

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Effect definitions for server-only spells.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpellID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `EffectIndex` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `DifficultyID` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Effect` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `EffectAura` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `EffectAmplitude` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `EffectAttributes` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `EffectAuraPeriod` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `EffectBonusCoefficient` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `EffectChainAmplitude` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `EffectChainTargets` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `EffectItemType` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `EffectMechanic` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `EffectPointsPerResource` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `EffectPosFacing` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `EffectRealPointsPerLevel` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 17 | `EffectTriggerSpell` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `BonusCoefficientFromAP` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 19 | `PvpMultiplier` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 20 | `Coefficient` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 21 | `Variance` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 22 | `ResourceCoefficient` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 23 | `GroupSizeBasePointsCoefficient` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 24 | `EffectBasePoints` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 25 | `EffectMiscValue1` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 26 | `EffectMiscValue2` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 27 | `EffectRadiusIndex1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 28 | `EffectRadiusIndex2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 29 | `EffectSpellClassMask1` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 30 | `EffectSpellClassMask2` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 31 | `EffectSpellClassMask3` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 32 | `EffectSpellClassMask4` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 33 | `ImplicitTarget1` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 34 | `ImplicitTarget2` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpellID`, `EffectIndex`, `DifficultyID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:2742](../../../src/server/game/Spells/SpellMgr.cpp#L2742)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpellID` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2758) |
| `EffectIndex` | `effect.EffectIndex = fields[1].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2761) |
| `DifficultyID` | `Difficulty difficulty = Difficulty(fields[2].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2759) |
| `Effect` | `effect.Effect = fields[3].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2762) |
| `EffectAura` | `effect.EffectAura = fields[4].GetInt16()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2763) |
| `EffectAmplitude` | `effect.EffectAmplitude = fields[5].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2764) |
| `EffectAttributes` | `effect.EffectAttributes = fields[6].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2765) |
| `EffectAuraPeriod` | `effect.EffectAuraPeriod = fields[7].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2766) |
| `EffectBonusCoefficient` | `effect.EffectBonusCoefficient = fields[8].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2767) |
| `EffectChainAmplitude` | `effect.EffectChainAmplitude = fields[9].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2768) |
| `EffectChainTargets` | `effect.EffectChainTargets = fields[10].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2769) |
| `EffectItemType` | `effect.EffectItemType = fields[11].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2770) |
| `EffectMechanic` | `effect.EffectMechanic = Mechanics(fields[12].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2771) |
| `EffectPointsPerResource` | `effect.EffectPointsPerResource = fields[13].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2772) |
| `EffectPosFacing` | `effect.EffectPosFacing = fields[14].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2773) |
| `EffectRealPointsPerLevel` | `effect.EffectRealPointsPerLevel = fields[15].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2774) |
| `EffectTriggerSpell` | `effect.EffectTriggerSpell = fields[16].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2775) |
| `BonusCoefficientFromAP` | `effect.BonusCoefficientFromAP = fields[17].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2776) |
| `PvpMultiplier` | `effect.PvpMultiplier = fields[18].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2777) |
| `Coefficient` | `effect.Coefficient = fields[19].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2778) |
| `Variance` | `effect.Variance = fields[20].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2779) |
| `ResourceCoefficient` | `effect.ResourceCoefficient = fields[21].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2780) |
| `GroupSizeBasePointsCoefficient` | `effect.GroupSizeBasePointsCoefficient = fields[22].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2781) |
| `EffectBasePoints` | `effect.EffectBasePoints = fields[23].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2782) |
| `EffectMiscValue1` | `effect.EffectMiscValue[0] = fields[24].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2783) |
| `EffectMiscValue2` | `effect.EffectMiscValue[1] = fields[25].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2784) |
| `EffectRadiusIndex1` | `effect.EffectRadiusIndex[0] = fields[26].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2785) |
| `EffectRadiusIndex2` | `effect.EffectRadiusIndex[1] = fields[27].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2786) |
| `EffectSpellClassMask4` | `effect.EffectSpellClassMask = flag128(fields[28].GetInt32(), fields[29].GetInt32(), fields[30].GetInt32(), fields[31].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2787) |
| `ImplicitTarget1` | `effect.ImplicitTarget[0] = fields[32].GetInt16()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2788) |
| `ImplicitTarget2` | `effect.ImplicitTarget[1] = fields[33].GetInt16()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2789) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `serverside_spell_effect` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/serverside_spell_effect) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
