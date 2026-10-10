# World Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## LootModes

[src/server/game/Miscellaneous/SharedDefines.h:75](../../../src/server/game/Miscellaneous/SharedDefines.h#L75)

```cpp
enum LootModes
{
    LOOT_MODE_DEFAULT                  = 0x1,
    LOOT_MODE_HARD_MODE_1              = 0x2,
    LOOT_MODE_HARD_MODE_2              = 0x4,
    LOOT_MODE_HARD_MODE_3              = 0x8,
    LOOT_MODE_HARD_MODE_4              = 0x10,
    LOOT_MODE_JUNK_FISH                = 0x8000
};
```

## Gender

[src/server/game/Miscellaneous/SharedDefines.h:143](../../../src/server/game/Miscellaneous/SharedDefines.h#L143)

```cpp
enum Gender
{
    GENDER_UNKNOWN                     = -1,
    GENDER_MALE                        =  0,
    GENDER_FEMALE                      =  1,
    GENDER_NONE                        =  2
};
```

## ReputationRank

[src/server/game/Miscellaneous/SharedDefines.h:208](../../../src/server/game/Miscellaneous/SharedDefines.h#L208)

```cpp
enum ReputationRank
{
    REP_HATED       = 0,
    REP_HOSTILE     = 1,
    REP_UNFRIENDLY  = 2,
    REP_NEUTRAL     = 3,
    REP_FRIENDLY    = 4,
    REP_HONORED     = 5,
    REP_REVERED     = 6,
    REP_EXALTED     = 7
};
```

## SpellSchools

[src/server/game/Miscellaneous/SharedDefines.h:327](../../../src/server/game/Miscellaneous/SharedDefines.h#L327)

```cpp
enum SpellSchools : uint16
{
    SPELL_SCHOOL_NORMAL                 = 0, // TITLE Physical
    SPELL_SCHOOL_HOLY                   = 1, // TITLE Holy
    SPELL_SCHOOL_FIRE                   = 2, // TITLE Fire
    SPELL_SCHOOL_NATURE                 = 3, // TITLE Nature
    SPELL_SCHOOL_FROST                  = 4, // TITLE Frost
    SPELL_SCHOOL_SHADOW                 = 5, // TITLE Shadow
    SPELL_SCHOOL_ARCANE                 = 6, // TITLE Arcane
    MAX_SPELL_SCHOOL                    = 7  // SKIP
};
```

## SpellSchoolMask

[src/server/game/Miscellaneous/SharedDefines.h:339](../../../src/server/game/Miscellaneous/SharedDefines.h#L339)

```cpp
enum SpellSchoolMask : uint32
{
    SPELL_SCHOOL_MASK_NONE    = 0x00,                       // not exist
    SPELL_SCHOOL_MASK_NORMAL  = (1 << SPELL_SCHOOL_NORMAL), // PHYSICAL (Armor)
    SPELL_SCHOOL_MASK_HOLY    = (1 << SPELL_SCHOOL_HOLY),
    SPELL_SCHOOL_MASK_FIRE    = (1 << SPELL_SCHOOL_FIRE),
    SPELL_SCHOOL_MASK_NATURE  = (1 << SPELL_SCHOOL_NATURE),
    SPELL_SCHOOL_MASK_FROST   = (1 << SPELL_SCHOOL_FROST),
    SPELL_SCHOOL_MASK_SHADOW  = (1 << SPELL_SCHOOL_SHADOW),
    SPELL_SCHOOL_MASK_ARCANE  = (1 << SPELL_SCHOOL_ARCANE),

    // unions

    // 124, not include normal and holy damage
    SPELL_SCHOOL_MASK_SPELL   = (SPELL_SCHOOL_MASK_FIRE   |
                                  SPELL_SCHOOL_MASK_NATURE | SPELL_SCHOOL_MASK_FROST  |
                                  SPELL_SCHOOL_MASK_SHADOW | SPELL_SCHOOL_MASK_ARCANE),
    // 126
    SPELL_SCHOOL_MASK_MAGIC   = (SPELL_SCHOOL_MASK_HOLY | SPELL_SCHOOL_MASK_SPELL),

    // 127
    SPELL_SCHOOL_MASK_ALL     = (SPELL_SCHOOL_MASK_NORMAL | SPELL_SCHOOL_MASK_MAGIC)
};
```

## TeamId

[src/server/game/Miscellaneous/SharedDefines.h:1285](../../../src/server/game/Miscellaneous/SharedDefines.h#L1285)

```cpp
enum TeamId
{
    TEAM_ALLIANCE = 0,
    TEAM_HORDE,
    TEAM_NEUTRAL
};
```

## Team

[src/server/game/Miscellaneous/SharedDefines.h:1306](../../../src/server/game/Miscellaneous/SharedDefines.h#L1306)

```cpp
enum Team
{
    HORDE               = 67,
    ALLIANCE            = 469,
    PANDARIA_NEUTRAL    = 1249,                             // Starting pandas should have this team
    TEAM_OTHER          = 0                                 // if ReputationListId > 0 && Flags != FACTION_FLAG_TEAM_HEADER
};
```

## GameObjectFlags

[src/server/game/Miscellaneous/SharedDefines.h:3233](../../../src/server/game/Miscellaneous/SharedDefines.h#L3233)

```cpp
enum GameObjectFlags
{
    GO_FLAG_IN_USE                                  = 0x00000001, // disables interaction while animated
    GO_FLAG_LOCKED                                  = 0x00000002, // require key, spell, event, etc to be opened. Makes "Locked" appear in tooltip
    GO_FLAG_INTERACT_COND                           = 0x00000004, // cannot interact (condition to interact - requires GO_DYNFLAG_LO_ACTIVATE to enable interaction clientside)
    GO_FLAG_TRANSPORT                               = 0x00000008, // any kind of transport? Object can transport (elevator, boat, car)
    GO_FLAG_NOT_SELECTABLE                          = 0x00000010, // not selectable even in GM mode
    GO_FLAG_NODESPAWN                               = 0x00000020, // never despawn, typically for doors, they just change state
    GO_FLAG_AI_OBSTACLE                             = 0x00000040, // makes the client register the object in something called AIObstacleMgr, unknown what it does
    GO_FLAG_FREEZE_ANIMATION                        = 0x00000080,

    // for object types GAMEOBJECT_TYPE_GARRISON_BUILDING, GAMEOBJECT_TYPE_GARRISON_PLOT and GAMEOBJECT_TYPE_PHASEABLE_MO flag bits 8 to 12 are used as WMOAreaTable::NameSetID
    GO_FLAG_DAMAGED                                 = 0x00000200,
    GO_FLAG_DESTROYED                               = 0x00000400,

    GO_FLAG_IGNORE_CURRENT_STATE_FOR_USE_SPELL      = 0x00004000, // Allows casting use spell without checking current state (opening open gameobjects, unlocking unlocked gameobjects and closing closed gameobjects)
    GO_FLAG_INTERACT_DISTANCE_IGNORES_MODEL         = 0x00008000, // Client completely ignores model bounds for interaction distance check
    GO_FLAG_IGNORE_CURRENT_STATE_FOR_USE_SPELL_EXCEPT_UNLOCKED = 0x00040000, // Allows casting use spell without checking current state except unlocking unlocked gamobjets (opening open gameobjects and closing closed gameobjects)
    GO_FLAG_INTERACT_DISTANCE_USES_TEMPLATE_MODEL   = 0x00080000, // client checks interaction distance from model sent in SMSG_QUERY_GAMEOBJECT_RESPONSE instead of GAMEOBJECT_DISPLAYID
    GO_FLAG_MAP_OBJECT                              = 0x00100000, // pre-7.0 model loading used to be controlled by file extension (wmo vs m2)
    GO_FLAG_IN_MULTI_USE                            = 0x00200000, // GO_FLAG_IN_USE equivalent for objects usable by multiple players
    GO_FLAG_LOW_PRIORITY_SELECTION                  = 0x04000000, // client will give lower cursor priority to this object when multiple objects overlap
};
```

## GameObjectDynamicLowFlags

[src/server/game/Miscellaneous/SharedDefines.h:3259](../../../src/server/game/Miscellaneous/SharedDefines.h#L3259)

```cpp
enum GameObjectDynamicLowFlags : uint16
{
    GO_DYNFLAG_LO_HIDE_MODEL        = 0x0002,               // Object model is not shown with this flag
    GO_DYNFLAG_LO_ACTIVATE          = 0x0004,               // enables interaction with GO
    GO_DYNFLAG_LO_ANIMATE           = 0x0008,               // possibly more distinct animation of GO
    GO_DYNFLAG_LO_DEPLETED          = 0x0010,               // can no longer be interacted with (and for gathering nodes it forces "open" visual state)
    GO_DYNFLAG_LO_SPARKLE           = 0x0020,               // makes GO sparkle
    GO_DYNFLAG_LO_STOPPED           = 0x0040,               // Transport is stopped
    GO_DYNFLAG_LO_NO_INTERACT       = 0x0080,
    GO_DYNFLAG_LO_INVERTED_MOVEMENT = 0x0100,               // GAMEOBJECT_TYPE_TRANSPORT only
    GO_DYNFLAG_LO_INTERACT_COND     = 0x0200,               // Cannot interact (requires GO_DYNFLAG_LO_ACTIVATE to enable interaction clientside)
    GO_DYNFLAG_LO_HIGHLIGHT         = 0x4000,               // Allows object highlight when GO_DYNFLAG_LO_ACTIVATE are set, not only when player is on quest determined by Data fields
    GO_DYNFLAG_LO_STATE_TRANSITION_ANIM_DONE = 0x8000,      // don't play state transition anim on entering visibility
};
```

## GameObjectDestructibleState

[src/server/game/Miscellaneous/SharedDefines.h:3287](../../../src/server/game/Miscellaneous/SharedDefines.h#L3287)

```cpp
enum GameObjectDestructibleState
{
    GO_DESTRUCTIBLE_INTACT      = 0,
    GO_DESTRUCTIBLE_DAMAGED     = 1,
    GO_DESTRUCTIBLE_DESTROYED   = 2,
    GO_DESTRUCTIBLE_REBUILDING  = 3
};
```

## CreatureType

[src/server/game/Miscellaneous/SharedDefines.h:5016](../../../src/server/game/Miscellaneous/SharedDefines.h#L5016)

```cpp
enum CreatureType
{
    CREATURE_TYPE_BEAST            = 1,
    CREATURE_TYPE_DRAGONKIN        = 2,
    CREATURE_TYPE_DEMON            = 3,
    CREATURE_TYPE_ELEMENTAL        = 4,
    CREATURE_TYPE_GIANT            = 5,
    CREATURE_TYPE_UNDEAD           = 6,
    CREATURE_TYPE_HUMANOID         = 7,
    CREATURE_TYPE_CRITTER          = 8,
    CREATURE_TYPE_MECHANICAL       = 9,
    CREATURE_TYPE_NOT_SPECIFIED    = 10,
    CREATURE_TYPE_TOTEM            = 11,
    CREATURE_TYPE_NON_COMBAT_PET   = 12,
    CREATURE_TYPE_GAS_CLOUD        = 13,
    CREATURE_TYPE_WILD_PET         = 14,
    CREATURE_TYPE_ABERRATION       = 15
};
```

## CreatureFamily

[src/server/game/Miscellaneous/SharedDefines.h:5040](../../../src/server/game/Miscellaneous/SharedDefines.h#L5040)

```cpp
enum CreatureFamily
{
    CREATURE_FAMILY_NONE                = 0,
    CREATURE_FAMILY_WOLF                = 1,
    CREATURE_FAMILY_CAT                 = 2,
    CREATURE_FAMILY_SPIDER              = 3,
    CREATURE_FAMILY_BEAR                = 4,
    CREATURE_FAMILY_BOAR                = 5,
    CREATURE_FAMILY_CROCOLISK           = 6,
    CREATURE_FAMILY_CARRION_BIRD        = 7,
    CREATURE_FAMILY_CRAB                = 8,
    CREATURE_FAMILY_GORILLA             = 9,
    CREATURE_FAMILY_RAPTOR              = 11,
    CREATURE_FAMILY_TALLSTRIDER         = 12,
    CREATURE_FAMILY_FELHUNTER           = 15,
    CREATURE_FAMILY_VOIDWALKER          = 16,
    CREATURE_FAMILY_SUCCUBUS            = 17,
    CREATURE_FAMILY_DOOMGUARD           = 19,
    CREATURE_FAMILY_SCORPID             = 20,
    CREATURE_FAMILY_TURTLE              = 21,
    CREATURE_FAMILY_IMP                 = 23,
    CREATURE_FAMILY_BAT                 = 24,
    CREATURE_FAMILY_HYENA               = 25,
    CREATURE_FAMILY_BIRD_OF_PREY        = 26,
    CREATURE_FAMILY_WIND_SERPENT        = 27,
    CREATURE_FAMILY_REMOTE_CONTROL      = 28,
    CREATURE_FAMILY_FELGUARD            = 29,
    CREATURE_FAMILY_DRAGONHAWK          = 30,
    CREATURE_FAMILY_RAVAGER             = 31,
    CREATURE_FAMILY_WARP_STALKER        = 32,
    CREATURE_FAMILY_SPOREBAT            = 33,
    CREATURE_FAMILY_RAY                 = 34,
    CREATURE_FAMILY_SERPENT             = 35,
    CREATURE_FAMILY_MOTH                = 37,
    CREATURE_FAMILY_CHIMAERA            = 38,
    CREATURE_FAMILY_DEVILSAUR           = 39,
    CREATURE_FAMILY_GHOUL               = 40,
    CREATURE_FAMILY_AQIRI               = 41,
    CREATURE_FAMILY_WORM                = 42,
    CREATURE_FAMILY_CLEFTHOOF           = 43,
    CREATURE_FAMILY_WASP                = 44,
    CREATURE_FAMILY_CORE_HOUND          = 45,
    CREATURE_FAMILY_SPIRIT_BEAST        = 46,
    CREATURE_FAMILY_WATER_ELEMENTAL     = 49,
    CREATURE_FAMILY_FOX                 = 50,
    CREATURE_FAMILY_MONKEY              = 51,
    CREATURE_FAMILY_HOUND               = 52,
    CREATURE_FAMILY_BEETLE              = 53,
    CREATURE_FAMILY_SHALE_BEAST         = 55,
    CREATURE_FAMILY_ZOMBIE              = 56,
    CREATURE_FAMILY_QA_TEST             = 57,
    CREATURE_FAMILY_HYDRA               = 68,
    CREATURE_FAMILY_FELIMP              = 100,
    CREATURE_FAMILY_VOIDLORD            = 101,
    CREATURE_FAMILY_SHIVARRA            = 102,
    CREATURE_FAMILY_OBSERVER            = 103,
    CREATURE_FAMILY_WRATHGUARD          = 104,
    CREATURE_FAMILY_INFERNAL            = 108,
    CREATURE_FAMILY_FIREELEMENTAL       = 116,
    CREATURE_FAMILY_EARTHELEMENTAL      = 117,
    CREATURE_FAMILY_WATERFOWL           = 125,
    CREATURE_FAMILY_WATERSTRIDER        = 126,
    CREATURE_FAMILY_RODENT              = 127,
    CREATURE_FAMILY_STONE_HOUND         = 128,
    CREATURE_FAMILY_GRUFFHORN           = 129,
    CREATURE_FAMILY_BASILISK            = 130,
    CREATURE_FAMILY_DIREHORN            = 138,
    CREATURE_FAMILY_STORMELEMENTAL      = 145,
    CREATURE_FAMILY_TERRORGUARD         = 147,
    CREATURE_FAMILY_ABYSSAL             = 148,
    CREATURE_FAMILY_RIVERBEAST          = 150,
    CREATURE_FAMILY_STAG                = 151,
    CREATURE_FAMILY_MECHANICAL          = 154,
    CREATURE_FAMILY_ABOMINATION         = 155,
    CREATURE_FAMILY_SCALEHIDE           = 156,
    CREATURE_FAMILY_OXEN                = 157,
    CREATURE_FAMILY_FEATHERMANE         = 160,
    CREATURE_FAMILY_LIZARD              = 288,
    CREATURE_FAMILY_PTERRORDAX          = 290,
    CREATURE_FAMILY_HOPPER              = 291,
    CREATURE_FAMILY_CARAPID             = 292,
    CREATURE_FAMILY_BLOOD_BEAST         = 296,
    CREATURE_FAMILY_CAMEL               = 298,
    CREATURE_FAMILY_COURSER             = 299,
    CREATURE_FAMILY_MAMMOTH             = 300,
    CREATURE_FAMILY_INCUBUS             = 302,
    CREATURE_FAMILY_LESSER_DRAGONKIN    = 303,
    CREATURE_FAMILY_WHIPTAIL            = 315
};
```

## CreatureTypeFlags

[src/server/game/Miscellaneous/SharedDefines.h:5130](../../../src/server/game/Miscellaneous/SharedDefines.h#L5130)

```cpp
enum CreatureTypeFlags
{
    CREATURE_TYPE_FLAG_TAMEABLE                          = 0x00000001, // Makes the mob tameable (must also be a beast and have family set)
    CREATURE_TYPE_FLAG_VISIBLE_TO_GHOSTS                 = 0x00000002, // Creature is also visible for not alive player. Allows gossip interaction if npcflag allows?
    CREATURE_TYPE_FLAG_BOSS_MOB                          = 0x00000004, // Changes creature's visible level to "??" in the creature's portrait
    CREATURE_TYPE_FLAG_DO_NOT_PLAY_WOUND_ANIM            = 0x00000008,
    CREATURE_TYPE_FLAG_NO_FACTION_TOOLTIP                = 0x00000010,
    CREATURE_TYPE_FLAG_MORE_AUDIBLE                      = 0x00000020, // Sound related
    CREATURE_TYPE_FLAG_SPELL_ATTACKABLE                  = 0x00000040,
    CREATURE_TYPE_FLAG_INTERACT_WHILE_DEAD               = 0x00000080, // Player can interact with the creature if creature is dead (not if player is dead)
    CREATURE_TYPE_FLAG_SKIN_WITH_HERBALISM               = 0x00000100, // Can be looted by herbalist
    CREATURE_TYPE_FLAG_SKIN_WITH_MINING                  = 0x00000200, // Can be looted by miner
    CREATURE_TYPE_FLAG_NO_DEATH_MESSAGE                  = 0x00000400, // Death event will not show up in combat log
    CREATURE_TYPE_FLAG_ALLOW_MOUNTED_COMBAT              = 0x00000800, // Creature can remain mounted when entering combat
    CREATURE_TYPE_FLAG_CAN_ASSIST                        = 0x00001000, // ? Can aid any player in combat if in range?
    CREATURE_TYPE_FLAG_NO_PET_BAR                        = 0x00002000,
    CREATURE_TYPE_FLAG_MASK_UID                          = 0x00004000,
    CREATURE_TYPE_FLAG_SKIN_WITH_ENGINEERING             = 0x00008000, // Can be looted by engineer
    CREATURE_TYPE_FLAG_TAMEABLE_EXOTIC                   = 0x00010000, // Can be tamed by hunter as exotic pet
    CREATURE_TYPE_FLAG_USE_MODEL_COLLISION_SIZE          = 0x00020000, // Collision related. (always using default collision box?)
    CREATURE_TYPE_FLAG_ALLOW_INTERACTION_WHILE_IN_COMBAT = 0x00040000,
    CREATURE_TYPE_FLAG_COLLIDE_WITH_MISSILES             = 0x00080000, // Projectiles can collide with this creature - interacts with TARGET_DEST_TRAJ
    CREATURE_TYPE_FLAG_NO_NAME_PLATE                     = 0x00100000,
    CREATURE_TYPE_FLAG_DO_NOT_PLAY_MOUNTED_ANIMATIONS    = 0x00200000,
    CREATURE_TYPE_FLAG_LINK_ALL                          = 0x00400000,
    CREATURE_TYPE_FLAG_INTERACT_ONLY_WITH_CREATOR        = 0x00800000,
    CREATURE_TYPE_FLAG_DO_NOT_PLAY_UNIT_EVENT_SOUNDS     = 0x01000000,
    CREATURE_TYPE_FLAG_HAS_NO_SHADOW_BLOB                = 0x02000000,
    CREATURE_TYPE_FLAG_TREAT_AS_RAID_UNIT                = 0x04000000, //!< Creature can be targeted by spells that require target to be in caster's party/raid
    CREATURE_TYPE_FLAG_FORCE_GOSSIP                      = 0x08000000, // Allows the creature to display a single gossip option.
    CREATURE_TYPE_FLAG_DO_NOT_SHEATHE                    = 0x10000000,
    CREATURE_TYPE_FLAG_DO_NOT_TARGET_ON_INTERACTION      = 0x20000000,
    CREATURE_TYPE_FLAG_DO_NOT_RENDER_OBJECT_NAME         = 0x40000000,
    CREATURE_TYPE_FLAG_QUEST_BOSS                        = 0x80000000  // Not verified
};
```

## CreatureTypeFlags2

[src/server/game/Miscellaneous/SharedDefines.h:5166](../../../src/server/game/Miscellaneous/SharedDefines.h#L5166)

```cpp
enum CreatureTypeFlags2
{
    CREATURE_TYPE_FLAG_2_PREDICTIVE_POWER_REGEN          = 0x00000001,
    CREATURE_TYPE_FLAG_2_HIDE_LEVEL_INFO_IN_TOOLTIP      = 0x00000002,
    CREATURE_TYPE_FLAG_2_HIDE_HEALTH_BAR_UNDER_TOOLTIP   = 0x00000004,
    CREATURE_TYPE_FLAG_2_NEVER_DISPLAY_EMOTE_OR_CHAT_TEXT_IN_A_CHAT_BUBBLE = 0x00000008,
    CREATURE_TYPE_FLAG_2_NO_DEATH_THUD = 0x00000010,
    CREATURE_TYPE_FLAG_2_NO_INTERACT_ON_LEFT_CLICK = 0x00000020,
    CREATURE_TYPE_FLAG_2_UNK7 = 0x00000040,
    CREATURE_TYPE_FLAG_2_UNK8 = 0x00000080
};
```

## CreatureClassifications

[src/server/game/Miscellaneous/SharedDefines.h:5178](../../../src/server/game/Miscellaneous/SharedDefines.h#L5178)

```cpp
enum class CreatureClassifications : uint32
{
    Normal                    = 0,
    Elite                     = 1,
    RareElite                 = 2,
    Obsolete                  = 3,
    Rare                      = 4,
    Trivial                   = 5,
    MinusMob                  = 6
};
```

## PvPTeamId

[src/server/game/Miscellaneous/SharedDefines.h:6913](../../../src/server/game/Miscellaneous/SharedDefines.h#L6913)

```cpp
enum PvPTeamId : uint8
{
    PVP_TEAM_HORDE       = 0, // Battleground: Horde,    Arena: Green
    PVP_TEAM_ALLIANCE    = 1, // Battleground: Alliance, Arena: Gold
    PVP_TEAM_NEUTRAL     = 2  // Battleground: Neutral,  Arena: None
};
```

## UnitFlags

[src/server/game/Entities/Unit/UnitDefines.h:165](../../../src/server/game/Entities/Unit/UnitDefines.h#L165)

```cpp
enum UnitFlags : uint32
{
    UNIT_FLAG_SERVER_CONTROLLED     = 0x00000001,           // set only when unit movement is controlled by server - by SPLINE/MONSTER_MOVE packets, together with UNIT_FLAG_STUNNED; only set to units controlled by client; client function CGUnit_C::IsClientControlled returns false when set for owner
    UNIT_FLAG_NON_ATTACKABLE        = 0x00000002,           // not attackable, set when creature starts to cast spells with SPELL_EFFECT_SPAWN and cast time, removed when spell hits caster, original name is UNIT_FLAG_SPAWNING. Rename when it will be removed from all scripts
    UNIT_FLAG_REMOVE_CLIENT_CONTROL = 0x00000004,           // This is a legacy flag used to disable movement player's movement while controlling other units, SMSG_CLIENT_CONTROL replaces this functionality clientside now. CONFUSED and FLEEING flags have the same effect on client movement asDISABLE_MOVE_CONTROL in addition to preventing spell casts/autoattack (they all allow climbing steeper hills and emotes while moving)
    UNIT_FLAG_PLAYER_CONTROLLED     = 0x00000008,           // controlled by player, use _IMMUNE_TO_PC instead of _IMMUNE_TO_NPC
    UNIT_FLAG_RENAME                = 0x00000010,
    UNIT_FLAG_PREPARATION           = 0x00000020,           // don't take reagents for spells with SPELL_ATTR5_NO_REAGENT_WHILE_PREP
    UNIT_FLAG_UNK_6                 = 0x00000040,
    UNIT_FLAG_NOT_ATTACKABLE_1      = 0x00000080,           // ?? (UNIT_FLAG_PLAYER_CONTROLLED | UNIT_FLAG_NOT_ATTACKABLE_1) is NON_PVP_ATTACKABLE
    UNIT_FLAG_IMMUNE_TO_PC          = 0x00000100,           // disables combat/assistance with PlayerCharacters (PC) - see Unit::IsValidAttackTarget, Unit::IsValidAssistTarget
    UNIT_FLAG_IMMUNE_TO_NPC         = 0x00000200,           // disables combat/assistance with NonPlayerCharacters (NPC) - see Unit::IsValidAttackTarget, Unit::IsValidAssistTarget
    UNIT_FLAG_LOOTING               = 0x00000400,           // loot animation
    UNIT_FLAG_PET_IN_COMBAT         = 0x00000800,           // on player pets: whether the pet is chasing a target to attack || on other units: whether any of the unit's minions is in combat
    UNIT_FLAG_PVP_ENABLING          = 0x00001000,           // changed in 3.0.3, now UNIT_BYTES_2_OFFSET_PVP_FLAG from UNIT_FIELD_BYTES_2
    UNIT_FLAG_FORCE_NAMEPLATE       = 0x00002000,           // Force show nameplate, 9.0
    UNIT_FLAG_CANT_SWIM             = 0x00004000,           // TITLE Can't Swim
    UNIT_FLAG_CAN_SWIM              = 0x00008000,           // TITLE Can Swim DESCRIPTION shows swim animation in water
    UNIT_FLAG_NON_ATTACKABLE_2      = 0x00010000,           // removes attackable icon, if on yourself, cannot assist self but can cast TARGET_SELF spells - added by SPELL_AURA_MOD_UNATTACKABLE
    UNIT_FLAG_PACIFIED              = 0x00020000,           // 3.0.3 ok
    UNIT_FLAG_STUNNED               = 0x00040000,           // 3.0.3 ok
    UNIT_FLAG_IN_COMBAT             = 0x00080000,
    UNIT_FLAG_ON_TAXI               = 0x00100000,           // disable casting at client side spell not allowed by taxi flight (mounted?), probably used with 0x4 flag
    UNIT_FLAG_DISARMED              = 0x00200000,           // 3.0.3, disable melee spells casting..., "Required melee weapon" added to melee spells tooltip.
    UNIT_FLAG_CONFUSED              = 0x00400000,
    UNIT_FLAG_FLEEING               = 0x00800000,
    UNIT_FLAG_POSSESSED             = 0x01000000,           // under direct client control by a player (possess or vehicle)
    UNIT_FLAG_UNINTERACTIBLE        = 0x02000000,
    UNIT_FLAG_SKINNABLE             = 0x04000000,
    UNIT_FLAG_MOUNT                 = 0x08000000,
    UNIT_FLAG_UNK_28                = 0x10000000,
    UNIT_FLAG_PREVENT_EMOTES_FROM_CHAT_TEXT = 0x20000000,   // Prevent automatically playing emotes from parsing chat text, for example "lol" in /say, ending message with ? or !, or using /yell
    UNIT_FLAG_SHEATHE               = 0x40000000,
    UNIT_FLAG_IMMUNE                = 0x80000000,           // Immune to damage

    UNIT_FLAG_DISALLOWED            = (UNIT_FLAG_SERVER_CONTROLLED | UNIT_FLAG_NON_ATTACKABLE | UNIT_FLAG_REMOVE_CLIENT_CONTROL |
                                       UNIT_FLAG_PLAYER_CONTROLLED | UNIT_FLAG_RENAME | UNIT_FLAG_PREPARATION | /* UNIT_FLAG_UNK_6 | */
                                       UNIT_FLAG_NOT_ATTACKABLE_1 | UNIT_FLAG_LOOTING | UNIT_FLAG_PET_IN_COMBAT | UNIT_FLAG_PVP_ENABLING |
                                       UNIT_FLAG_CANT_SWIM | UNIT_FLAG_CAN_SWIM | UNIT_FLAG_NON_ATTACKABLE_2 | UNIT_FLAG_PACIFIED | UNIT_FLAG_STUNNED |
                                       UNIT_FLAG_IN_COMBAT | UNIT_FLAG_ON_TAXI | UNIT_FLAG_DISARMED | UNIT_FLAG_CONFUSED | UNIT_FLAG_FLEEING |
                                       UNIT_FLAG_POSSESSED | UNIT_FLAG_SKINNABLE | UNIT_FLAG_MOUNT | UNIT_FLAG_UNK_28 |
                                       UNIT_FLAG_PREVENT_EMOTES_FROM_CHAT_TEXT | UNIT_FLAG_SHEATHE | UNIT_FLAG_IMMUNE), // SKIP

    UNIT_FLAG_ALLOWED               = (0xFFFFFFFF & ~UNIT_FLAG_DISALLOWED) // SKIP
};
```

## UnitFlags2

[src/server/game/Entities/Unit/UnitDefines.h:215](../../../src/server/game/Entities/Unit/UnitDefines.h#L215)

```cpp
enum UnitFlags2 : uint32
{
    UNIT_FLAG2_FEIGN_DEATH                                      = 0x00000001,
    UNIT_FLAG2_HIDE_BODY                                        = 0x00000002,   // TITLE Hide Body DESCRIPTION Hide unit model (show only player equip)
    UNIT_FLAG2_IGNORE_REPUTATION                                = 0x00000004,
    UNIT_FLAG2_COMPREHEND_LANG                                  = 0x00000008,
    UNIT_FLAG2_MIRROR_IMAGE                                     = 0x00000010,
    UNIT_FLAG2_DONT_FADE_IN                                     = 0x00000020,   // TITLE Don't Fade In DESCRIPTION Unit model instantly appears when summoned (does not fade in)
    UNIT_FLAG2_FORCE_MOVEMENT                                   = 0x00000040,
    UNIT_FLAG2_DISARM_OFFHAND                                   = 0x00000080,
    UNIT_FLAG2_DISABLE_PRED_STATS                               = 0x00000100,   // Player has disabled predicted stats (Used by raid frames)
    UNIT_FLAG2_ALLOW_CHANGING_TALENTS                           = 0x00000200,   // Allows changing talents outside rest area
    UNIT_FLAG2_DISARM_RANGED                                    = 0x00000400,   // this does not disable ranged weapon display (maybe additional flag needed?)
    UNIT_FLAG2_REGENERATE_POWER                                 = 0x00000800,
    UNIT_FLAG2_RESTRICT_PARTY_INTERACTION                       = 0x00001000,   // Restrict interaction to party or raid
    UNIT_FLAG2_PREVENT_SPELL_CLICK                              = 0x00002000,   // Prevent spellclick
    UNIT_FLAG2_INTERACT_WHILE_HOSTILE                           = 0x00004000,   // TITLE Interact while Hostile
    UNIT_FLAG2_CANNOT_TURN                                      = 0x00008000,   // TITLE Cannot Turn
    UNIT_FLAG2_UNK2                                             = 0x00010000,
    UNIT_FLAG2_PLAY_DEATH_ANIM                                  = 0x00020000,   // Plays special death animation upon death
    UNIT_FLAG2_ALLOW_CHEAT_SPELLS                               = 0x00040000,   // Allows casting spells with AttributesEx7 & SPELL_ATTR7_IS_CHEAT_SPELL
    UNIT_FLAG2_SUPPRESS_HIGHLIGHT_WHEN_TARGETED_OR_MOUSED_OVER  = 0x00080000,   // TITLE Suppress highlight when targeted or moused over
    UNIT_FLAG2_TREAT_AS_RAID_UNIT_FOR_HELPFUL_SPELLS            = 0x00100000,   // TITLE Treat as Raid Unit For Helpful Spells (Instances ONLY)
    UNIT_FLAG2_LARGE_AOI                                        = 0x00200000,   // TITLE Large (AOI)
    UNIT_FLAG2_GIGANTIC_AOI                                     = 0x00400000,   // TITLE Gigantic (AOI)
    UNIT_FLAG2_NO_ACTIONS                                       = 0x00800000,
    UNIT_FLAG2_AI_WILL_ONLY_SWIM_IF_TARGET_SWIMS                = 0x01000000,   // TITLE AI will only swim if target swims
    UNIT_FLAG2_DONT_GENERATE_COMBAT_LOG_WHEN_ENGAGED_WITH_NPCS  = 0x02000000,   // TITLE Don't generate combat log when engaged with NPC's
    UNIT_FLAG2_UNTARGETABLE_BY_CLIENT                           = 0x04000000,   // TITLE Untargetable By Client
    UNIT_FLAG2_ATTACKER_IGNORES_MINIMUM_RANGES                  = 0x08000000,   // TITLE Attacker Ignores Minimum Ranges
    UNIT_FLAG2_UNINTERACTIBLE_IF_HOSTILE                        = 0x10000000,   // TITLE Uninteractible If Hostile
    UNIT_FLAG2_UNUSED_11                                        = 0x20000000,
    UNIT_FLAG2_INFINITE_AOI                                     = 0x40000000,   // TITLE Infinite (AOI)
    UNIT_FLAG2_UNUSED_13                                        = 0x80000000,

    UNIT_FLAG2_DISALLOWED                                       = (/* UNIT_FLAG2_FEIGN_DEATH | */ UNIT_FLAG2_IGNORE_REPUTATION | UNIT_FLAG2_COMPREHEND_LANG |
                                                                   UNIT_FLAG2_MIRROR_IMAGE | UNIT_FLAG2_FORCE_MOVEMENT | UNIT_FLAG2_DISARM_OFFHAND |
                                                                   UNIT_FLAG2_DISABLE_PRED_STATS | UNIT_FLAG2_ALLOW_CHANGING_TALENTS | UNIT_FLAG2_DISARM_RANGED |
                                                                /* UNIT_FLAG2_REGENERATE_POWER | */ UNIT_FLAG2_RESTRICT_PARTY_INTERACTION | UNIT_FLAG2_CANNOT_TURN |
                                                                   UNIT_FLAG2_PREVENT_SPELL_CLICK | /* UNIT_FLAG2_INTERACT_WHILE_HOSTILE | */ /* UNIT_FLAG2_UNK2 | */
                                                                /* UNIT_FLAG2_PLAY_DEATH_ANIM | */ UNIT_FLAG2_ALLOW_CHEAT_SPELLS | UNIT_FLAG2_SUPPRESS_HIGHLIGHT_WHEN_TARGETED_OR_MOUSED_OVER |
                                                                   UNIT_FLAG2_TREAT_AS_RAID_UNIT_FOR_HELPFUL_SPELLS | UNIT_FLAG2_LARGE_AOI | UNIT_FLAG2_GIGANTIC_AOI | UNIT_FLAG2_NO_ACTIONS |
                                                                   UNIT_FLAG2_AI_WILL_ONLY_SWIM_IF_TARGET_SWIMS | UNIT_FLAG2_DONT_GENERATE_COMBAT_LOG_WHEN_ENGAGED_WITH_NPCS | UNIT_FLAG2_ATTACKER_IGNORES_MINIMUM_RANGES |
                                                                   UNIT_FLAG2_UNINTERACTIBLE_IF_HOSTILE | UNIT_FLAG2_UNUSED_11 | UNIT_FLAG2_INFINITE_AOI | UNIT_FLAG2_UNUSED_13),  // SKIP

    UNIT_FLAG2_ALLOWED                                          = (0xFFFFFFFF & ~UNIT_FLAG2_DISALLOWED) // SKIP
};
```

## UnitFlags3

[src/server/game/Entities/Unit/UnitDefines.h:267](../../../src/server/game/Entities/Unit/UnitDefines.h#L267)

```cpp
enum UnitFlags3 : uint32
{
    UNIT_FLAG3_UNK0                                         = 0x00000001,
    UNIT_FLAG3_UNCONSCIOUS_ON_DEATH                         = 0x00000002,   // TITLE Unconscious on Death DESCRIPTION Shows "Unconscious" in unit tooltip instead of "Dead"
    UNIT_FLAG3_ALLOW_MOUNTED_COMBAT                         = 0x00000004,   // TITLE Allow mounted combat
    UNIT_FLAG3_GARRISON_PET                                 = 0x00000008,   // TITLE Garrison pet DESCRIPTION Special garrison pet creatures that display one of favorite player battle pets - this flag allows querying name and turns off default battle pet behavior
    UNIT_FLAG3_UI_CAN_GET_POSITION                          = 0x00000010,   // TITLE UI Can Get Position DESCRIPTION Allows lua functions like UnitPosition to always get the position even for npcs or non-grouped players
    UNIT_FLAG3_AI_OBSTACLE                                  = 0x00000020,
    UNIT_FLAG3_ALTERNATIVE_DEFAULT_LANGUAGE                 = 0x00000040,
    UNIT_FLAG3_SUPPRESS_ALL_NPC_FEEDBACK                    = 0x00000080,   // TITLE Suppress all NPC feedback DESCRIPTION Skips playing sounds on left clicking npc for all npcs as long as npc with this flag is visible
    UNIT_FLAG3_IGNORE_COMBAT                                = 0x00000100,   // TITLE Ignore Combat DESCRIPTION Same as SPELL_AURA_IGNORE_COMBAT
    UNIT_FLAG3_SUPPRESS_NPC_FEEDBACK                        = 0x00000200,   // TITLE Suppress NPC feedback DESCRIPTION Skips playing sounds on left clicking npc
    UNIT_FLAG3_UNK10                                        = 0x00000400,
    UNIT_FLAG3_UNK11                                        = 0x00000800,
    UNIT_FLAG3_UNK12                                        = 0x00001000,
    UNIT_FLAG3_FAKE_DEAD                                    = 0x00002000,   // TITLE Show as dead
    UNIT_FLAG3_NO_FACING_ON_INTERACT_AND_FAST_FACING_CHASE  = 0x00004000,   // Causes the creature to both not change facing on interaction and speeds up smooth facing changes while attacking (clientside)
    UNIT_FLAG3_UNTARGETABLE_FROM_UI                         = 0x00008000,   // TITLE Untargetable from UI DESCRIPTION Cannot be targeted from lua functions StartAttack, TargetUnit, PetAttack
    UNIT_FLAG3_NO_FACING_ON_INTERACT_WHILE_FAKE_DEAD        = 0x00010000,   // Prevents facing changes while interacting if creature has flag UNIT_FLAG3_FAKE_DEAD
    UNIT_FLAG3_ALREADY_SKINNED                              = 0x00020000,
    UNIT_FLAG3_SUPPRESS_ALL_NPC_SOUNDS                      = 0x00040000,   // TITLE Suppress all NPC sounds DESCRIPTION Skips playing sounds on beginning and end of npc interaction for all npcs as long as npc with this flag is visible
    UNIT_FLAG3_SUPPRESS_NPC_SOUNDS                          = 0x00080000,   // TITLE Suppress NPC sounds DESCRIPTION Skips playing sounds on beginning and end of npc interaction
    UNIT_FLAG3_ALLOW_INTERACTION_WHILE_IN_COMBAT            = 0x00100000,   // TITLE Allow Interaction While in Combat DESCRIPTION Allows using various NPC functions while in combat (vendor, gossip, questgiver)
    UNIT_FLAG3_UNK21                                        = 0x00200000,
    UNIT_FLAG3_DONT_FADE_OUT                                = 0x00400000,
    UNIT_FLAG3_UNK23                                        = 0x00800000,
    UNIT_FLAG3_FORCE_HIDE_NAMEPLATE                         = 0x01000000,
    UNIT_FLAG3_UNK25                                        = 0x02000000,
    UNIT_FLAG3_UNK26                                        = 0x04000000,
    UNIT_FLAG3_UNK27                                        = 0x08000000,
    UNIT_FLAG3_UNK28                                        = 0x10000000,
    UNIT_FLAG3_UNK29                                        = 0x20000000,
    UNIT_FLAG3_UNK30                                        = 0x40000000,
    UNIT_FLAG3_UNK31                                        = 0x80000000,

    UNIT_FLAG3_DISALLOWED                                   = (UNIT_FLAG3_UNK0 | /* UNIT_FLAG3_UNCONSCIOUS_ON_DEATH | */ /* UNIT_FLAG3_ALLOW_MOUNTED_COMBAT | */ UNIT_FLAG3_GARRISON_PET |
                                                               /* UNIT_FLAG3_UI_CAN_GET_POSITION | */ /* UNIT_FLAG3_AI_OBSTACLE | */ UNIT_FLAG3_ALTERNATIVE_DEFAULT_LANGUAGE | /* UNIT_FLAG3_SUPPRESS_ALL_NPC_FEEDBACK | */
                                                               UNIT_FLAG3_IGNORE_COMBAT | UNIT_FLAG3_SUPPRESS_NPC_FEEDBACK | UNIT_FLAG3_UNK10 | UNIT_FLAG3_UNK11 |
                                                               UNIT_FLAG3_UNK12 | /* UNIT_FLAG3_FAKE_DEAD |*/ /* UNIT_FLAG3_NO_FACING_ON_INTERACT_AND_FAST_FACING_CHASE | */ /* UNIT_FLAG3_UNTARGETABLE_FROM_UI | */
                                                               /* UNIT_FLAG3_NO_FACING_ON_INTERACT_WHILE_FAKE_DEAD | */ UNIT_FLAG3_ALREADY_SKINNED | /* UNIT_FLAG3_SUPPRESS_ALL_NPC_SOUNDS | */ /* UNIT_FLAG3_SUPPRESS_NPC_SOUNDS | */
                                                               UNIT_FLAG3_ALLOW_INTERACTION_WHILE_IN_COMBAT | UNIT_FLAG3_UNK21 | /* UNIT_FLAG3_DONT_FADE_OUT | */ UNIT_FLAG3_UNK23 |
                                                               /* UNIT_FLAG3_FORCE_HIDE_NAMEPLATE | */ UNIT_FLAG3_UNK25 | UNIT_FLAG3_UNK26 | UNIT_FLAG3_UNK27 |
                                                               UNIT_FLAG3_UNK28 | UNIT_FLAG3_UNK29 | UNIT_FLAG3_UNK30 | UNIT_FLAG3_UNK31), // SKIP
    UNIT_FLAG3_ALLOWED                                      = (0xFFFFFFFF & ~UNIT_FLAG3_DISALLOWED) // SKIP
};
```

## NPCFlags

[src/server/game/Entities/Unit/UnitDefines.h:317](../../../src/server/game/Entities/Unit/UnitDefines.h#L317)

```cpp
enum NPCFlags : uint32
{
    UNIT_NPC_FLAG_NONE                  = 0x00000000,
    UNIT_NPC_FLAG_GOSSIP                = 0x00000001,     // TITLE has gossip menu DESCRIPTION 100%
    UNIT_NPC_FLAG_QUESTGIVER            = 0x00000002,     // TITLE is quest giver DESCRIPTION 100%
    UNIT_NPC_FLAG_ACCOUNT_BANKER        = 0x00000004,     // TITLE is account banker
    UNIT_NPC_FLAG_UNK2                  = 0x00000008,
    UNIT_NPC_FLAG_TRAINER               = 0x00000010,     // TITLE is trainer DESCRIPTION 100%
    UNIT_NPC_FLAG_TRAINER_CLASS         = 0x00000020,     // TITLE is class trainer DESCRIPTION 100%
    UNIT_NPC_FLAG_TRAINER_PROFESSION    = 0x00000040,     // TITLE is profession trainer DESCRIPTION 100%
    UNIT_NPC_FLAG_VENDOR                = 0x00000080,     // TITLE is vendor (generic) DESCRIPTION 100%
    UNIT_NPC_FLAG_VENDOR_AMMO           = 0x00000100,     // TITLE is vendor (ammo) DESCRIPTION 100%, general goods vendor
    UNIT_NPC_FLAG_VENDOR_FOOD           = 0x00000200,     // TITLE is vendor (food) DESCRIPTION 100%
    UNIT_NPC_FLAG_VENDOR_POISON         = 0x00000400,     // TITLE is vendor (poison) DESCRIPTION guessed
    UNIT_NPC_FLAG_VENDOR_REAGENT        = 0x00000800,     // TITLE is vendor (reagents) DESCRIPTION 100%
    UNIT_NPC_FLAG_REPAIR                = 0x00001000,     // TITLE can repair DESCRIPTION 100%
    UNIT_NPC_FLAG_FLIGHTMASTER          = 0x00002000,     // TITLE is flight master DESCRIPTION 100%
    UNIT_NPC_FLAG_SPIRIT_HEALER         = 0x00004000,     // TITLE is spirit healer
    UNIT_NPC_FLAG_AREA_SPIRIT_HEALER    = 0x00008000,     // TITLE is area spirit healer
    UNIT_NPC_FLAG_INNKEEPER             = 0x00010000,     // TITLE is innkeeper
    UNIT_NPC_FLAG_BANKER                = 0x00020000,     // TITLE is banker DESCRIPTION 100%
    UNIT_NPC_FLAG_PETITIONER            = 0x00040000,     // TITLE handles guild/arena petitions DESCRIPTION 100% 0xC0000 = guild petitions, 0x40000 = arena team petitions
    UNIT_NPC_FLAG_TABARDDESIGNER        = 0x00080000,     // TITLE is guild tabard designer DESCRIPTION 100%
    UNIT_NPC_FLAG_BATTLEMASTER          = 0x00100000,     // TITLE is battlemaster DESCRIPTION 100%
    UNIT_NPC_FLAG_AUCTIONEER            = 0x00200000,     // TITLE is auctioneer DESCRIPTION 100%
    UNIT_NPC_FLAG_STABLEMASTER          = 0x00400000,     // TITLE is stable master DESCRIPTION 100%
    UNIT_NPC_FLAG_GUILD_BANKER          = 0x00800000,     // TITLE is guild banker DESCRIPTION
    UNIT_NPC_FLAG_SPELLCLICK            = 0x01000000,     // TITLE has spell click enabled
    UNIT_NPC_FLAG_PLAYER_VEHICLE        = 0x02000000,     // TITLE is player vehicle DESCRIPTION players with mounts that have vehicle data should have it set
    UNIT_NPC_FLAG_MAILBOX               = 0x04000000,     // TITLE is mailbox
    UNIT_NPC_FLAG_ARTIFACT_POWER_RESPEC = 0x08000000,     // TITLE can reset artifact powers
    UNIT_NPC_FLAG_TRANSMOGRIFIER        = 0x10000000,     // TITLE transmogrification
    UNIT_NPC_FLAG_VAULTKEEPER           = 0x20000000,     // TITLE is void storage
    UNIT_NPC_FLAG_WILD_BATTLE_PET       = 0x40000000,     // TITLE is wild battle pet DESCRIPTION Pet that player can fight (Battle Pet)
    UNIT_NPC_FLAG_BLACK_MARKET          = 0x80000000      // TITLE is black market
};
```

## NPCFlags2

[src/server/game/Entities/Unit/UnitDefines.h:360](../../../src/server/game/Entities/Unit/UnitDefines.h#L360)

```cpp
enum NPCFlags2 : uint32
{
    UNIT_NPC_FLAG_2_NONE                                            = 0x00000000,
    UNIT_NPC_FLAG_2_ITEM_UPGRADE_MASTER                             = 0x00000001,   // TITLE is item upgrade
    UNIT_NPC_FLAG_2_GARRISON_ARCHITECT                              = 0x00000002,   // TITLE is garrison architect DESCRIPTION garrison building placement UI
    UNIT_NPC_FLAG_2_STEERING                                        = 0x00000004,   // TITLE is avoiding obstacles DESCRIPTION clientside pathfinding
    UNIT_NPC_FLAG_2_AREA_SPIRIT_HEALER_INDIVIDUAL                   = 0x00000008,   // TITLE is area spirit healer individual DESCRIPTION area spirit healer with individual timers
    UNIT_NPC_FLAG_2_SHIPMENT_CRAFTER                                = 0x00000010,   // TITLE is shipment crafter DESCRIPTION garrison work orders
    UNIT_NPC_FLAG_2_GARRISON_MISSION_NPC                            = 0x00000020,   // TITLE is garrison mission
    UNIT_NPC_FLAG_2_TRADESKILL_NPC                                  = 0x00000040,   // TITLE is tradeskill DESCRIPTION crafting at npc
    UNIT_NPC_FLAG_2_BLACK_MARKET_VIEW                               = 0x00000080,   // TITLE is black market view DESCRIPTION only allows viewing black market auctions, no bidding
    UNIT_NPC_FLAG_2_GARRISON_TALENT_NPC                             = 0x00000200,   // TITLE is garrrison talent
    UNIT_NPC_FLAG_2_CONTRIBUTION_COLLECTOR                          = 0x00000400,   // TITLE is contribution collector
    UNIT_NPC_FLAG_2_FAST_STEERING_AVOIDS_OBSTACLES                  = 0x00002000,   // TITLE enables avoiding obstacles when FastSteering spline flag is set
    UNIT_NPC_FLAG_2_AZERITE_RESPEC                                  = 0x00004000,   // TITLE is azerite respec
    UNIT_NPC_FLAG_2_ISLANDS_QUEUE                                   = 0x00008000,   // TITLE is islands queue
    UNIT_NPC_FLAG_2_SUPPRESS_NPC_SOUNDS_EXCEPT_END_OF_INTERACTION   = 0x00010000,
    UNIT_NPC_FLAG_2_PERKS_VENDOR                                    = 0x00080000,   // TITLE is trading post vendor
    UNIT_NPC_FLAG_2_PERSONAL_TABARD_DESIGNER                        = 0x00200000,   // TITLE is personal tabard designer
};
```

## GameObjectChestFlags

[src/server/game/Entities/GameObject/GameObjectData.h:32](../../../src/server/game/Entities/GameObject/GameObjectData.h#L32)

```cpp
enum class GameObjectChestFlags : int32
{
    Consumable                  = 0x0001,
    RequireLOS                  = 0x0002,
    LeaveLoot                   = 0x0004,
    NotInCombat                 = 0x0008,
    LogLoot                     = 0x0010,
    UseGroupLootRules           = 0x0020,
    FloatingTooltip             = 0x0040,
    GroupXP                     = 0x0080,
    DamageImmuneOK              = 0x0100,
    GiganticAOI                 = 0x0200,
    LargeAOI                    = 0x0400,
    TurnPersonalLootSecurityOff = 0x0800,
    ForceSingleLooter           = 0x1000
};
```

## GameObjectActions

[src/server/game/Entities/GameObject/GameObjectData.h:1457](../../../src/server/game/Entities/GameObject/GameObjectData.h#L1457)

```cpp
enum class GameObjectActions : uint32
{
                                        // Name from client executable          // Comments
    None                        = 0,    // -NONE-
    AnimateCustom0              = 1,    // Animate Custom0
    AnimateCustom1              = 2,    // Animate Custom1
    AnimateCustom2              = 3,    // Animate Custom2
    AnimateCustom3              = 4,    // Animate Custom3
    Disturb                     = 5,    // Disturb                              // Triggers trap
    Unlock                      = 6,    // Unlock                               // Resets GO_FLAG_LOCKED
    Lock                        = 7,    // Lock                                 // Sets GO_FLAG_LOCKED
    Open                        = 8,    // Open                                 // Sets GO_STATE_ACTIVE
    OpenAndUnlock               = 9,    // Open + Unlock                        // Sets GO_STATE_ACTIVE and resets GO_FLAG_LOCKED
    Close                       = 10,   // Close                                // Sets GO_STATE_READY
    ToggleOpen                  = 11,   // Toggle Open
    Destroy                     = 12,   // Destroy                              // Sets GO_STATE_DESTROYED
    Rebuild                     = 13,   // Rebuild                              // Resets from GO_STATE_DESTROYED
    Creation                    = 14,   // Creation
    Despawn                     = 15,   // Despawn
    MakeInert                   = 16,   // Make Inert                           // Disables interactions
    MakeActive                  = 17,   // Make Active                          // Enables interactions
    CloseAndLock                = 18,   // Close + Lock                         // Sets GO_STATE_READY and sets GO_FLAG_LOCKED
    UseArtKit0                  = 19,   // Use ArtKit0                          // 46904: 121
    UseArtKit1                  = 20,   // Use ArtKit1                          // 36639: 81, 46903: 122
    UseArtKit2                  = 21,   // Use ArtKit2
    UseArtKit3                  = 22,   // Use ArtKit3
    SetTapList                  = 23,   // Set Tap List
    GoTo1stFloor                = 24,   // Go to 1st floor
    GoTo2ndFloor                = 25,   // Go to 2nd floor
    GoTo3rdFloor                = 26,   // Go to 3rd floor
    GoTo4thFloor                = 27,   // Go to 4th floor
    GoTo5thFloor                = 28,   // Go to 5th floor
    GoTo6thFloor                = 29,   // Go to 6th floor
    GoTo7thFloor                = 30,   // Go to 7th floor
    GoTo8thFloor                = 31,   // Go to 8th floor
    GoTo9thFloor                = 32,   // Go to 9th floor
    GoTo10thFloor               = 33,   // Go to 10th floor
    UseArtKit4                  = 34,   // Use ArtKit4
    PlayAnimKit                 = 35,   // Play Anim Kit "{AnimKit}"
    OpenAndPlayAnimKit          = 36,   // Open + Play Anim Kit "{AnimKit}"
    CloseAndPlayAnimKit         = 37,   // Close + Play Anim Kit "{AnimKit}"
    PlayOneShotAnimKit          = 38,   // Play One-shot Anim Kit "{AnimKit}"
    StopAnimKit                 = 39,   // Stop Anim Kit
    OpenAndStopAnimKit          = 40,   // Open + Stop Anim Kit
    CloseAndStopAnimKit         = 41,   // Close + Stop Anim Kit
    PlaySpellVisual             = 42,   // Play Spell Visual "{SpellVisual}"
    StopSpellVisual             = 43,   // Stop Spell Visual
    SetTappedToChallengePlayers = 44,   // Set Tapped to Challenge Players
    Max
};
```
