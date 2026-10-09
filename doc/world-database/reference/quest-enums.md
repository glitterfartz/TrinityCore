# Quest Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## QuestFailedReason

[src/server/game/Quests/QuestDef.h:54](../../../src/server/game/Quests/QuestDef.h#L54)

```cpp
enum QuestFailedReason : uint32
{
    QUEST_ERR_NONE                              = 0,
    QUEST_ERR_FAILED_LOW_LEVEL                  = 1,        // DESCRIPTION "You are not high enough level for that quest.""
    QUEST_ERR_FAILED_WRONG_RACE                 = 6,        // DESCRIPTION "That quest is not available to your race."
    QUEST_ERR_ALREADY_DONE                      = 7,        // DESCRIPTION "You have completed that daily quest today."
    QUEST_ERR_ONLY_ONE_TIMED                    = 12,       // DESCRIPTION "You can only be on one timed quest at a time"
    QUEST_ERR_ALREADY_ON1                       = 13,       // DESCRIPTION "You are already on that quest"
    QUEST_ERR_FAILED_EXPANSION                  = 16,       // DESCRIPTION "This quest requires an expansion enabled account."
    QUEST_ERR_ALREADY_ON2                       = 18,       // DESCRIPTION "You are already on that quest"
    QUEST_ERR_FAILED_MISSING_ITEMS              = 21,       // DESCRIPTION "You don't have the required items with you.  Check storage."
    QUEST_ERR_FAILED_NOT_ENOUGH_MONEY           = 23,       // DESCRIPTION "You don't have enough money for that quest"
    QUEST_ERR_FAILED_CAIS                       = 24,       // DESCRIPTION "You cannot complete quests once you have reached tired time"
    QUEST_ERR_ALREADY_DONE_DAILY                = 26,       // DESCRIPTION "You have completed that daily quest today."
    QUEST_ERR_FAILED_SPELL                      = 28,       // DESCRIPTION "You haven't learned the required spell."
    QUEST_ERR_HAS_IN_PROGRESS                   = 30        // DESCRIPTION "Progress Bar objective not completed"
};
```

## QuestPushReason

[src/server/game/Quests/QuestDef.h:73](../../../src/server/game/Quests/QuestDef.h#L73)

```cpp
enum class QuestPushReason : uint8
{
    Success                         = 0,    // "Sharing quest with %s..."
    Invalid                         = 1,    // "%s is not eligible for that quest"
    InvalidToRecipient              = 2,    // "%s's attempt to share quest "%s" failed. You are not eligible for that quest."
    Accepted                        = 3,    // "%s has accepted your quest"
    Declined                        = 4,    // "%s has declined your quest"
    Busy                            = 5,    // "%s is busy"
    Dead                            = 6,    // "%s is dead."
    DeadToRecipient                 = 7,    // "%s's attempt to share quest "%s" failed. You are dead."
    LogFull                         = 8,    // "%s's quest log is full"
    LogFullToRecipient              = 9,    // "%s's attempt to share quest "%s" failed. Your quest log is full."
    OnQuest                         = 10,   // "%s is already on that quest"
    OnQuestToRecipient              = 11,   // "%s's attempt to share quest "%s" failed. You are already on that quest."
    AlreadyDone                     = 12,   // "%s has completed that quest"
    AlreadyDoneToRecipient          = 13,   // "%s's attempt to share quest "%s" failed. You have completed that quest."
    NotDaily                        = 14,   // "That quest cannot be shared today"
    TimerExpired                    = 15,   // "Quest sharing timer has expired"
    NotInParty                      = 16,   // "You are not in a party"
    DifferentServerDaily            = 17,   // "%s is not eligible for that quest today"
    DifferentServerDailyToRecipient = 18,   // "%s's attempt to share quest "%s" failed. You are not eligible for that quest today."
    NotAllowed                      = 19,   // "That quest cannot be shared"
    Prerequisite                    = 20,   // "%s hasn't completed all of the prerequisite quests required for that quest."
    PrerequisiteToRecipient         = 21,   // "%s's attempt to share quest "%s" failed. You must complete all of the prerequisite quests first."
    LowLevel                        = 22,   // "%s is too low level for that quest."
    LowLevelToRecipient             = 23,   // "%s's attempt to share quest "%s" failed. You are too low level for that quest."
    HighLevel                       = 24,   // "%s is too high level for that quest."
    HighLevelToRecipient            = 25,   // "%s's attempt to share quest "%s" failed. You are too high level for that quest."
    Class                           = 26,   // "%s is the wrong class for that quest."
    ClassToRecipient                = 27,   // "%s's attempt to share quest "%s" failed. You are the wrong class for that quest."
    Race                            = 28,   // "%s is the wrong race for that quest."
    RaceToRecipient                 = 29,   // "%s's attempt to share quest "%s" failed. You are the wrong race for that quest."
    LowFaction                      = 30,   // "%s's reputation is too low for that quest."
    LowFactionToRecipient           = 31,   // "%s's attempt to share quest "%s" failed. Your reputation is too low for that quest."
    HighFaction                     = 32,   // "%s's reputation is too high for that quest."
    HighFactionToRecipient          = 33,   // "%s's attempt to share quest "%s" failed. Your reputation is too high for that quest."
    Expansion                       = 34,   // "%s doesn't own the required expansion for that quest."
    ExpansionToRecipient            = 35,   // "%s's attempt to share quest "%s" failed. You do not own the required expansion for that quest."
    NotGarrisonOwner                = 36,   // "%s must own a garrison to accept that quest."
    NotGarrisonOwnerToRecipient     = 37,   // "%s's attempt to share quest "%s" failed. You must own a garrison to accept that quest."
    WrongCovenant                   = 38,   // "%s is in the wrong covenant for that quest."
    WrongCovenantToRecipient        = 39,   // "%s's attempt to share quest "%s" failed. You are in the wrong covenant for that quest."
    NewPlayerExperience             = 40,   // "%s must complete Exile's Reach to accept that quest."
    NewPlayerExperienceToRecipient  = 41,   // "%s's attempt to share quest "%s" failed. You must complete Exile's Reach to accept that quest."
    WrongFaction                    = 42,   // "%s is the wrong faction for that quest."
    WrongFactionToRecipient         = 43,   // "%s's attempt to share quest "%s" failed. You are the wrong faction for that quest."
    CrossFactionRestricted          = 44,   // "Quests can't be shared in cross-faction groups."
};
```

## QuestTradeSkill

[src/server/game/Quests/QuestDef.h:122](../../../src/server/game/Quests/QuestDef.h#L122)

```cpp
enum QuestTradeSkill
{
    QUEST_TRSKILL_NONE           = 0,
    QUEST_TRSKILL_ALCHEMY        = 1,
    QUEST_TRSKILL_BLACKSMITHING  = 2,
    QUEST_TRSKILL_COOKING        = 3,
    QUEST_TRSKILL_ENCHANTING     = 4,
    QUEST_TRSKILL_ENGINEERING    = 5,
    QUEST_TRSKILL_FIRSTAID       = 6,
    QUEST_TRSKILL_HERBALISM      = 7,
    QUEST_TRSKILL_LEATHERWORKING = 8,
    QUEST_TRSKILL_POISONS        = 9,
    QUEST_TRSKILL_TAILORING      = 10,
    QUEST_TRSKILL_MINING         = 11,
    QUEST_TRSKILL_FISHING        = 12,
    QUEST_TRSKILL_SKINNING       = 13,
    QUEST_TRSKILL_JEWELCRAFTING  = 14
};
```

## QuestStatus

[src/server/game/Quests/QuestDef.h:141](../../../src/server/game/Quests/QuestDef.h#L141)

```cpp
enum QuestStatus : uint8
{
    QUEST_STATUS_NONE           = 0,
    QUEST_STATUS_COMPLETE       = 1,
    //QUEST_STATUS_UNAVAILABLE    = 2,
    QUEST_STATUS_INCOMPLETE     = 3,
    //QUEST_STATUS_AVAILABLE      = 4,
    QUEST_STATUS_FAILED         = 5,
    QUEST_STATUS_REWARDED       = 6,        // Not used in DB
    MAX_QUEST_STATUS
};
```

## QuestGiverStatus

[src/server/game/Quests/QuestDef.h:153](../../../src/server/game/Quests/QuestDef.h#L153)

```cpp
enum class QuestGiverStatus : uint64
{
    None                                = 0x000000000000,
    Future                              = 0x000000000002,
    FutureJourneyQuest                  = 0x000000000004,
    FutureLegendaryQuest                = 0x000000000008,
    FutureImportantQuest                = 0x000000000010,
    TrivialRepeatableTurnin             = 0x000000000020,
    Trivial                             = 0x000000000040,
    TrivialDailyQuest                   = 0x000000000080,
    TrivialRepeatableQuest              = 0x000000000100,
    TrivialMetaQuest                    = 0x000000000200,
    TrivialJourneyQuest                 = 0x000000000400,
    TrivialLegendaryQuest               = 0x000000000800,
    TrivialImportantQuest               = 0x000000001000,
    Reward                              = 0x000000002000,
    RepeatableReward                    = 0x000000004000,
    MetaReward                          = 0x000000008000,
    JourneyReward                       = 0x000000010000,
    CovenantCallingReward               = 0x000000020000,
    LegendaryReward                     = 0x000000040000,
    ImportantReward                     = 0x000000080000,
    RepeatableTurnin                    = 0x000000100000,
    QuestAccountCompleted               = 0x000000200000,
    Quest                               = 0x000000400000,
    DailyQuest                          = 0x000000800000,
    RepeatableQuest                     = 0x000001000000,
    MetaQuest                           = 0x000002000000,
    CovenantCallingQuest                = 0x000004000000,
    JourneyQuestAccountCompleted        = 0x000008000000,
    JourneyQuest                        = 0x000010000000,
    LegendaryQuestAccountCompleted      = 0x000020000000,
    LegendaryQuest                      = 0x000040000000,
    ImportantQuestAccountCompleted      = 0x000080000000,
    ImportantQuest                      = 0x000100000000,
    RewardCompleteNoPOI                 = 0x000200000000,
    RewardCompletePOI                   = 0x000400000000,
    RepeatableRewardCompleteNoPOI       = 0x000800000000,
    RepeatableRewardCompletePOI         = 0x001000000000,
    MetaQuestRewardCompleteNoPOI        = 0x002000000000,
    MetaQuestRewardCompletePOI          = 0x004000000000,
    CovenantCallingRewardCompleteNoPOI  = 0x008000000000,
    CovenantCallingRewardCompletePOI    = 0x010000000000,
    JourneyRewardCompleteNoPOI          = 0x020000000000,
    JourneyRewardCompletePOI            = 0x040000000000,
    LegendaryRewardCompleteNoPOI        = 0x080000000000,
    LegendaryRewardCompletePOI          = 0x100000000000,
    ImportantQuestRewardCompleteNoPOI   = 0x200000000000,
    ImportantQuestRewardCompletePOI     = 0x400000000000,
};
```

## QuestFlags

[src/server/game/Quests/QuestDef.h:211](../../../src/server/game/Quests/QuestDef.h#L211)

```cpp
enum QuestFlags : uint32
{
    QUEST_FLAGS_NONE                        = 0x00000000,
    QUEST_FLAGS_COMPLETION_NO_DEATH         = 0x00000001,
    QUEST_FLAGS_COMPLETION_EVENT            = 0x00000002,
    QUEST_FLAGS_COMPLETION_AREA_TRIGGER     = 0x00000004,
    QUEST_FLAGS_SHARABLE                    = 0x00000008,   // Can be shared: Player::CanShareQuest()
    QUEST_FLAGS_HAS_CONDITION               = 0x00000010,   // Not used currently
    QUEST_FLAGS_HIDE_REWARD_POI             = 0x00000020,   // Hides questgiver turn-in minimap icon
    QUEST_FLAGS_RAID_GROUP_OK               = 0x00000040,   // Can be completed while in raid
    QUEST_FLAGS_WAR_MODE_REWARDS_OPT_IN     = 0x00000080,   // Not used currently
    QUEST_FLAGS_NO_MONEY_FOR_XP             = 0x00000100,   // Experience is not converted to gold at max level
    QUEST_FLAGS_HIDE_REWARD                 = 0x00000200,   // Items and money rewarded only sent in SMSG_QUESTGIVER_OFFER_REWARD (not in SMSG_QUEST_GIVER_QUEST_DETAILS or in client quest log(SMSG_QUEST_QUERY_RESPONSE))
    QUEST_FLAGS_TRACKING_EVENT              = 0x00000400,   // These quests are automatically rewarded on quest complete and they will never appear in quest log client side.
    QUEST_FLAGS_DEPRECATE_REPUTATION        = 0x00000800,   // Not used currently
    QUEST_FLAGS_DAILY                       = 0x00001000,   // Used to know quest is Daily one
    QUEST_FLAGS_FLAGS_PVP                   = 0x00002000,   // Having this quest in log forces PvP flag
    QUEST_FLAGS_DEPRECATED                  = 0x00004000,   // Used on quests that are not generally available
    QUEST_FLAGS_WEEKLY                      = 0x00008000,
    QUEST_FLAGS_AUTO_COMPLETE               = 0x00010000,   // Quests with this flag player submit automatically by special button in player gui
    QUEST_FLAGS_DISPLAY_ITEM_IN_TRACKER     = 0x00020000,   // Displays usable item in quest tracker
    QUEST_FLAGS_DISABLE_COMPLETION_TEXT     = 0x00040000,   // use Objective text as Complete text
    QUEST_FLAGS_AUTO_ACCEPT                 = 0x00080000,   // The client recognizes this flag as auto-accept.
    QUEST_FLAGS_PLAYER_CAST_ACCEPT          = 0x00100000,   // Accept Spell Player Cast
    QUEST_FLAGS_PLAYER_CAST_COMPLETE        = 0x00200000,   // Complete Spell Player Cast
    QUEST_FLAGS_UPDATE_PHASESHIFT           = 0x00400000,   // Update Phase Shift
    QUEST_FLAGS_SOR_WHITELIST               = 0x00800000,   // Scroll of Resurrection Whitelist
    QUEST_FLAGS_LAUNCH_GOSSIP_COMPLETE      = 0x01000000,   // Gossip on Quest Completion - Force Gossip
    QUEST_FLAGS_REMOVE_SURPLUS_ITEMS        = 0x02000000,   // Remove all items from inventory that have the same id as the objective, not just the amount required by quest
    QUEST_FLAGS_WELL_KNOWN                  = 0x04000000,   // Well-Known
    QUEST_FLAGS_PORTRAIT_IN_QUEST_LOG       = 0x08000000,   // Portrait from Log
    QUEST_FLAGS_SHOW_ITEM_WHEN_COMPLETED    = 0x10000000,   // Show Item When Completed
    QUEST_FLAGS_LAUNCH_GOSSIP_ACCEPT        = 0x20000000,   // Gossip on Quest Accept - Force Gossip
    QUEST_FLAGS_ITEMS_GLOW_WHEN_COMPLETE    = 0x40000000,   // Items Glow When Done
    QUEST_FLAGS_FAIL_ON_LOGOUT              = 0x80000000    // Fail on Logout
};
```

## QuestFlagsEx

[src/server/game/Quests/QuestDef.h:249](../../../src/server/game/Quests/QuestDef.h#L249)

```cpp
enum QuestFlagsEx : uint32
{
    QUEST_FLAGS_EX_NONE                                     = 0x00000000,
    QUEST_FLAGS_EX_NO_ITEM_REMOVAL                          = 0x00000001,   // Keep Additional Items
    QUEST_FLAGS_EX_SUPPRESS_GOSSIP_COMPLETE                 = 0x00000002,   // Gossip on Quest Completion - Suppress Gossip
    QUEST_FLAGS_EX_SUPPRESS_GOSSIP_ACCEPT                   = 0x00000004,   // Gossip on Quest Accept - Suppress Gossip
    QUEST_FLAGS_EX_DENY_PLAYER_QUESTGIVER                   = 0x00000008,   // Disallow Player as Questgiver (advanced)
    QUEST_FLAGS_EX_DISPLAY_CLASS_CHOICE_REWARDS             = 0x00000010,   // Choice Reward Filter - Matches Class
    QUEST_FLAGS_EX_DISPLAY_SPEC_CHOICE_REWARDS              = 0x00000020,   // Choice Reward Filter - Matches Spec
    QUEST_FLAGS_EX_REMOVE_ON_PERIODIC_RESET                 = 0x00000040,   // Remove from Log on Periodic Reset
    QUEST_FLAGS_EX_ACCOUNT                                  = 0x00000080,   // Account-Level Quest
    QUEST_FLAGS_EX_LEGENDARY                                = 0x00000100,   // Legendary Quest
    QUEST_FLAGS_EX_NO_GUILD_XP                              = 0x00000200,   // No Guild XP
    QUEST_FLAGS_EX_RESET_CACHE_ON_ACCEPT                    = 0x00000400,   // Reset Cache on Accept (internal)
    QUEST_FLAGS_EX_NO_ABANDON_ONCE_BEGUN                    = 0x00000800,   // No Abandon Once Any Objective Complete
    QUEST_FLAGS_EX_RECAST_ACCEPT_SPELL_ON_LOGIN             = 0x00001000,   // Recast accept spell on login
    QUEST_FLAGS_EX_UPDATE_ZONE_AURAS                        = 0x00002000,   // Update Zone Auras
    QUEST_FLAGS_EX_NO_CREDIT_FOR_PROXY                      = 0x00004000,   // No Credit for Proxy Creatures
    QUEST_FLAGS_EX_DISPLAY_AS_DAILY                         = 0x00008000,   // Display As Daily Quest
    QUEST_FLAGS_EX_DISPLAY_QUEST_LINE                       = 0x00010000,
    QUEST_FLAGS_EX_INTERNAL_BUILDS_ONLY                     = 0x00020000,   // Quest for Internal Builds ONLY
    QUEST_FLAGS_EX_SUPPRESS_SPELL_LEARN_TEXT                = 0x00040000,   // Suppress spell learn text line (for followers)
    QUEST_FLAGS_EX_DISPLAY_AS_OBJECTIVE                     = 0x00080000,   // Display Header as Objective for Tasks
    QUEST_FLAGS_EX_ALLOW_ALL_IN_GARRISON                    = 0x00100000,   // Garrison non-owners allowed
    QUEST_FLAGS_EX_REMOVE_ON_WEEKLY_RESET                   = 0x00200000,   // Remove quest on weekly reset
    QUEST_FLAGS_EX_SUPPRESS_GREETINGS_ON_ACCEPT             = 0x00400000,   // Suppress farewell audio after quest accept
    QUEST_FLAGS_EX_REWARDS_IGNORE_CAPS                      = 0x00800000,   // Rewards bypass weekly caps and Season Total
    QUEST_FLAGS_EX_IS_WORLD_QUEST                           = 0x01000000,   // Is a World Quest
    QUEST_FLAGS_EX_NOT_IGNORABLE                            = 0x02000000,   // Not Ignorable
    QUEST_FLAGS_EX_AUTO_PUSH                                = 0x04000000,   // Auto Push
    QUEST_FLAGS_EX_NO_SPELL_COMPLETE_EFFECTS                = 0x08000000,   // No Complete Quest Spell Effect
    QUEST_FLAGS_EX_DO_NOT_TOAST_HONOR_REWARD                = 0x10000000,   // Do Not Toast Honor Reward
    QUEST_FLAGS_EX_KEEP_REPEATABLE_QUEST_ON_FACTION_CHANGE  = 0x20000000,   // Keep repeatable quest on faction change
    QUEST_FLAGS_EX_KEEP_PROGRESS_ON_FACTION_CHANGE          = 0x40000000,   // Keep quest progress on faction change
    QUEST_FLAGS_EX_PUSH_TEAM_QUEST_USING_MAP_CONTROLLER     = 0x80000000
};
```

## QuestFlagsEx2

[src/server/game/Quests/QuestDef.h:286](../../../src/server/game/Quests/QuestDef.h#L286)

```cpp
enum QuestFlagsEx2 : uint32
{
    QUEST_FLAGS_EX2_RESET_ON_GAME_MILESTONE             = 0x00000001,
    QUEST_FLAGS_EX2_WAR_MODE_REWARDS_OPT_OUT            = 0x00000002,
    QUEST_FLAGS_EX2_AWARD_HIGHEST_PROFESSION            = 0x00000004,
    QUEST_FLAGS_EX2_NOT_REPLAYABLE                      = 0x00000008,
    QUEST_FLAGS_EX2_NO_REPLAY_REWARDS                   = 0x00000010,
    QUEST_FLAGS_EX2_DISABLE_WAYPOINT_PATHING            = 0x00000020,
    QUEST_FLAGS_EX2_RESET_ON_MYTHIC_PLUS_SEASON         = 0x00000040,
    QUEST_FLAGS_EX2_RESET_ON_PVP_SEASON                 = 0x00000080,
    QUEST_FLAGS_EX2_ENABLE_OVERRIDE_SORT_ORDER          = 0x00000100,
    QUEST_FLAGS_EX2_FORCE_STARTING_LOC_ON_ZONE_MAP      = 0x00000200,
    QUEST_FLAGS_EX2_BONUS_LOOT_NEVER                    = 0x00000400,
    QUEST_FLAGS_EX2_BONUS_LOOT_ALWAYS                   = 0x00000800,
    QUEST_FLAGS_EX2_HIDE_TASK_ON_MAIN_MAP               = 0x00001000,
    QUEST_FLAGS_EX2_HIDE_TASK_IN_TRACKER                = 0x00002000,
    QUEST_FLAGS_EX2_SKIP_DISABLED_CHECK                 = 0x00004000,
    QUEST_FLAGS_EX2_ENFORCE_MAXIMUM_QUEST_LEVEL         = 0x00008000,
    QUEST_FLAGS_EX2_CONTENT_ALERT                       = 0x00010000,
    QUEST_FLAGS_EX2_DISPLAY_TIME_REMAINING              = 0x00020000,
    QUEST_FLAGS_EX2_CLEAR_TASK_PROGRESS_WHEN_ABANDONED  = 0x00040000,
    QUEST_FLAGS_EX2_SUPPRESS_GREETINGS_ON_COMPLETE      = 0x00080000,
    QUEST_FLAGS_EX2_HIDE_REQUIRED_ITEMS_ON_TURN_IN      = 0x00100000,
    QUEST_FLAGS_EX2_IGNORE_SOULBOUND_ITEMS              = 0x00200000,
    QUEST_FLAGS_EX2_DONT_DEFER_START_EFFECTS            = 0x00400000,
    QUEST_FLAGS_EX2_HIDE_REQUIRED_ITEMS_PRE_TURN_IN     = 0x00800000,

    QUEST_FLAGS_EX2_ABANDON_ON_DISABLE                  = 0x04000000,
};
```

## QuestSpecialFlags

[src/server/game/Quests/QuestDef.h:316](../../../src/server/game/Quests/QuestDef.h#L316)

```cpp
enum QuestSpecialFlags
{
    QUEST_SPECIAL_FLAGS_NONE                 = 0x000,
    // Trinity flags for set SpecialFlags in DB if required but used only at server
    QUEST_SPECIAL_FLAGS_REPEATABLE           = 0x001,   // Set by 1 in SpecialFlags from DB
    QUEST_SPECIAL_FLAGS_AUTO_PUSH_TO_PARTY   = 0x002,   // Set by 2 in SpecialFlags from DB will make quest be pushed to entire party when one member accepts it
    QUEST_SPECIAL_FLAGS_AUTO_ACCEPT          = 0x004,   // Set by 4 in SpecialFlags in DB if the quest is to be auto-accepted.
    QUEST_SPECIAL_FLAGS_DF_QUEST             = 0x008,   // Set by 8 in SpecialFlags in DB if the quest is used by Dungeon Finder.
    QUEST_SPECIAL_FLAGS_MONTHLY              = 0x010,   // Set by 16 in SpecialFlags in DB if the quest is reset at the begining of the month
    // room for more custom flags

    QUEST_SPECIAL_FLAGS_DB_ALLOWED = QUEST_SPECIAL_FLAGS_REPEATABLE | QUEST_SPECIAL_FLAGS_AUTO_PUSH_TO_PARTY | QUEST_SPECIAL_FLAGS_AUTO_ACCEPT | QUEST_SPECIAL_FLAGS_DF_QUEST | QUEST_SPECIAL_FLAGS_MONTHLY,

    QUEST_SPECIAL_FLAGS_SEQUENCED_OBJECTIVES = 0x020,    // Internal flag computed only
};
```

## QuestTagType

[src/server/game/Quests/QuestDef.h:332](../../../src/server/game/Quests/QuestDef.h#L332)

```cpp
enum class QuestTagType
{
    Tag,
    Profession,
    Normal,
    Pvp,
    PetBattle,
    Bounty,
    Dungeon,
    Invasion,
    Raid,
    Contribution,
    RatedRreward,
    InvasionWrapper,
    FactionAssault,
    Islands,
    Threat,
    CovenantCalling
};
```

## QuestObjectiveType

[src/server/game/Quests/QuestDef.h:352](../../../src/server/game/Quests/QuestDef.h#L352)

```cpp
enum QuestObjectiveType
{
    QUEST_OBJECTIVE_MONSTER                 = 0,
    QUEST_OBJECTIVE_ITEM                    = 1,
    QUEST_OBJECTIVE_GAMEOBJECT              = 2,
    QUEST_OBJECTIVE_TALKTO                  = 3,
    QUEST_OBJECTIVE_CURRENCY                = 4,
    QUEST_OBJECTIVE_LEARNSPELL              = 5,
    QUEST_OBJECTIVE_MIN_REPUTATION          = 6,
    QUEST_OBJECTIVE_MAX_REPUTATION          = 7,
    QUEST_OBJECTIVE_MONEY                   = 8,
    QUEST_OBJECTIVE_PLAYERKILLS             = 9,
    QUEST_OBJECTIVE_AREATRIGGER             = 10,
    QUEST_OBJECTIVE_WINPETBATTLEAGAINSTNPC  = 11,
    QUEST_OBJECTIVE_DEFEATBATTLEPET         = 12,
    QUEST_OBJECTIVE_WINPVPPETBATTLES        = 13,
    QUEST_OBJECTIVE_CRITERIA_TREE           = 14,
    QUEST_OBJECTIVE_PROGRESS_BAR            = 15,
    QUEST_OBJECTIVE_HAVE_CURRENCY           = 16,   // requires the player to have X currency when turning in but does not consume it
    QUEST_OBJECTIVE_OBTAIN_CURRENCY         = 17,   // requires the player to gain X currency after starting the quest but not required to keep it until the end (does not consume)
    QUEST_OBJECTIVE_INCREASE_REPUTATION     = 18,   // requires the player to gain X reputation with a faction
    QUEST_OBJECTIVE_AREA_TRIGGER_ENTER      = 19,
    QUEST_OBJECTIVE_AREA_TRIGGER_EXIT       = 20,
    QUEST_OBJECTIVE_KILL_WITH_LABEL         = 21,
    QUEST_OBJECTIVE_UNK_1127                = 22,

    MAX_QUEST_OBJECTIVE_TYPE
};
```

## QuestObjectiveFlags

[src/server/game/Quests/QuestDef.h:381](../../../src/server/game/Quests/QuestDef.h#L381)

```cpp
enum QuestObjectiveFlags
{
    QUEST_OBJECTIVE_FLAG_TRACKED_ON_MINIMAP                 = 0x0001, // client displays large yellow blob on minimap for creature/gameobject
    QUEST_OBJECTIVE_FLAG_SEQUENCED                          = 0x0002, // client will not see the objective displayed until all previous objectives are completed
    QUEST_OBJECTIVE_FLAG_OPTIONAL                           = 0x0004, // not required to complete the quest
    QUEST_OBJECTIVE_FLAG_HIDDEN                             = 0x0008, // never displayed in quest log
    QUEST_OBJECTIVE_FLAG_HIDE_CREDIT_MSG                    = 0x0010, // skip showing item objective progress
    QUEST_OBJECTIVE_FLAG_PRESERVE_QUEST_ITEMS               = 0x0020,
    QUEST_OBJECTIVE_FLAG_PART_OF_PROGRESS_BAR               = 0x0040, // hidden objective used to calculate progress bar percent (quests are limited to a single progress bar objective)
    QUEST_OBJECTIVE_FLAG_KILL_PLAYERS_SAME_FACTION          = 0x0080,
    QUEST_OBJECTIVE_FLAG_NO_SHARE_PROGRESS                  = 0x0100,
    QUEST_OBJECTIVE_FLAG_IGNORE_SOULBOUND_ITEMS             = 0x0200,
};
```

## QuestObjectiveFlags2

[src/server/game/Quests/QuestDef.h:395](../../../src/server/game/Quests/QuestDef.h#L395)

```cpp
enum QuestObjectiveFlags2
{
    QUEST_OBJECTIVE_FLAG_2_QUEST_BOUND_ITEM = 0x1   // Item is bound to a single objective, only increments the counter for one quest if multiple require the same item and is not stored in inventory
};
```

## QuestCompleteSpellType

[src/server/game/Quests/QuestDef.h:400](../../../src/server/game/Quests/QuestDef.h#L400)

```cpp
enum class QuestCompleteSpellType : uint32
{
    LegacyBehavior      = 0,
    Follower            = 1,
    Tradeskill          = 2,
    Ability             = 3,
    Aura                = 4,
    Spell               = 5,
    Unlock              = 6,
    Companion           = 7,
    QuestlineUnlock     = 8,
    QuestlineReward     = 9,
    QuestlineUnlockPart = 10,
    Max
};
```

## QuestRewardContextFlags

[src/server/game/Quests/QuestDef.h:416](../../../src/server/game/Quests/QuestDef.h#L416)

```cpp
enum class QuestRewardContextFlags : int32
{
    None                    = 0x0,
    FirstCompletionBonus    = 0x1,
    RepeatCompletionBonus   = 0x2
};
```
