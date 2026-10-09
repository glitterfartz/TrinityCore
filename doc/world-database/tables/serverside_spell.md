# serverside_spell

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server-only spell definitions not supplied by client spell data.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `DifficultyID` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `CategoryId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Dispel` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Mechanic` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Attributes` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `AttributesEx` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `AttributesEx2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `AttributesEx3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `AttributesEx4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `AttributesEx5` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `AttributesEx6` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `AttributesEx7` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `AttributesEx8` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `AttributesEx9` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `AttributesEx10` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 17 | `AttributesEx11` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `AttributesEx12` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 19 | `AttributesEx13` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 20 | `AttributesEx14` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 21 | `AttributesEx15` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 22 | `AttributesEx16` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 23 | `Stances` | `bigint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 24 | `StancesNot` | `bigint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 25 | `Targets` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 26 | `TargetCreatureType` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 27 | `RequiresSpellFocus` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 28 | `FacingCasterFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 29 | `CasterAuraState` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 30 | `TargetAuraState` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 31 | `ExcludeCasterAuraState` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 32 | `ExcludeTargetAuraState` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 33 | `CasterAuraSpell` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 34 | `TargetAuraSpell` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 35 | `ExcludeCasterAuraSpell` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 36 | `ExcludeTargetAuraSpell` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 37 | `CasterAuraType` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 38 | `TargetAuraType` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 39 | `ExcludeCasterAuraType` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 40 | `ExcludeTargetAuraType` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 41 | `CastingTimeIndex` | `int unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 42 | `RecoveryTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 43 | `CategoryRecoveryTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 44 | `StartRecoveryCategory` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 45 | `StartRecoveryTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 46 | `InterruptFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 47 | `AuraInterruptFlags1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 48 | `AuraInterruptFlags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 49 | `ChannelInterruptFlags1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 50 | `ChannelInterruptFlags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 51 | `ProcFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 52 | `ProcFlags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 53 | `ProcChance` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 54 | `ProcCharges` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 55 | `ProcCooldown` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 56 | `ProcBasePPM` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 57 | `MaxLevel` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 58 | `BaseLevel` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 59 | `SpellLevel` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 60 | `DurationIndex` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 61 | `RangeIndex` | `int unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 62 | `Speed` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 63 | `LaunchDelay` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 64 | `StackAmount` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 65 | `EquippedItemClass` | `int` | NO | `-1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 66 | `EquippedItemSubClassMask` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 67 | `EquippedItemInventoryTypeMask` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 68 | `ContentTuningId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 69 | `SpellName` | `varchar(100)` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 70 | `ConeAngle` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 71 | `ConeWidth` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 72 | `MaxTargetLevel` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 73 | `MaxAffectedTargets` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 74 | `SpellFamilyName` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 75 | `SpellFamilyFlags1` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 76 | `SpellFamilyFlags2` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 77 | `SpellFamilyFlags3` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 78 | `SpellFamilyFlags4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 79 | `DmgClass` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 80 | `PreventionType` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 81 | `AreaGroupId` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 82 | `SchoolMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 83 | `ChargeCategoryId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id`, `DifficultyID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:2859](../../../src/server/game/Spells/SpellMgr.cpp#L2859)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2885) |
| `DifficultyID` | `Difficulty difficulty = Difficulty(fields[1].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2886) |
| `CategoryId` | `spellInfo.CategoryId = fields[2].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2897) |
| `Dispel` | `spellInfo.Dispel = fields[3].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2898) |
| `Mechanic` | `spellInfo.Mechanic = fields[4].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2899) |
| `Attributes` | `spellInfo.Attributes = fields[5].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2900) |
| `AttributesEx` | `spellInfo.AttributesEx = fields[6].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2901) |
| `AttributesEx2` | `spellInfo.AttributesEx2 = fields[7].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2902) |
| `AttributesEx3` | `spellInfo.AttributesEx3 = fields[8].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2903) |
| `AttributesEx4` | `spellInfo.AttributesEx4 = fields[9].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2904) |
| `AttributesEx5` | `spellInfo.AttributesEx5 = fields[10].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2905) |
| `AttributesEx6` | `spellInfo.AttributesEx6 = fields[11].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2906) |
| `AttributesEx7` | `spellInfo.AttributesEx7 = fields[12].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2907) |
| `AttributesEx8` | `spellInfo.AttributesEx8 = fields[13].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2908) |
| `AttributesEx9` | `spellInfo.AttributesEx9 = fields[14].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2909) |
| `AttributesEx10` | `spellInfo.AttributesEx10 = fields[15].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2910) |
| `AttributesEx11` | `spellInfo.AttributesEx11 = fields[16].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2911) |
| `AttributesEx12` | `spellInfo.AttributesEx12 = fields[17].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2912) |
| `AttributesEx13` | `spellInfo.AttributesEx13 = fields[18].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2913) |
| `AttributesEx14` | `spellInfo.AttributesEx14 = fields[19].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2914) |
| `AttributesEx15` | `spellInfo.AttributesEx15 = fields[20].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2915) |
| `AttributesEx16` | `spellInfo.AttributesEx16 = fields[21].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2916) |
| `Stances` | `spellInfo.Stances = fields[22].GetUInt64()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2917) |
| `StancesNot` | `spellInfo.StancesNot = fields[23].GetUInt64()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2918) |
| `Targets` | `spellInfo.Targets = fields[24].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2919) |
| `TargetCreatureType` | `spellInfo.TargetCreatureType = fields[25].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2920) |
| `RequiresSpellFocus` | `spellInfo.RequiresSpellFocus = fields[26].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2921) |
| `FacingCasterFlags` | `spellInfo.FacingCasterFlags = fields[27].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2922) |
| `CasterAuraState` | `spellInfo.CasterAuraState = fields[28].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2923) |
| `TargetAuraState` | `spellInfo.TargetAuraState = fields[29].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2924) |
| `ExcludeCasterAuraState` | `spellInfo.ExcludeCasterAuraState = fields[30].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2925) |
| `ExcludeTargetAuraState` | `spellInfo.ExcludeTargetAuraState = fields[31].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2926) |
| `CasterAuraSpell` | `spellInfo.CasterAuraSpell = fields[32].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2927) |
| `TargetAuraSpell` | `spellInfo.TargetAuraSpell = fields[33].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2928) |
| `ExcludeCasterAuraSpell` | `spellInfo.ExcludeCasterAuraSpell = fields[34].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2929) |
| `ExcludeTargetAuraSpell` | `spellInfo.ExcludeTargetAuraSpell = fields[35].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2930) |
| `CasterAuraType` | `spellInfo.CasterAuraType = AuraType(fields[36].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2931) |
| `TargetAuraType` | `spellInfo.TargetAuraType = AuraType(fields[37].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2932) |
| `ExcludeCasterAuraType` | `spellInfo.ExcludeCasterAuraType = AuraType(fields[38].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2933) |
| `ExcludeTargetAuraType` | `spellInfo.ExcludeTargetAuraType = AuraType(fields[39].GetInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2934) |
| `CastingTimeIndex` | `spellInfo.CastTimeEntry = sSpellCastTimesStore.LookupEntry(fields[40].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2935) |
| `RecoveryTime` | `spellInfo.RecoveryTime = fields[41].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2936) |
| `CategoryRecoveryTime` | `spellInfo.CategoryRecoveryTime = fields[42].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2937) |
| `StartRecoveryCategory` | `spellInfo.StartRecoveryCategory = fields[43].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2938) |
| `StartRecoveryTime` | `spellInfo.StartRecoveryTime = fields[44].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2939) |
| `InterruptFlags` | `spellInfo.InterruptFlags = SpellInterruptFlags(fields[45].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2940) |
| `AuraInterruptFlags1` | `spellInfo.AuraInterruptFlags = SpellAuraInterruptFlags(fields[46].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2941) |
| `AuraInterruptFlags2` | `spellInfo.AuraInterruptFlags2 = SpellAuraInterruptFlags2(fields[47].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2942) |
| `ChannelInterruptFlags1` | `spellInfo.ChannelInterruptFlags = SpellAuraInterruptFlags(fields[48].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2943) |
| `ChannelInterruptFlags2` | `spellInfo.ChannelInterruptFlags2 = SpellAuraInterruptFlags2(fields[49].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2944) |
| `ProcFlags` | `spellInfo.ProcFlags[0] = fields[50].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2945) |
| `ProcFlags2` | `spellInfo.ProcFlags[1] = fields[51].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2946) |
| `ProcChance` | `spellInfo.ProcChance = fields[52].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2947) |
| `ProcCharges` | `spellInfo.ProcCharges = fields[53].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2948) |
| `ProcCooldown` | `spellInfo.ProcCooldown = fields[54].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2949) |
| `ProcBasePPM` | `spellInfo.ProcBasePPM = fields[55].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2950) |
| `MaxLevel` | `spellInfo.MaxLevel = fields[56].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2951) |
| `BaseLevel` | `spellInfo.BaseLevel = fields[57].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2952) |
| `SpellLevel` | `spellInfo.SpellLevel = fields[58].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2953) |
| `DurationIndex` | `spellInfo.DurationEntry = sSpellDurationStore.LookupEntry(fields[59].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2954) |
| `RangeIndex` | `spellInfo.RangeEntry = sSpellRangeStore.LookupEntry(fields[60].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2955) |
| `Speed` | `spellInfo.Speed = fields[61].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2956) |
| `LaunchDelay` | `spellInfo.LaunchDelay = fields[62].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2957) |
| `StackAmount` | `spellInfo.StackAmount = fields[63].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2958) |
| `EquippedItemClass` | `spellInfo.EquippedItemClass = fields[64].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2959) |
| `EquippedItemSubClassMask` | `spellInfo.EquippedItemSubClassMask = fields[65].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2960) |
| `EquippedItemInventoryTypeMask` | `spellInfo.EquippedItemInventoryTypeMask = fields[66].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2961) |
| `ContentTuningId` | `spellInfo.ContentTuningId = fields[67].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2962) |
| `SpellName` | `mServersideSpellNames.emplace_back(spellId, fields[68].GetStringView())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2894) |
| `ConeAngle` | `spellInfo.ConeAngle = fields[69].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2963) |
| `ConeWidth` | `spellInfo.Width = fields[70].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2964) |
| `MaxTargetLevel` | `spellInfo.MaxTargetLevel = fields[71].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2965) |
| `MaxAffectedTargets` | `spellInfo.MaxAffectedTargets = fields[72].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2966) |
| `SpellFamilyName` | `spellInfo.SpellFamilyName = fields[73].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2967) |
| `SpellFamilyFlags4` | `spellInfo.SpellFamilyFlags = flag128(fields[74].GetUInt32(), fields[75].GetUInt32(), fields[76].GetUInt32(), fields[77].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2968) |
| `DmgClass` | `spellInfo.DmgClass = fields[78].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2969) |
| `PreventionType` | `spellInfo.PreventionType = fields[79].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2970) |
| `AreaGroupId` | `spellInfo.RequiredAreasID = fields[80].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2971) |
| `SchoolMask` | `spellInfo.SchoolMask = fields[81].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2972) |
| `ChargeCategoryId` | `spellInfo.ChargeCategoryId = fields[82].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L2973) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `serverside_spell` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/serverside_spell) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
