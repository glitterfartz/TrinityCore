# Conditions Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## ConditionTypes

[src/server/game/Conditions/ConditionMgr.h:60](../../../src/server/game/Conditions/ConditionMgr.h#L60)

```cpp
enum ConditionTypes
{                                                              // value1                 value2         value3
    CONDITION_NONE                     = 0,                    // 0                      0              0                  always true
    CONDITION_AURA                     = 1,                    // spell_id               effindex       0                  true if target has aura of spell_id with effect effindex
    CONDITION_ITEM                     = 2,                    // item_id                count          bank               true if has #count of item_ids (if 'bank' is set it searches in bank slots too)
    CONDITION_ITEM_EQUIPPED            = 3,                    // item_id                0              0                  true if has item_id equipped
    CONDITION_ZONEID                   = 4,                    // zone_id                0              0                  true if in zone_id
    CONDITION_REPUTATION_RANK          = 5,                    // faction_id             rankMask       0                  true if has min_rank for faction_id
    CONDITION_TEAM                     = 6,                    // player_team            0,             0                  469 - Alliance, 67 - Horde)
    CONDITION_SKILL                    = 7,                    // skill_id               skill_value    0                  true if has skill_value for skill_id
    CONDITION_QUESTREWARDED            = 8,                    // quest_id               0              0                  true if quest_id was rewarded before
    CONDITION_QUESTTAKEN               = 9,                    // quest_id               0,             0                  true while quest active
    CONDITION_DRUNKENSTATE             = 10,                   // DrunkenState           0,             0                  true if player is drunk enough
    CONDITION_WORLD_STATE              = 11,                   // index                  value          0                  true if world has the value for the index
    CONDITION_ACTIVE_EVENT             = 12,                   // event_id               0              0                  true if event is active
    CONDITION_INSTANCE_INFO            = 13,                   // entry                  data           type               true if the instance info defined by type (enum InstanceInfo) equals data.
    CONDITION_QUEST_NONE               = 14,                   // quest_id               0              0                  true if doesn't have quest saved
    CONDITION_CLASS                    = 15,                   // class                  0              0                  true if player's class is equal to class
    CONDITION_RACE                     = 16,                   // race                   0              0                  true if player's race is equal to race
    CONDITION_ACHIEVEMENT              = 17,                   // achievement_id         0              0                  true if achievement is complete
    CONDITION_TITLE                    = 18,                   // title id               0              0                  true if player has title
    CONDITION_SPAWNMASK_DEPRECATED     = 19,                   // DEPRECATED
    CONDITION_GENDER                   = 20,                   // gender                 0              0                  true if player's gender is equal to gender
    CONDITION_UNIT_STATE               = 21,                   // unitState              0              0                  true if unit has unitState
    CONDITION_MAPID                    = 22,                   // map_id                 0              0                  true if in map_id
    CONDITION_AREAID                   = 23,                   // area_id                0              0                  true if in area_id
    CONDITION_CREATURE_TYPE            = 24,                   // cinfo.type             0              0                  true if creature_template.type = value1
    CONDITION_SPELL                    = 25,                   // spell_id               0              0                  true if player has learned spell
    CONDITION_PHASEID                  = 26,                   // phaseid                0              0                  true if object is in phaseid
    CONDITION_LEVEL                    = 27,                   // level                  ComparisonType 0                  true if unit's level is equal to param1 (param2 can modify the statement)
    CONDITION_QUEST_COMPLETE           = 28,                   // quest_id               0              0                  true if player has quest_id with all objectives complete, but not yet rewarded
    CONDITION_NEAR_CREATURE            = 29,                   // creature entry         distance       dead (0/1)         true if there is a creature of entry in range
    CONDITION_NEAR_GAMEOBJECT          = 30,                   // gameobject entry       distance       0                  true if there is a gameobject of entry in range
    CONDITION_OBJECT_ENTRY_GUID_LEGACY = 31,                   // LEGACY_TypeID          entry          guid               true if object is type TypeID and the entry is 0 or matches entry of the object or matches guid of the object
    CONDITION_TYPE_MASK_LEGACY         = 32,                   // LEGACY_TypeMask        0              0                  true if object is type object's TypeMask matches provided TypeMask
    CONDITION_RELATION_TO              = 33,                   // ConditionTarget        RelationType   0                  true if object is in given relation with object specified by ConditionTarget
    CONDITION_REACTION_TO              = 34,                   // ConditionTarget        rankMask       0                  true if object's reaction matches rankMask object specified by ConditionTarget
    CONDITION_DISTANCE_TO              = 35,                   // ConditionTarget        distance       ComparisonType     true if object and ConditionTarget are within distance given by parameters
    CONDITION_ALIVE                    = 36,                   // 0                      0              0                  true if unit is alive
    CONDITION_HP_VAL                   = 37,                   // hpVal                  ComparisonType 0                  true if unit's hp matches given value
    CONDITION_HP_PCT                   = 38,                   // hpPct                  ComparisonType 0                  true if unit's hp matches given pct
    CONDITION_REALM_ACHIEVEMENT        = 39,                   // achievement_id         0              0                  true if realm achievement is complete
    CONDITION_IN_WATER                 = 40,                   // 0                      0              0                  true if unit in water
    CONDITION_TERRAIN_SWAP             = 41,                   // terrainSwap            0              0                  true if object is in terrainswap
    CONDITION_STAND_STATE              = 42,                   // stateType              state          0                  true if unit matches specified sitstate (0,x: has exactly state x; 1,0: any standing state; 1,1: any sitting state;)
    CONDITION_DAILY_QUEST_DONE         = 43,                   // quest id               0              0                  true if daily quest has been completed for the day
    CONDITION_CHARMED                  = 44,                   // 0                      0              0                  true if unit is currently charmed
    CONDITION_PET_TYPE                 = 45,                   // mask                   0              0                  true if player has a pet of given type(s)
    CONDITION_TAXI                     = 46,                   // 0                      0              0                  true if player is on taxi
    CONDITION_QUESTSTATE               = 47,                   // quest_id               state_mask     0                  true if player is in any of the provided quest states for the quest (1 = not taken, 2 = completed, 8 = in progress, 32 = failed, 64 = rewarded)
    CONDITION_QUEST_OBJECTIVE_PROGRESS = 48,                   // ID                     0              progressValue      true if player has ID objective progress equal to ConditionValue3 (and quest is in quest log)
    CONDITION_DIFFICULTY_ID            = 49,                   // Difficulty             0              0                  true is map has difficulty id
    CONDITION_GAMEMASTER               = 50,                   // canBeGM                0              0                  true if player is gamemaster (or can be gamemaster)
    CONDITION_OBJECT_ENTRY_GUID        = 51,                   // TypeID                 entry          guid               true if object is type TypeID and the entry is 0 or matches entry of the object or matches guid of the object
    CONDITION_TYPE_MASK                = 52,                   // TypeMask               0              0                  true if object is type object's TypeMask matches provided TypeMask
    CONDITION_BATTLE_PET_COUNT         = 53,                   // SpecieId               count          ComparisonType     true if player has `count` of battle pet species
    CONDITION_SCENARIO_STEP            = 54,                   // ScenarioStepId         0              0                  true if player is at scenario with current step equal to ScenarioStepID
    CONDITION_SCENE_IN_PROGRESS        = 55,                   // SceneScriptPackageId   0              0                  true if player is playing a scene with ScriptPackageId equal to given value
    CONDITION_PLAYER_CONDITION         = 56,                   // PlayerConditionId      0              0                  true if player satisfies PlayerCondition
    CONDITION_PRIVATE_OBJECT           = 57,                   // 0                      0              0                  true if entity is private object
    CONDITION_STRING_ID                = 58,
    CONDITION_LABEL                    = 59,                   // Label                  0              0                  true if creature/gameobject has specified Label in CreatureLabel.db2/GameObjectLabel.db2
    CONDITION_GROUP_STATUS             = 60,                   // GroupStatus            0              0                  true if player group status is (0 = not in group, 1 = in group, 2 = in group but not in raid, 3 = in raid group, 4 = not in group or not in raid)
    CONDITION_MAX
};
```

## ConditionSourceType

[src/server/game/Conditions/ConditionMgr.h:155](../../../src/server/game/Conditions/ConditionMgr.h#L155)

```cpp
enum ConditionSourceType
{
    CONDITION_SOURCE_TYPE_NONE                           = 0,
    CONDITION_SOURCE_TYPE_CREATURE_LOOT_TEMPLATE         = 1,
    CONDITION_SOURCE_TYPE_DISENCHANT_LOOT_TEMPLATE       = 2,
    CONDITION_SOURCE_TYPE_FISHING_LOOT_TEMPLATE          = 3,
    CONDITION_SOURCE_TYPE_GAMEOBJECT_LOOT_TEMPLATE       = 4,
    CONDITION_SOURCE_TYPE_ITEM_LOOT_TEMPLATE             = 5,
    CONDITION_SOURCE_TYPE_MAIL_LOOT_TEMPLATE             = 6,
    CONDITION_SOURCE_TYPE_MILLING_LOOT_TEMPLATE          = 7,
    CONDITION_SOURCE_TYPE_PICKPOCKETING_LOOT_TEMPLATE    = 8,
    CONDITION_SOURCE_TYPE_PROSPECTING_LOOT_TEMPLATE      = 9,
    CONDITION_SOURCE_TYPE_REFERENCE_LOOT_TEMPLATE        = 10,
    CONDITION_SOURCE_TYPE_SKINNING_LOOT_TEMPLATE         = 11,
    CONDITION_SOURCE_TYPE_SPELL_LOOT_TEMPLATE            = 12,
    CONDITION_SOURCE_TYPE_SPELL_IMPLICIT_TARGET          = 13,
    CONDITION_SOURCE_TYPE_GOSSIP_MENU                    = 14,
    CONDITION_SOURCE_TYPE_GOSSIP_MENU_OPTION             = 15,
    CONDITION_SOURCE_TYPE_CREATURE_TEMPLATE_VEHICLE      = 16,
    CONDITION_SOURCE_TYPE_SPELL                          = 17,
    CONDITION_SOURCE_TYPE_SPELL_CLICK_EVENT              = 18,
    CONDITION_SOURCE_TYPE_QUEST_AVAILABLE                = 19,
    // Condition source type 20 unused
    CONDITION_SOURCE_TYPE_VEHICLE_SPELL                  = 21,
    CONDITION_SOURCE_TYPE_SMART_EVENT                    = 22,
    CONDITION_SOURCE_TYPE_NPC_VENDOR                     = 23,
    CONDITION_SOURCE_TYPE_SPELL_PROC                     = 24,
    CONDITION_SOURCE_TYPE_TERRAIN_SWAP                   = 25,
    CONDITION_SOURCE_TYPE_PHASE                          = 26,
    CONDITION_SOURCE_TYPE_GRAVEYARD                      = 27,
    CONDITION_SOURCE_TYPE_AREATRIGGER                    = 28,
    CONDITION_SOURCE_TYPE_CONVERSATION_LINE              = 29,
    CONDITION_SOURCE_TYPE_AREATRIGGER_CLIENT_TRIGGERED   = 30,
    CONDITION_SOURCE_TYPE_TRAINER_SPELL                  = 31,
    CONDITION_SOURCE_TYPE_OBJECT_ID_VISIBILITY           = 32,
    CONDITION_SOURCE_TYPE_SPAWN_GROUP                    = 33,
    CONDITION_SOURCE_TYPE_PLAYER_CONDITION               = 34,
    CONDITION_SOURCE_TYPE_SKILL_LINE_ABILITY             = 35,
    CONDITION_SOURCE_TYPE_PLAYER_CHOICE_RESPONSE         = 36,

    CONDITION_SOURCE_TYPE_MAX_DB_ALLOWED,
    CONDITION_SOURCE_TYPE_REFERENCE_CONDITION            = CONDITION_SOURCE_TYPE_MAX_DB_ALLOWED, // internal, not set in db
    CONDITION_SOURCE_TYPE_MAX                            // MAX
};
```

## RelationType

[src/server/game/Conditions/ConditionMgr.h:200](../../../src/server/game/Conditions/ConditionMgr.h#L200)

```cpp
enum RelationType
{
    RELATION_SELF = 0,
    RELATION_IN_PARTY,
    RELATION_IN_RAID_OR_PARTY,
    RELATION_OWNED_BY,
    RELATION_PASSENGER_OF,
    RELATION_CREATED_BY,
    RELATION_MAX
};
```

## InstanceInfo

[src/server/game/Conditions/ConditionMgr.h:211](../../../src/server/game/Conditions/ConditionMgr.h#L211)

```cpp
enum InstanceInfo
{
    INSTANCE_INFO_DATA = 0,
    INSTANCE_INFO_GUID_DATA,
    INSTANCE_INFO_BOSS_STATE,
    INSTANCE_INFO_DATA64
};
```

## GroupStatusCondition

[src/server/game/Conditions/ConditionMgr.h:219](../../../src/server/game/Conditions/ConditionMgr.h#L219)

```cpp
enum class GroupStatusCondition : uint32
{
    NotInGroup              = 0,
    InGroup                 = 1,
    InGroupButNotInRaid     = 2,
    InRaid                  = 3,
    NotInGroupOrNotInRaid   = 4
};
```

## MaxConditionTargets

[src/server/game/Conditions/ConditionMgr.h:228](../../../src/server/game/Conditions/ConditionMgr.h#L228)

```cpp
enum MaxConditionTargets
{
    MAX_CONDITION_TARGETS = 3
};
```
