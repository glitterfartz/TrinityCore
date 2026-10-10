# creature_template_difficulty

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Difficulty-specific creature tuning, loot references, and static flags.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Template extension. |
| 2 | `DifficultyID` | `int` | NO | `0` | PRI | — | Client difficulty ID selecting this template extension. |
| 3 | `LevelScalingDeltaMin` | `smallint` | NO | `0` | — | — | Minimum level-scaling delta loaded into DeltaLevelMin. |
| 4 | `LevelScalingDeltaMax` | `smallint` | NO | `0` | — | — | Maximum level-scaling delta loaded into DeltaLevelMax. |
| 5 | `ContentTuningID` | `int` | NO | `0` | — | — | External content-tuning record used for level/scaling behavior. |
| 6 | `HealthScalingExpansion` | `int` | NO | `0` | — | — | Expansion selector for health scaling; the loader validates and substitutes invalid values. |
| 7 | `HealthModifier` | `float` | NO | `1` | — | — | Creature health scaling multiplier. |
| 8 | `ManaModifier` | `float` | NO | `1` | — | — | Creature mana scaling multiplier. |
| 9 | `ArmorModifier` | `float` | NO | `1` | — | — | Creature armor scaling multiplier. |
| 10 | `DamageModifier` | `float` | NO | `1` | — | — | Damage scaling multiplier; the loader also applies classification scaling. |
| 11 | `CreatureDifficultyID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `TypeFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `TypeFlags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `TypeFlags3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `LootID` | `int unsigned` | NO | `0` | — | — | Logical reference to [creature_loot_template.Entry](creature_loot_template.md). Loot entry may differ from creature entry. |
| 16 | `PickPocketLootID` | `int unsigned` | NO | `0` | — | — | Logical reference to [pickpocketing_loot_template.Entry](pickpocketing_loot_template.md). Pickpocket loot entry. |
| 17 | `SkinLootID` | `int unsigned` | NO | `0` | — | — | Logical reference to [skinning_loot_template.Entry](skinning_loot_template.md). Skinning loot entry. |
| 18 | `GoldMin` | `int unsigned` | NO | `0` | — | — | Minimum money drop; use copper units and keep GoldMax at least GoldMin. |
| 19 | `GoldMax` | `int unsigned` | NO | `0` | — | — | Maximum money drop; the loader repairs values below GoldMin. |
| 20 | `StaticFlags1` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 1. See [creature static enums](../reference/spawn-enums.md). |
| 21 | `StaticFlags2` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 2. See [creature static enums](../reference/spawn-enums.md). |
| 22 | `StaticFlags3` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 3. See [creature static enums](../reference/spawn-enums.md). |
| 23 | `StaticFlags4` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 4. See [creature static enums](../reference/spawn-enums.md). |
| 24 | `StaticFlags5` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 5. See [creature static enums](../reference/spawn-enums.md). |
| 25 | `StaticFlags6` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 6. See [creature static enums](../reference/spawn-enums.md). |
| 26 | `StaticFlags7` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 7. See [creature static enums](../reference/spawn-enums.md). |
| 27 | `StaticFlags8` | `int unsigned` | NO | `0` | — | — | Creature static behavior mask for flag set 8. See [creature static enums](../reference/spawn-enums.md). |
| 28 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Entry`, `DifficultyID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_difficulty](creature_template_difficulty.md).`LootID` → [creature_loot_template](creature_loot_template.md).`Entry`: Loot entry may differ from creature entry.
- [creature_template_difficulty](creature_template_difficulty.md).`PickPocketLootID` → [pickpocketing_loot_template](pickpocketing_loot_template.md).`Entry`: Pickpocket loot entry.
- [creature_template_difficulty](creature_template_difficulty.md).`SkinLootID` → [skinning_loot_template](skinning_loot_template.md).`Entry`: Skinning loot entry.
- [creature_template_difficulty](creature_template_difficulty.md).`Entry` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:923](../../../src/server/game/Globals/ObjectMgr.cpp#L923)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L943) |
| `DifficultyID` | `Difficulty difficulty = Difficulty(fields[1].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L944) |
| `LevelScalingDeltaMin` | `creatureDifficulty.DeltaLevelMin          = fields[2].GetInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L954) |
| `LevelScalingDeltaMax` | `creatureDifficulty.DeltaLevelMax          = fields[3].GetInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L955) |
| `ContentTuningID` | `creatureDifficulty.ContentTuningID        = fields[4].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L956) |
| `HealthScalingExpansion` | `creatureDifficulty.HealthScalingExpansion = fields[5].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L957) |
| `HealthModifier` | `creatureDifficulty.HealthModifier         = fields[6].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L958) |
| `ManaModifier` | `creatureDifficulty.ManaModifier           = fields[7].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L959) |
| `ArmorModifier` | `creatureDifficulty.ArmorModifier          = fields[8].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L960) |
| `DamageModifier` | `creatureDifficulty.DamageModifier         = fields[9].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L961) |
| `CreatureDifficultyID` | `creatureDifficulty.CreatureDifficultyID   = fields[10].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L962) |
| `TypeFlags` | `creatureDifficulty.TypeFlags              = fields[11].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L963) |
| `TypeFlags2` | `creatureDifficulty.TypeFlags2             = fields[12].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L964) |
| `TypeFlags3` | `creatureDifficulty.TypeFlags3             = fields[13].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L965) |
| `LootID` | `creatureDifficulty.LootID                 = fields[14].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L966) |
| `PickPocketLootID` | `creatureDifficulty.PickPocketLootID       = fields[15].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L967) |
| `SkinLootID` | `creatureDifficulty.SkinLootID             = fields[16].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L968) |
| `GoldMin` | `creatureDifficulty.GoldMin                = fields[17].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L969) |
| `GoldMax` | `creatureDifficulty.GoldMax                = fields[18].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L970) |
| `StaticFlags8` | `CreatureStaticFlags6(fields[24].GetUInt32()), CreatureStaticFlags7(fields[25].GetUInt32()),  CreatureStaticFlags8(fields[26].GetUInt32()))` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L973) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template_difficulty` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template_difficulty) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
