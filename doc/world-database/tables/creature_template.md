# creature_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Base NPC definitions shared by creature spawns and summoned creatures.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `KillCredit1` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `KillCredit2` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `name` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `femaleName` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `subname` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `TitleAlt` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `IconName` | `varchar(64)` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `RequiredExpansion` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `VignetteID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `faction` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `npcflag` | `bigint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `speed_walk` | `float` | NO | `1` | — | — | Database comment: Result of 2.5/2.5, most common value |
| 14 | `speed_run` | `float` | NO | `1.14286` | — | — | Database comment: Result of 8.0/7.0, most common value |
| 15 | `scale` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `Classification` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 17 | `dmgschool` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `BaseAttackTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 19 | `RangeAttackTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 20 | `BaseVariance` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 21 | `RangeVariance` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 22 | `unit_class` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 23 | `unit_flags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 24 | `unit_flags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 25 | `unit_flags3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 26 | `family` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 27 | `trainer_class` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 28 | `type` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 29 | `VehicleId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 30 | `AIName` | `varchar(64)` | NO | `''` | — | — | Registered AI implementation name. SmartAI requires the corresponding SmartAI source rows. |
| 31 | `MovementType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 32 | `ExperienceModifier` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 33 | `RacialLeader` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 34 | `movementId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 35 | `WidgetSetID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 36 | `WidgetSetUnitConditionID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 37 | `RegenHealth` | `tinyint unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 38 | `CreatureImmunitiesId` | `int` | NO | `0` | — | — | Logical reference to [creature_immunities.ID](creature_immunities.md). Reusable immunity definition. |
| 39 | `flags_extra` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 40 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 41 | `StringId` | `varchar(64)` | YES | NULL / absent; see conventions | — | — | Author-defined string identifier used by object lookup and string-ID conditions. |
| 42 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature](creature.md).`id` → [creature_template](creature_template.md).`entry`: Template identity shared by NPC spawns.
- [creature_template](creature_template.md).`CreatureImmunitiesId` → [creature_immunities](creature_immunities.md).`ID`: Reusable immunity definition.
- [creature_template_model](creature_template_model.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_template_addon](creature_template_addon.md).`entry` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_text](creature_text.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_template_difficulty](creature_template_difficulty.md).`Entry` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_template_gossip](creature_template_gossip.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_template_sparring](creature_template_sparring.md).`Entry` → [creature_template](creature_template.md).`entry`: Template extension.
- [npc_vendor](npc_vendor.md).`entry` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_template_movement](creature_template_movement.md).`CreatureId` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_questender](creature_questender.md).`id` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_template_locale](creature_template_locale.md).`entry` → [creature_template](creature_template.md).`entry`: Translation parent identity; include all identity components plus locale.
- [creature_template_spell](creature_template_spell.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.
- [creature_queststarter](creature_queststarter.md).`id` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_template_resistance](creature_template_resistance.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:370](../../../src/server/game/Globals/ObjectMgr.cpp#L370)
- [src/server/game/Globals/ObjectMgr.cpp:401](../../../src/server/game/Globals/ObjectMgr.cpp#L401)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:41](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L41)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:42](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L42)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:66](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L66)
- [src/server/scripts/Commands/cs_reload.cpp:434](../../../src/server/scripts/Commands/cs_reload.cpp#L434)
- [src/server/scripts/Commands/cs_tele.cpp:368](../../../src/server/scripts/Commands/cs_tele.cpp#L368)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L403) |
| `name` | `creatureTemplate.Name                   = fields[3].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L411) |
| `femaleName` | `creatureTemplate.FemaleName             = fields[4].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L412) |
| `subname` | `creatureTemplate.SubName                = fields[5].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L413) |
| `TitleAlt` | `creatureTemplate.TitleAlt               = fields[6].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L414) |
| `IconName` | `creatureTemplate.IconName               = fields[7].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L415) |
| `RequiredExpansion` | `creatureTemplate.RequiredExpansion      = fields[8].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L416) |
| `VignetteID` | `creatureTemplate.VignetteID             = fields[9].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L417) |
| `faction` | `creatureTemplate.faction                = fields[10].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L418) |
| `npcflag` | `creatureTemplate.npcflag                = fields[11].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L419) |
| `speed_walk` | `creatureTemplate.speed_walk             = fields[12].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L420) |
| `speed_run` | `creatureTemplate.speed_run              = fields[13].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L421) |
| `scale` | `creatureTemplate.scale                  = fields[14].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L422) |
| `Classification` | `creatureTemplate.Classification         = CreatureClassifications(fields[15].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L423) |
| `dmgschool` | `creatureTemplate.dmgschool              = uint32(fields[16].GetInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L424) |
| `BaseAttackTime` | `creatureTemplate.BaseAttackTime         = fields[17].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L425) |
| `RangeAttackTime` | `creatureTemplate.RangeAttackTime        = fields[18].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L426) |
| `BaseVariance` | `creatureTemplate.BaseVariance           = fields[19].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L427) |
| `RangeVariance` | `creatureTemplate.RangeVariance          = fields[20].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L428) |
| `unit_class` | `creatureTemplate.unit_class             = uint32(fields[21].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L429) |
| `unit_flags` | `creatureTemplate.unit_flags             = fields[22].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L430) |
| `unit_flags2` | `creatureTemplate.unit_flags2            = fields[23].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L431) |
| `unit_flags3` | `creatureTemplate.unit_flags3            = fields[24].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L432) |
| `family` | `creatureTemplate.family                 = CreatureFamily(fields[25].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L433) |
| `trainer_class` | `creatureTemplate.trainer_class          = uint32(fields[26].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L434) |
| `type` | `creatureTemplate.type                   = uint32(fields[27].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L435) |
| `VehicleId` | `creatureTemplate.VehicleId              = fields[28].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L443) |
| `AIName` | `creatureTemplate.AIName                 = fields[29].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L444) |
| `MovementType` | `creatureTemplate.MovementType           = uint32(fields[30].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L445) |
| `ExperienceModifier` | `creatureTemplate.ModExperience          = fields[35].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L459) |
| `RacialLeader` | `creatureTemplate.RacialLeader           = fields[36].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L460) |
| `movementId` | `creatureTemplate.movementId             = fields[37].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L461) |
| `WidgetSetID` | `creatureTemplate.WidgetSetID            = fields[38].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L462) |
| `WidgetSetUnitConditionID` | `creatureTemplate.WidgetSetUnitConditionID = fields[39].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L463) |
| `RegenHealth` | `creatureTemplate.RegenHealth            = fields[40].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L464) |
| `CreatureImmunitiesId` | `creatureTemplate.CreatureImmunitiesId   = fields[41].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L465) |
| `flags_extra` | `creatureTemplate.flags_extra            = fields[42].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L466) |
| `ScriptName` | `creatureTemplate.ScriptID               = GetScriptId(fields[43].GetStringView())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L467) |
| `StringId` | `creatureTemplate.StringId               = fields[44].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L468) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
