# quest_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Quest identity, presentation, reward, race eligibility, and flag data.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Quest System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `QuestType` | `tinyint unsigned` | NO | `2` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `QuestPackageID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `ContentTuningID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `QuestSortID` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `QuestInfoID` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `SuggestedGroupNum` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `RewardNextQuest` | `int unsigned` | NO | `0` | — | — | Quest presented after rewarding this quest; does not by itself encode every prerequisite. |
| 9 | `RewardXPDifficulty` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `RewardXPMultiplier` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `RewardMoneyDifficulty` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `RewardMoneyMultiplier` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `RewardBonusMoney` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `RewardDisplaySpell1` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 15 | `RewardDisplaySpell2` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 16 | `RewardDisplaySpell3` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 17 | `RewardSpell` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `RewardHonor` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 19 | `RewardKillHonor` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 20 | `StartItem` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 21 | `RewardArtifactXPDifficulty` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 22 | `RewardArtifactXPMultiplier` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 23 | `RewardArtifactCategoryID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 24 | `Flags` | `int unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 25 | `FlagsEx` | `int unsigned` | NO | `0` | — | — | Extended owning-subsystem flags. |
| 26 | `FlagsEx2` | `int unsigned` | NO | `0` | — | — | Second extended owning-subsystem flag set. |
| 27 | `FlagsEx3` | `int unsigned` | NO | `0` | — | — | Third extended owning-subsystem flag set. |
| 28 | `RewardItem1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 29 | `RewardAmount1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 30 | `RewardItem2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 31 | `RewardAmount2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 32 | `RewardItem3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 33 | `RewardAmount3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 34 | `RewardItem4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 35 | `RewardAmount4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 36 | `ItemDrop1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 37 | `ItemDropQuantity1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 38 | `ItemDrop2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 39 | `ItemDropQuantity2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 40 | `ItemDrop3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 41 | `ItemDropQuantity3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 42 | `ItemDrop4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 43 | `ItemDropQuantity4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 44 | `RewardChoiceItemID1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 45 | `RewardChoiceItemQuantity1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 46 | `RewardChoiceItemDisplayID1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 47 | `RewardChoiceItemID2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 48 | `RewardChoiceItemQuantity2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 49 | `RewardChoiceItemDisplayID2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 50 | `RewardChoiceItemID3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 51 | `RewardChoiceItemQuantity3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 52 | `RewardChoiceItemDisplayID3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 53 | `RewardChoiceItemID4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 54 | `RewardChoiceItemQuantity4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 55 | `RewardChoiceItemDisplayID4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 56 | `RewardChoiceItemID5` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 57 | `RewardChoiceItemQuantity5` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 58 | `RewardChoiceItemDisplayID5` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 59 | `RewardChoiceItemID6` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 60 | `RewardChoiceItemQuantity6` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 61 | `RewardChoiceItemDisplayID6` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 62 | `POIContinent` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 63 | `POIx` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 64 | `POIy` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 65 | `POIPriority` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 66 | `RewardTitle` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 67 | `RewardArenaPoints` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 68 | `RewardSkillLineID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 69 | `RewardNumSkillUps` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 70 | `PortraitGiver` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 71 | `PortraitGiverMount` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 72 | `PortraitGiverModelSceneID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 73 | `PortraitTurnIn` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 74 | `RewardFactionID1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 75 | `RewardFactionValue1` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 76 | `RewardFactionOverride1` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 77 | `RewardFactionCapIn1` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 78 | `RewardFactionID2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 79 | `RewardFactionValue2` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 80 | `RewardFactionOverride2` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 81 | `RewardFactionCapIn2` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 82 | `RewardFactionID3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 83 | `RewardFactionValue3` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 84 | `RewardFactionOverride3` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 85 | `RewardFactionCapIn3` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 86 | `RewardFactionID4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 87 | `RewardFactionValue4` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 88 | `RewardFactionOverride4` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 89 | `RewardFactionCapIn4` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 90 | `RewardFactionID5` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 91 | `RewardFactionValue5` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 92 | `RewardFactionOverride5` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 93 | `RewardFactionCapIn5` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 94 | `RewardFactionFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 95 | `RewardCurrencyID1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 96 | `RewardCurrencyQty1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 97 | `RewardCurrencyID2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 98 | `RewardCurrencyQty2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 99 | `RewardCurrencyID3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 100 | `RewardCurrencyQty3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 101 | `RewardCurrencyID4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 102 | `RewardCurrencyQty4` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 103 | `AcceptedSoundKitID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 104 | `CompleteSoundKitID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 105 | `AreaGroupID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 106 | `TimeAllowed` | `bigint` | NO | `0` | — | — | Quest time limit; inspect QuestDef and Quest.cpp for conversion to timers. |
| 107 | `AllowableRaces` | `bigint unsigned` | YES | `0` | — | — | Race eligibility mask; modern race masks may require wider-than-32-bit arithmetic. |
| 108 | `Expansion` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 109 | `ManagedWorldStateID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 110 | `QuestSessionBonus` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 111 | `LogTitle` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 112 | `LogDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 113 | `QuestDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 114 | `AreaDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 115 | `PortraitGiverText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 116 | `PortraitGiverName` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 117 | `PortraitTurnInText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 118 | `PortraitTurnInName` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 119 | `QuestCompletionLog` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 120 | `ResetByScheduler` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 121 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |
| 122 | `RewardFavor` | `int` | NO | `0` | — | — | Reward favor value read by the current quest loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_objectives](quest_objectives.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_poi_points](quest_poi_points.md).`QuestID` → [quest_template](quest_template.md).`ID`: Also join blob keys to quest_poi.
- [quest_pool_members](quest_pool_members.md).`questId` → [quest_template](quest_template.md).`ID`: Quest selected by pool.
- [quest_offer_reward_conditional](quest_offer_reward_conditional.md).`QuestId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [gameobject_queststarter](gameobject_queststarter.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.
- [quest_request_items_conditional](quest_request_items_conditional.md).`QuestId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_description_conditional](quest_description_conditional.md).`QuestId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [gameobject_questender](gameobject_questender.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.
- [quest_mail_sender](quest_mail_sender.md).`QuestId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_reward_display_spell](quest_reward_display_spell.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [creature_questender](creature_questender.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.
- [quest_poi](quest_poi.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_reward_choice_items](quest_reward_choice_items.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_completion_log_conditional](quest_completion_log_conditional.md).`QuestId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_treasure_pickers](quest_treasure_pickers.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_reward_house_decor](quest_reward_house_decor.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_template_locale](quest_template_locale.md).`ID` → [quest_template](quest_template.md).`ID`: Translation parent identity; include all identity components plus locale.
- [creature_queststarter](creature_queststarter.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.
- [quest_pool_members](quest_pool_members.md).`questId` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_poi_points](quest_poi_points.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_reward_house_room](quest_reward_house_room.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:4554](../../../src/server/game/Globals/ObjectMgr.cpp#L4554)
- [src/server/game/Quests/QuestDef.cpp:53](../../../src/server/game/Quests/QuestDef.cpp#L53)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `_id(questRecord.ID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L89) |
| `QuestType` | `_type(questRecord.QuestType().GetUInt8()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L90) |
| `QuestPackageID` | `_packageID(questRecord.QuestPackageID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L91) |
| `ContentTuningID` | `_contentTuningID(questRecord.ContentTuningID().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L92) |
| `QuestSortID` | `_questSortID(questRecord.QuestSortID().GetInt16()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L93) |
| `QuestInfoID` | `_questInfoID(questRecord.QuestInfoID().GetUInt16()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L94) |
| `SuggestedGroupNum` | `_suggestedPlayers(questRecord.SuggestedGroupNum().GetUInt8()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L95) |
| `RewardNextQuest` | `_rewardNextQuest(questRecord.RewardNextQuest().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L96) |
| `RewardXPDifficulty` | `_rewardXPDifficulty(questRecord.RewardXPDifficulty().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L97) |
| `RewardXPMultiplier` | `_rewardXPMultiplier(questRecord.RewardXPMultiplier().GetFloat()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L98) |
| `RewardMoneyDifficulty` | `_rewardMoneyDifficulty(questRecord.RewardMoneyDifficulty().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L99) |
| `RewardMoneyMultiplier` | `_rewardMoneyMultiplier(questRecord.RewardMoneyMultiplier().GetFloat()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L100) |
| `RewardBonusMoney` | `_rewardBonusMoney(questRecord.RewardBonusMoney().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L101) |
| `RewardSpell` | `_rewardSpell(questRecord.RewardSpell().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L102) |
| `RewardHonor` | `_rewardHonor(questRecord.RewardHonor().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L103) |
| `RewardKillHonor` | `_rewardKillHonor(questRecord.RewardKillHonor().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L104) |
| `StartItem` | `_sourceItemId(questRecord.StartItem().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L109) |
| `RewardArtifactXPDifficulty` | `_rewardArtifactXPDifficulty(questRecord.RewardArtifactXPDifficulty().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L106) |
| `RewardArtifactXPMultiplier` | `_rewardArtifactXPMultiplier(questRecord.RewardArtifactXPMultiplier().GetFloat()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L107) |
| `RewardArtifactCategoryID` | `_rewardArtifactCategoryID(questRecord.RewardArtifactCategoryID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L108) |
| `Flags` | `_flags(questRecord.Flags().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L110) |
| `FlagsEx` | `_flagsEx(questRecord.FlagsEx().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L111) |
| `FlagsEx2` | `_flagsEx2(questRecord.FlagsEx2().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L112) |
| `FlagsEx3` | `_flagsEx3(questRecord.FlagsEx3().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L113) |
| `RewardItem1` | `RewardItemId({ questRecord.RewardItem1().GetUInt32(), questRecord.RewardItem2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L71) |
| `RewardAmount1` | `RewardItemCount({ questRecord.RewardAmount1().GetUInt32(), questRecord.RewardAmount2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L73) |
| `RewardItem2` | `RewardItemId({ questRecord.RewardItem1().GetUInt32(), questRecord.RewardItem2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L71) |
| `RewardAmount2` | `RewardItemCount({ questRecord.RewardAmount1().GetUInt32(), questRecord.RewardAmount2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L73) |
| `RewardItem3` | `questRecord.RewardItem3().GetUInt32(), questRecord.RewardItem4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L72) |
| `RewardAmount3` | `questRecord.RewardAmount3().GetUInt32(), questRecord.RewardAmount4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L74) |
| `RewardItem4` | `questRecord.RewardItem3().GetUInt32(), questRecord.RewardItem4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L72) |
| `RewardAmount4` | `questRecord.RewardAmount3().GetUInt32(), questRecord.RewardAmount4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L74) |
| `ItemDrop1` | `ItemDrop({ questRecord.ItemDrop1().GetUInt32(), questRecord.ItemDrop2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L58) |
| `ItemDropQuantity1` | `ItemDropQuantity({ questRecord.ItemDropQuantity1().GetUInt32(), questRecord.ItemDropQuantity2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L60) |
| `ItemDrop2` | `ItemDrop({ questRecord.ItemDrop1().GetUInt32(), questRecord.ItemDrop2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L58) |
| `ItemDropQuantity2` | `ItemDropQuantity({ questRecord.ItemDropQuantity1().GetUInt32(), questRecord.ItemDropQuantity2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L60) |
| `ItemDrop3` | `questRecord.ItemDrop3().GetUInt32(), questRecord.ItemDrop4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L59) |
| `ItemDropQuantity3` | `questRecord.ItemDropQuantity3().GetUInt32(), questRecord.ItemDropQuantity4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L61) |
| `ItemDrop4` | `questRecord.ItemDrop3().GetUInt32(), questRecord.ItemDrop4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L59) |
| `ItemDropQuantity4` | `questRecord.ItemDropQuantity3().GetUInt32(), questRecord.ItemDropQuantity4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L61) |
| `RewardChoiceItemID1` | `RewardChoiceItemId({ questRecord.RewardChoiceItemID1().GetUInt32(), questRecord.RewardChoiceItemID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L62) |
| `RewardChoiceItemQuantity1` | `RewardChoiceItemCount({ questRecord.RewardChoiceItemQuantity1().GetUInt32(), questRecord.RewardChoiceItemQuantity2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L65) |
| `RewardChoiceItemDisplayID1` | `RewardChoiceItemDisplayId({ questRecord.RewardChoiceItemDisplayID1().GetUInt32(), questRecord.RewardChoiceItemDisplayID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L68) |
| `RewardChoiceItemID2` | `RewardChoiceItemId({ questRecord.RewardChoiceItemID1().GetUInt32(), questRecord.RewardChoiceItemID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L62) |
| `RewardChoiceItemQuantity2` | `RewardChoiceItemCount({ questRecord.RewardChoiceItemQuantity1().GetUInt32(), questRecord.RewardChoiceItemQuantity2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L65) |
| `RewardChoiceItemDisplayID2` | `RewardChoiceItemDisplayId({ questRecord.RewardChoiceItemDisplayID1().GetUInt32(), questRecord.RewardChoiceItemDisplayID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L68) |
| `RewardChoiceItemID3` | `questRecord.RewardChoiceItemID3().GetUInt32(), questRecord.RewardChoiceItemID4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L63) |
| `RewardChoiceItemQuantity3` | `questRecord.RewardChoiceItemQuantity3().GetUInt32(), questRecord.RewardChoiceItemQuantity4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L66) |
| `RewardChoiceItemDisplayID3` | `questRecord.RewardChoiceItemDisplayID3().GetUInt32(), questRecord.RewardChoiceItemDisplayID4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L69) |
| `RewardChoiceItemID4` | `questRecord.RewardChoiceItemID3().GetUInt32(), questRecord.RewardChoiceItemID4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L63) |
| `RewardChoiceItemQuantity4` | `questRecord.RewardChoiceItemQuantity3().GetUInt32(), questRecord.RewardChoiceItemQuantity4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L66) |
| `RewardChoiceItemDisplayID4` | `questRecord.RewardChoiceItemDisplayID3().GetUInt32(), questRecord.RewardChoiceItemDisplayID4().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L69) |
| `RewardChoiceItemID5` | `questRecord.RewardChoiceItemID5().GetUInt32(), questRecord.RewardChoiceItemID6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L64) |
| `RewardChoiceItemQuantity5` | `questRecord.RewardChoiceItemQuantity5().GetUInt32(), questRecord.RewardChoiceItemQuantity6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L67) |
| `RewardChoiceItemDisplayID5` | `questRecord.RewardChoiceItemDisplayID5().GetUInt32(), questRecord.RewardChoiceItemDisplayID6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L70) |
| `RewardChoiceItemID6` | `questRecord.RewardChoiceItemID5().GetUInt32(), questRecord.RewardChoiceItemID6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L64) |
| `RewardChoiceItemQuantity6` | `questRecord.RewardChoiceItemQuantity5().GetUInt32(), questRecord.RewardChoiceItemQuantity6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L67) |
| `RewardChoiceItemDisplayID6` | `questRecord.RewardChoiceItemDisplayID5().GetUInt32(), questRecord.RewardChoiceItemDisplayID6().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L70) |
| `POIContinent` | `_poiContinent(questRecord.POIContinent().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L114) |
| `POIx` | `_poiX(questRecord.POIx().GetFloat()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L115) |
| `POIy` | `_poiY(questRecord.POIy().GetFloat()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L116) |
| `POIPriority` | `_poiPriority(questRecord.POIPriority().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L117) |
| `RewardTitle` | `_rewardTitleId(questRecord.RewardTitle().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L118) |
| `RewardArenaPoints` | `_rewardArenaPoints(questRecord.RewardArenaPoints().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L119) |
| `RewardSkillLineID` | `_rewardSkillId(questRecord.RewardSkillLineID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L120) |
| `RewardNumSkillUps` | `_rewardSkillPoints(questRecord.RewardNumSkillUps().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L121) |
| `PortraitGiver` | `_questGiverPortrait(questRecord.PortraitGiver().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L122) |
| `PortraitGiverMount` | `_questGiverPortraitMount(questRecord.PortraitGiverMount().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L123) |
| `PortraitGiverModelSceneID` | `_questGiverPortraitModelSceneId(questRecord.PortraitGiverModelSceneID().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L124) |
| `PortraitTurnIn` | `_questTurnInPortrait(questRecord.PortraitTurnIn().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L125) |
| `RewardFactionID1` | `RewardFactionId({ questRecord.RewardFactionID1().GetUInt32(), questRecord.RewardFactionID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L75) |
| `RewardFactionValue1` | `RewardFactionValue({ questRecord.RewardFactionValue1().GetInt32(), questRecord.RewardFactionValue2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L77) |
| `RewardFactionOverride1` | `RewardFactionOverride({ questRecord.RewardFactionOverride1().GetInt32(), questRecord.RewardFactionOverride2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L79) |
| `RewardFactionCapIn1` | `RewardFactionCapIn({ questRecord.RewardFactionCapIn1().GetInt32(), questRecord.RewardFactionCapIn2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L81) |
| `RewardFactionID2` | `RewardFactionId({ questRecord.RewardFactionID1().GetUInt32(), questRecord.RewardFactionID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L75) |
| `RewardFactionValue2` | `RewardFactionValue({ questRecord.RewardFactionValue1().GetInt32(), questRecord.RewardFactionValue2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L77) |
| `RewardFactionOverride2` | `RewardFactionOverride({ questRecord.RewardFactionOverride1().GetInt32(), questRecord.RewardFactionOverride2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L79) |
| `RewardFactionCapIn2` | `RewardFactionCapIn({ questRecord.RewardFactionCapIn1().GetInt32(), questRecord.RewardFactionCapIn2().GetInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L81) |
| `RewardFactionID3` | `questRecord.RewardFactionID3().GetUInt32(), questRecord.RewardFactionID4().GetUInt32(), questRecord.RewardFactionID5().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L76) |
| `RewardFactionValue3` | `questRecord.RewardFactionValue3().GetInt32(), questRecord.RewardFactionValue4().GetInt32(), questRecord.RewardFactionValue5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L78) |
| `RewardFactionOverride3` | `questRecord.RewardFactionOverride3().GetInt32(), questRecord.RewardFactionOverride4().GetInt32(), questRecord.RewardFactionOverride5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L80) |
| `RewardFactionCapIn3` | `questRecord.RewardFactionCapIn3().GetInt32(), questRecord.RewardFactionCapIn4().GetInt32(), questRecord.RewardFactionCapIn5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L82) |
| `RewardFactionID4` | `questRecord.RewardFactionID3().GetUInt32(), questRecord.RewardFactionID4().GetUInt32(), questRecord.RewardFactionID5().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L76) |
| `RewardFactionValue4` | `questRecord.RewardFactionValue3().GetInt32(), questRecord.RewardFactionValue4().GetInt32(), questRecord.RewardFactionValue5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L78) |
| `RewardFactionOverride4` | `questRecord.RewardFactionOverride3().GetInt32(), questRecord.RewardFactionOverride4().GetInt32(), questRecord.RewardFactionOverride5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L80) |
| `RewardFactionCapIn4` | `questRecord.RewardFactionCapIn3().GetInt32(), questRecord.RewardFactionCapIn4().GetInt32(), questRecord.RewardFactionCapIn5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L82) |
| `RewardFactionID5` | `questRecord.RewardFactionID3().GetUInt32(), questRecord.RewardFactionID4().GetUInt32(), questRecord.RewardFactionID5().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L76) |
| `RewardFactionValue5` | `questRecord.RewardFactionValue3().GetInt32(), questRecord.RewardFactionValue4().GetInt32(), questRecord.RewardFactionValue5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L78) |
| `RewardFactionOverride5` | `questRecord.RewardFactionOverride3().GetInt32(), questRecord.RewardFactionOverride4().GetInt32(), questRecord.RewardFactionOverride5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L80) |
| `RewardFactionCapIn5` | `questRecord.RewardFactionCapIn3().GetInt32(), questRecord.RewardFactionCapIn4().GetInt32(), questRecord.RewardFactionCapIn5().GetInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L82) |
| `RewardFactionFlags` | `_rewardReputationMask(questRecord.RewardFactionFlags().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L126) |
| `RewardCurrencyID1` | `RewardCurrencyId({ questRecord.RewardCurrencyID1().GetUInt32(), questRecord.RewardCurrencyID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L83) |
| `RewardCurrencyQty1` | `RewardCurrencyCount({ questRecord.RewardCurrencyQty1().GetUInt32(), questRecord.RewardCurrencyQty2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L85) |
| `RewardCurrencyID2` | `RewardCurrencyId({ questRecord.RewardCurrencyID1().GetUInt32(), questRecord.RewardCurrencyID2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L83) |
| `RewardCurrencyQty2` | `RewardCurrencyCount({ questRecord.RewardCurrencyQty1().GetUInt32(), questRecord.RewardCurrencyQty2().GetUInt32(),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L85) |
| `RewardCurrencyID3` | `questRecord.RewardCurrencyID3().GetUInt32(), questRecord.RewardCurrencyID4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L84) |
| `RewardCurrencyQty3` | `questRecord.RewardCurrencyQty3().GetUInt32(), questRecord.RewardCurrencyQty4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L86) |
| `RewardCurrencyID4` | `questRecord.RewardCurrencyID3().GetUInt32(), questRecord.RewardCurrencyID4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L84) |
| `RewardCurrencyQty4` | `questRecord.RewardCurrencyQty3().GetUInt32(), questRecord.RewardCurrencyQty4().GetUInt32() }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L86) |
| `AcceptedSoundKitID` | `_soundAccept(questRecord.AcceptedSoundKitID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L127) |
| `CompleteSoundKitID` | `_soundTurnIn(questRecord.CompleteSoundKitID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L128) |
| `AreaGroupID` | `_areaGroupID(questRecord.AreaGroupID().GetUInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L129) |
| `TimeAllowed` | `_limitTime(questRecord.TimeAllowed().GetInt64()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L130) |
| `AllowableRaces` | `_allowableRaces({ .RawValue = advstd::bit_cast<std::array<int32, 2>>(questRecord.AllowableRaces().GetUInt64()) }),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L131) |
| `Expansion` | `_expansion(questRecord.Expansion().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L132) |
| `ManagedWorldStateID` | `_managedWorldStateID(questRecord.ManagedWorldStateID().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L133) |
| `QuestSessionBonus` | `_questSessionBonus(questRecord.QuestSessionBonus().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L134) |
| `LogTitle` | `_logTitle(questRecord.LogTitle().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L135) |
| `LogDescription` | `_logDescription(questRecord.LogDescription().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L136) |
| `QuestDescription` | `_questDescription(questRecord.QuestDescription().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L137) |
| `AreaDescription` | `_areaDescription(questRecord.AreaDescription().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L138) |
| `PortraitGiverText` | `_portraitGiverText(questRecord.PortraitGiverText().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L139) |
| `PortraitGiverName` | `_portraitGiverName(questRecord.PortraitGiverName().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L140) |
| `PortraitTurnInText` | `_portraitTurnInText(questRecord.PortraitTurnInText().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L141) |
| `PortraitTurnInName` | `_portraitTurnInName(questRecord.PortraitTurnInName().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L142) |
| `QuestCompletionLog` | `_questCompletionLog(questRecord.QuestCompletionLog().GetStringView()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L143) |
| `ResetByScheduler` | `_resetByScheduler(questRecord.ResetByScheduler().GetBool())` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L144) |
| `RewardFavor` | `_rewardFavor(questRecord.RewardFavor().GetInt32()),` | [loader](../../../src/server/game/Quests/QuestDef.cpp#L105) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
