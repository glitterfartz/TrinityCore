# Spell Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## SpellTargetSelectionCategories

[src/server/game/Spells/SpellInfo.h:41](../../../src/server/game/Spells/SpellInfo.h#L41)

```cpp
enum SpellTargetSelectionCategories
{
    TARGET_SELECT_CATEGORY_NYI,
    TARGET_SELECT_CATEGORY_DEFAULT,
    TARGET_SELECT_CATEGORY_CHANNEL,
    TARGET_SELECT_CATEGORY_NEARBY,
    TARGET_SELECT_CATEGORY_CONE,
    TARGET_SELECT_CATEGORY_AREA,
    TARGET_SELECT_CATEGORY_TRAJ,
    TARGET_SELECT_CATEGORY_LINE
};
```

## SpellTargetReferenceTypes

[src/server/game/Spells/SpellInfo.h:53](../../../src/server/game/Spells/SpellInfo.h#L53)

```cpp
enum SpellTargetReferenceTypes
{
    TARGET_REFERENCE_TYPE_NONE,
    TARGET_REFERENCE_TYPE_CASTER,
    TARGET_REFERENCE_TYPE_TARGET,
    TARGET_REFERENCE_TYPE_LAST,
    TARGET_REFERENCE_TYPE_SRC,
    TARGET_REFERENCE_TYPE_DEST
};
```

## SpellTargetObjectTypes

[src/server/game/Spells/SpellInfo.h:63](../../../src/server/game/Spells/SpellInfo.h#L63)

```cpp
enum SpellTargetObjectTypes : uint8
{
    TARGET_OBJECT_TYPE_NONE = 0,
    TARGET_OBJECT_TYPE_SRC,
    TARGET_OBJECT_TYPE_DEST,
    TARGET_OBJECT_TYPE_UNIT,
    TARGET_OBJECT_TYPE_UNIT_AND_DEST,
    TARGET_OBJECT_TYPE_GOBJ,
    TARGET_OBJECT_TYPE_GOBJ_ITEM,
    TARGET_OBJECT_TYPE_ITEM,
    TARGET_OBJECT_TYPE_CORPSE,
    // only for effect target type
    TARGET_OBJECT_TYPE_CORPSE_ENEMY,
    TARGET_OBJECT_TYPE_CORPSE_ALLY
};
```

## SpellTargetCheckTypes

[src/server/game/Spells/SpellInfo.h:79](../../../src/server/game/Spells/SpellInfo.h#L79)

```cpp
enum SpellTargetCheckTypes : uint8
{
    TARGET_CHECK_DEFAULT,
    TARGET_CHECK_ENTRY,
    TARGET_CHECK_ENEMY,
    TARGET_CHECK_ALLY,
    TARGET_CHECK_PARTY,
    TARGET_CHECK_RAID,
    TARGET_CHECK_RAID_CLASS,
    TARGET_CHECK_PASSENGER,
    TARGET_CHECK_SUMMONED
};
```

## SpellTargetDirectionTypes

[src/server/game/Spells/SpellInfo.h:92](../../../src/server/game/Spells/SpellInfo.h#L92)

```cpp
enum SpellTargetDirectionTypes
{
    TARGET_DIR_NONE,
    TARGET_DIR_FRONT,
    TARGET_DIR_BACK,
    TARGET_DIR_RIGHT,
    TARGET_DIR_LEFT,
    TARGET_DIR_FRONT_RIGHT,
    TARGET_DIR_BACK_RIGHT,
    TARGET_DIR_BACK_LEFT,
    TARGET_DIR_FRONT_LEFT,
    TARGET_DIR_RANDOM,
    TARGET_DIR_ENTRY
};
```

## SpellEffectImplicitTargetTypes

[src/server/game/Spells/SpellInfo.h:107](../../../src/server/game/Spells/SpellInfo.h#L107)

```cpp
enum SpellEffectImplicitTargetTypes
{
    EFFECT_IMPLICIT_TARGET_NONE = 0,
    EFFECT_IMPLICIT_TARGET_EXPLICIT,
    EFFECT_IMPLICIT_TARGET_CASTER
};
```

## SpellSpecificType

[src/server/game/Spells/SpellInfo.h:115](../../../src/server/game/Spells/SpellInfo.h#L115)

```cpp
enum SpellSpecificType
{
    SPELL_SPECIFIC_NORMAL                        = 0,
    SPELL_SPECIFIC_SEAL                          = 1,
    SPELL_SPECIFIC_AURA                          = 3,
    SPELL_SPECIFIC_STING                         = 4,
    SPELL_SPECIFIC_CURSE                         = 5,
    SPELL_SPECIFIC_ASPECT                        = 6,
    SPELL_SPECIFIC_TRACKER                       = 7,
    SPELL_SPECIFIC_WARLOCK_ARMOR                 = 8,
    SPELL_SPECIFIC_MAGE_ARMOR                    = 9,
    SPELL_SPECIFIC_ELEMENTAL_SHIELD              = 10,
    SPELL_SPECIFIC_MAGE_POLYMORPH                = 11,
    SPELL_SPECIFIC_FOOD                          = 19,
    SPELL_SPECIFIC_DRINK                         = 20,
    SPELL_SPECIFIC_FOOD_AND_DRINK                = 21,
    SPELL_SPECIFIC_PRESENCE                      = 22,
    SPELL_SPECIFIC_CHARM                         = 23,
    SPELL_SPECIFIC_SCROLL                        = 24,
    SPELL_SPECIFIC_MAGE_ARCANE_BRILLANCE         = 25,
    SPELL_SPECIFIC_WARRIOR_ENRAGE                = 26,
    SPELL_SPECIFIC_PRIEST_DIVINE_SPIRIT          = 27,
    SPELL_SPECIFIC_HAND                          = 28,
    SPELL_SPECIFIC_PHASE                         = 29,
    SPELL_SPECIFIC_BANE                          = 30
};
```

## SpellCustomAttributes

[src/server/game/Spells/SpellInfo.h:142](../../../src/server/game/Spells/SpellInfo.h#L142)

```cpp
enum SpellCustomAttributes
{
    SPELL_ATTR0_CU_ENCHANT_PROC                  = 0x00000001,
    SPELL_ATTR0_CU_CONE_BACK                     = 0x00000002,
    SPELL_ATTR0_CU_CONE_LINE                     = 0x00000004,
    SPELL_ATTR0_CU_SHARE_DAMAGE                  = 0x00000008,
    SPELL_ATTR0_CU_NO_INITIAL_THREAT             = 0x00000010,
    SPELL_ATTR0_CU_AURA_CC                       = 0x00000020,
    SPELL_ATTR0_CU_DONT_BREAK_STEALTH            = 0x00000040,
    SPELL_ATTR0_CU_CAN_CRIT                      = 0x00000080,
    SPELL_ATTR0_CU_DIRECT_DAMAGE                 = 0x00000100,
    SPELL_ATTR0_CU_CHARGE                        = 0x00000200,
    SPELL_ATTR0_CU_PICKPOCKET                    = 0x00000400,
    SPELL_ATTR0_CU_DEPRECATED_ROLLING_PERIODIC   = 0x00000800, // DO NOT REUSE
    SPELL_ATTR0_CU_DEPRECATED_NEGATIVE_EFF0      = 0x00001000, // DO NOT REUSE
    SPELL_ATTR0_CU_DEPRECATED_NEGATIVE_EFF1      = 0x00002000, // DO NOT REUSE
    SPELL_ATTR0_CU_DEPRECATED_NEGATIVE_EFF2      = 0x00004000, // DO NOT REUSE
    SPELL_ATTR0_CU_IGNORE_ARMOR                  = 0x00008000,
    SPELL_ATTR0_CU_REQ_TARGET_FACING_CASTER      = 0x00010000,
    SPELL_ATTR0_CU_REQ_CASTER_BEHIND_TARGET      = 0x00020000,
    SPELL_ATTR0_CU_ALLOW_INFLIGHT_TARGET         = 0x00040000,
    SPELL_ATTR0_CU_NEEDS_AMMO_DATA               = 0x00080000,
    SPELL_ATTR0_CU_BINARY_SPELL                  = 0x00100000,
    SPELL_ATTR0_CU_SCHOOLMASK_NORMAL_WITH_MAGIC  = 0x00200000,
    SPELL_ATTR0_CU_DEPRECATED_LIQUID_AURA        = 0x00400000, // DO NOT REUSE
    SPELL_ATTR0_CU_IS_TALENT                     = 0x00800000,
    SPELL_ATTR0_CU_AURA_CANNOT_BE_SAVED          = 0x01000000,
    SPELL_ATTR0_CU_CAN_TARGET_ANY_PRIVATE_OBJECT = 0x02000000,
};
```

## SpellInterruptFlags

[src/server/game/Spells/SpellDefines.h:59](../../../src/server/game/Spells/SpellDefines.h#L59)

```cpp
enum class SpellInterruptFlags : uint32
{
    None                        = 0,
    Movement                    = 0x00000001,
    DamagePushbackPlayerOnly    = 0x00000002,
    Stun                        = 0x00000004, // useless, even spells without it get interrupted
    Combat                      = 0x00000008, // used for both interrupting spell when entering combat and to reset auto attack timer
    DamageCancelsPlayerOnly     = 0x00000010,
    MeleeCombat                 = 0x00000020, // NYI
    Immunity                    = 0x00000040, // NYI
    DamageAbsorb                = 0x00000080,
    ZeroDamageCancels           = 0x00000100,
    DamagePushback              = 0x00000200,
    DamageCancels               = 0x00000400
};
```

## SpellAuraInterruptFlags

[src/server/game/Spells/SpellDefines.h:77](../../../src/server/game/Spells/SpellDefines.h#L77)

```cpp
enum class SpellAuraInterruptFlags : uint32
{
    None                        = 0,
    HostileActionReceived       = 0x00000001,
    Damage                      = 0x00000002,
    Action                      = 0x00000004,
    Moving                      = 0x00000008,
    Turning                     = 0x00000010,
    Anim                        = 0x00000020,
    Dismount                    = 0x00000040,
    UnderWater                  = 0x00000080, // TODO: disallow casting when swimming (SPELL_FAILED_ONLY_ABOVEWATER)
    AboveWater                  = 0x00000100, // TODO: disallow casting when not swimming (SPELL_FAILED_ONLY_UNDERWATER)
    Sheathing                   = 0x00000200,
    Interacting                 = 0x00000400, // TODO: more than gossip, replace all the feign death removals by aura type
    Looting                     = 0x00000800,
    Attacking                   = 0x00001000,
    ItemUse                     = 0x00002000,
    DamageChannelDuration       = 0x00004000,
    Shapeshifting               = 0x00008000,
    ActionDelayed               = 0x00010000,
    Mount                       = 0x00020000,
    Standing                    = 0x00040000,
    LeaveWorld                  = 0x00080000,
    StealthOrInvis              = 0x00100000,
    InvulnerabilityBuff         = 0x00200000,
    EnterWorld                  = 0x00400000,
    PvPActive                   = 0x00800000,
    NonPeriodicDamage           = 0x01000000,
    LandingOrFlight             = 0x02000000,
    Release                     = 0x04000000,
    DamageCancelsScript         = 0x08000000, // NYI dedicated aura script hook
    EnteringCombat              = 0x10000000,
    Login                       = 0x20000000,
    Summon                      = 0x40000000,
    LeavingCombat               = 0x80000000,

    NOT_VICTIM                  = HostileActionReceived | Damage | NonPeriodicDamage,
    AnyDamageMask               = Damage | NonPeriodicDamage | DamageCancelsScript
};
```

## SpellAuraInterruptFlags2

[src/server/game/Spells/SpellDefines.h:119](../../../src/server/game/Spells/SpellDefines.h#L119)

```cpp
enum class SpellAuraInterruptFlags2 : uint32
{
    None                                        = 0,
    Falling                                     = 0x00000001, // Implemented in Unit::UpdatePosition
    Swimming                                    = 0x00000002,
    NotMoving                                   = 0x00000004, // NYI
    Ground                                      = 0x00000008,
    Transform                                   = 0x00000010,
    Jump                                        = 0x00000020,
    ChangeSpec                                  = 0x00000040,
    AbandonVehicle                              = 0x00000080, // Implemented in Unit::_ExitVehicle
    StartOfRaidEncounterAndStartOfMythicPlus    = 0x00000100, // Implemented in Unit::AtStartOfEncounter
    EndOfRaidEncounterAndStartOfMythicPlus      = 0x00000200, // Implemented in Unit::AtEndOfEncounter
    Disconnect                                  = 0x00000400, // NYI
    EnteringInstance                            = 0x00000800, // Implemented in Map::AddPlayerToMap
    DuelEnd                                     = 0x00001000, // Implemented in Player::DuelComplete
    LeaveArenaOrBattleground                    = 0x00002000, // Implemented in Battleground::RemovePlayerAtLeave
    ChangeTalent                                = 0x00004000,
    ChangeGlyph                                 = 0x00008000,
    SeamlessTransfer                            = 0x00010000, // NYI
    WarModeLeave                                = 0x00020000, // Implemented in Player::UpdateWarModeAuras
    TouchingGround                              = 0x00040000, // NYI
    ChromieTime                                 = 0x00080000, // NYI
    SplineFlightOrFreeFlight                    = 0x00100000, // NYI
    ProcOrPeriodicAttacking                     = 0x00200000, // NYI
    ChallengeModeStart                          = 0x00400000, // Implemented in Unit::AtStartOfEncounter
    StartOfEncounter                            = 0x00800000, // Implemented in Unit::AtStartOfEncounter
    EndOfEncounter                              = 0x01000000, // Implemented in Unit::AtEndOfEncounter
    ReleaseEmpower                              = 0x02000000, // Implemented in Spell::update
};
```

## SpellModOp

[src/server/game/Spells/SpellDefines.h:152](../../../src/server/game/Spells/SpellDefines.h#L152)

```cpp
enum class SpellModOp : uint8
{
    HealingAndDamage            = 0,
    Duration                    = 1,
    Hate                        = 2,
    PointsIndex0                = 3,
    ProcCharges                 = 4,
    Range                       = 5,
    Radius                      = 6,
    CritChance                  = 7,
    Points                      = 8,
    ResistPushback              = 9,
    ChangeCastTime              = 10,
    Cooldown                    = 11,
    PointsIndex1                = 12,
    TargetResistance            = 13,
    PowerCost0                  = 14, // Used when SpellPowerEntry::PowerIndex == 0
    CritDamageAndHealing        = 15,
    HitChance                   = 16,
    ChainTargets                = 17,
    ProcChance                  = 18,
    Period                      = 19,
    ChainAmplitude              = 20,
    StartCooldown               = 21,
    PeriodicHealingAndDamage    = 22,
    PointsIndex2                = 23,
    BonusCoefficient            = 24,
    TriggerDamage               = 25, // NYI
    ProcFrequency               = 26,
    Amplitude                   = 27,
    DispelResistance            = 28,
    CrowdDamage                 = 29, // NYI
    PowerCostOnMiss             = 30,
    Doses                       = 31,
    PointsIndex3                = 32,
    PointsIndex4                = 33,
    PowerCost1                  = 34, // Used when SpellPowerEntry::PowerIndex == 1
    ChainJumpDistance           = 35,
    AreaTriggerMaxSummons       = 36, // NYI
    MaxAuraStacks               = 37,
    ProcCooldown                = 38,
    PowerCost2                  = 39, // Used when SpellPowerEntry::PowerIndex == 2
    MaxTargets                  = 40
};
```

## SpellPvpModifier

[src/server/game/Spells/SpellDefines.h:199](../../../src/server/game/Spells/SpellDefines.h#L199)

```cpp
enum class SpellPvpModifier : uint8
{
    HealingAndDamage            = 0,
    PeriodicHealingAndDamage    = 1,
    BonusCoefficient            = 2,

    Points                      = 4,
    PointsIndex0                = 5,
    PointsIndex1                = 6,
    PointsIndex2                = 7,
    PointsIndex3                = 8,
    PointsIndex4                = 9,
};
```

## SpellValueMod

[src/server/game/Spells/SpellDefines.h:213](../../../src/server/game/Spells/SpellDefines.h#L213)

```cpp
enum SpellValueMod : int32
{
    SPELLVALUE_MAX_TARGETS,
    SPELLVALUE_AURA_STACK,
    SPELLVALUE_DURATION,
    SPELLVALUE_PARENT_SPELL_TARGET_COUNT,
    SPELLVALUE_PARENT_SPELL_TARGET_INDEX,

    SPELLVALUE_INT_END
};
```

## SpellValueModFloat

[src/server/game/Spells/SpellDefines.h:224](../../../src/server/game/Spells/SpellDefines.h#L224)

```cpp
enum SpellValueModFloat : int32
{
    SPELLVALUE_BASE_POINT0  = uint8(SPELLVALUE_INT_END),
    SPELLVALUE_BASE_POINT1,
    SPELLVALUE_BASE_POINT2,
    SPELLVALUE_BASE_POINT3,
    SPELLVALUE_BASE_POINT4,
    SPELLVALUE_BASE_POINT5,
    SPELLVALUE_BASE_POINT6,
    SPELLVALUE_BASE_POINT7,
    SPELLVALUE_BASE_POINT8,
    SPELLVALUE_BASE_POINT9,
    SPELLVALUE_BASE_POINT10,
    SPELLVALUE_BASE_POINT11,
    SPELLVALUE_BASE_POINT12,
    SPELLVALUE_BASE_POINT13,
    SPELLVALUE_BASE_POINT14,
    SPELLVALUE_BASE_POINT15,
    SPELLVALUE_BASE_POINT16,
    SPELLVALUE_BASE_POINT17,
    SPELLVALUE_BASE_POINT18,
    SPELLVALUE_BASE_POINT19,
    SPELLVALUE_BASE_POINT20,
    SPELLVALUE_BASE_POINT21,
    SPELLVALUE_BASE_POINT22,
    SPELLVALUE_BASE_POINT23,
    SPELLVALUE_BASE_POINT24,
    SPELLVALUE_BASE_POINT25,
    SPELLVALUE_BASE_POINT26,
    SPELLVALUE_BASE_POINT27,
    SPELLVALUE_BASE_POINT28,
    SPELLVALUE_BASE_POINT29,
    SPELLVALUE_BASE_POINT30,
    SPELLVALUE_BASE_POINT31,

    SPELLVALUE_BASE_POINT_END,

    SPELLVALUE_RADIUS_MOD   = SPELLVALUE_BASE_POINT_END,
    SPELLVALUE_CRIT_CHANCE,
    SPELLVALUE_DURATION_PCT,
};
```

## SpellFacingFlags

[src/server/game/Spells/SpellDefines.h:266](../../../src/server/game/Spells/SpellDefines.h#L266)

```cpp
enum SpellFacingFlags
{
    SPELL_FACING_FLAG_INFRONT = 0x0001
};
```

## TriggerCastFlags

[src/server/game/Spells/SpellDefines.h:271](../../../src/server/game/Spells/SpellDefines.h#L271)

```cpp
enum TriggerCastFlags : uint32
{
    TRIGGERED_NONE                                  = 0x00000000,   //!< Not triggered
    TRIGGERED_IGNORE_GCD                            = 0x00000001,   //!< Will ignore GCD
    TRIGGERED_IGNORE_SPELL_AND_CATEGORY_CD          = 0x00000002,   //!< Will ignore Spell and Category cooldowns
    TRIGGERED_IGNORE_POWER_COST                     = 0x00000004,   //!< Will ignore power and reagent cost
    TRIGGERED_IGNORE_CAST_ITEM                      = 0x00000008,   //!< Will not take away cast item or update related achievement criteria
    TRIGGERED_IGNORE_AURA_SCALING                   = 0x00000010,   //!< Will ignore aura scaling
    TRIGGERED_IGNORE_CAST_IN_PROGRESS               = 0x00000020,   //!< Will not check if a current cast is in progress
    TRIGGERED_IGNORE_CAST_TIME                      = 0x00000040,   //!< Will always be instantly cast
    TRIGGERED_CAST_DIRECTLY                         = 0x00000080,   //!< In Spell::prepare, will be cast directly without setting containers for executed spell
    TRIGGERED_IGNORE_REAGENT_COST                   = 0x00000100,   //!< Will ignore reagent cost
    TRIGGERED_IGNORE_SET_FACING                     = 0x00000200,   //!< Will not adjust facing to target (if any)
    TRIGGERED_IGNORE_SHAPESHIFT                     = 0x00000400,   //!< Will ignore shapeshift checks
    // reuse                                        = 0x00000800,
    TRIGGERED_DISALLOW_PROC_EVENTS                  = 0x00001000,   //!< Disallows proc events from triggered spell (default)
    TRIGGERED_IGNORE_CASTER_MOUNTED_OR_ON_VEHICLE   = 0x00002000,   //!< Will ignore mounted/on vehicle restrictions
    // reuse                                        = 0x00004000,
    // reuse                                        = 0x00008000,
    TRIGGERED_IGNORE_CASTER_AURAS                   = 0x00010000,   //!< Will ignore caster aura restrictions or requirements
    TRIGGERED_DONT_RESET_PERIODIC_TIMER             = 0x00020000,   //!< Will allow periodic aura timers to keep ticking (instead of resetting)
    TRIGGERED_DONT_REPORT_CAST_ERROR                = 0x00040000,   //!< Will return SPELL_FAILED_DONT_REPORT in CheckCast functions
    TRIGGERED_FULL_MASK                             = 0x0007FFFF,   //!< Used when doing CastSpell with triggered == true
    TRIGGERED_IS_TRIGGERED_MASK                     = TRIGGERED_FULL_MASK
                                                        & ~(TRIGGERED_IGNORE_POWER_COST | TRIGGERED_IGNORE_CAST_IN_PROGRESS
                                                            | TRIGGERED_IGNORE_CAST_TIME | TRIGGERED_IGNORE_SHAPESHIFT
                                                            | TRIGGERED_DONT_REPORT_CAST_ERROR), //!< Will be recognized by Spell::IsTriggered as triggered

    // debug flags (used with .cast triggered commands)
    TRIGGERED_IGNORE_EQUIPPED_ITEM_REQUIREMENT      = 0x00080000,   //!< Will ignore equipped item requirements
    TRIGGERED_IGNORE_TARGET_CHECK                   = 0x00100000,   //!< Will ignore most target checks (mostly DBC target checks)
    TRIGGERED_IGNORE_CASTER_AURASTATE               = 0x00200000,   //!< Will ignore caster aura states including combat requirements and death state
    TRIGGERED_SUPPRESS_CASTER_ANIM                  = 0x00400000,   //!< Will not play cast animations on caster
    TRIGGERED_FULL_DEBUG_MASK                       = 0xFFFFFFFF
};
```

## SpellCastTargetFlags

[src/server/game/Spells/SpellDefines.h:309](../../../src/server/game/Spells/SpellDefines.h#L309)

```cpp
enum SpellCastTargetFlags : uint32
{
    TARGET_FLAG_NONE            = 0x00000000,
    TARGET_FLAG_UNUSED_1        = 0x00000001,               // not used
    TARGET_FLAG_UNIT            = 0x00000002,               // pguid
    TARGET_FLAG_UNIT_RAID       = 0x00000004,               // not sent, used to validate target (if raid member)
    TARGET_FLAG_UNIT_PARTY      = 0x00000008,               // not sent, used to validate target (if party member)
    TARGET_FLAG_ITEM            = 0x00000010,               // pguid
    TARGET_FLAG_SOURCE_LOCATION = 0x00000020,               // pguid, 3 float
    TARGET_FLAG_DEST_LOCATION   = 0x00000040,               // pguid, 3 float
    TARGET_FLAG_UNIT_ENEMY      = 0x00000080,               // not sent, used to validate target (if enemy)
    TARGET_FLAG_UNIT_ALLY       = 0x00000100,               // not sent, used to validate target (if ally)
    TARGET_FLAG_CORPSE_ENEMY    = 0x00000200,               // pguid
    TARGET_FLAG_UNIT_DEAD       = 0x00000400,               // not sent, used to validate target (if dead creature)
    TARGET_FLAG_GAMEOBJECT      = 0x00000800,               // pguid, used with TARGET_GAMEOBJECT_TARGET
    TARGET_FLAG_TRADE_ITEM      = 0x00001000,               // pguid
    TARGET_FLAG_STRING          = 0x00002000,               // string
    TARGET_FLAG_GAMEOBJECT_ITEM = 0x00004000,               // not sent, used with TARGET_GAMEOBJECT_ITEM_TARGET
    TARGET_FLAG_CORPSE_ALLY     = 0x00008000,               // pguid
    TARGET_FLAG_UNIT_MINIPET    = 0x00010000,               // pguid, used to validate target (if non combat pet)
    TARGET_FLAG_GLYPH_SLOT      = 0x00020000,               // used in glyph spells
    TARGET_FLAG_DEST_TARGET     = 0x00040000,               // sometimes appears with DEST_TARGET spells (may appear or not for a given spell)
    TARGET_FLAG_EXTRA_TARGETS   = 0x00080000,               // uint32 counter, loop { vec3 - screen position (?), guid }, not used so far
    TARGET_FLAG_UNIT_PASSENGER  = 0x00100000,               // guessed, used to validate target (if vehicle passenger)
    TARGET_FLAG_UNK400000       = 0X00400000,
    TARGET_FLAG_UNK1000000      = 0X01000000,
    TARGET_FLAG_UNK4000000      = 0X04000000,
    TARGET_FLAG_UNK10000000     = 0X10000000,
    TARGET_FLAG_UNK40000000     = 0X40000000,

    TARGET_FLAG_UNIT_MASK = TARGET_FLAG_UNIT | TARGET_FLAG_UNIT_RAID | TARGET_FLAG_UNIT_PARTY
        | TARGET_FLAG_UNIT_ENEMY | TARGET_FLAG_UNIT_ALLY | TARGET_FLAG_UNIT_DEAD | TARGET_FLAG_UNIT_MINIPET | TARGET_FLAG_UNIT_PASSENGER,
    TARGET_FLAG_GAMEOBJECT_MASK = TARGET_FLAG_GAMEOBJECT | TARGET_FLAG_GAMEOBJECT_ITEM,
    TARGET_FLAG_CORPSE_MASK = TARGET_FLAG_CORPSE_ALLY | TARGET_FLAG_CORPSE_ENEMY,
    TARGET_FLAG_ITEM_MASK = TARGET_FLAG_TRADE_ITEM | TARGET_FLAG_ITEM | TARGET_FLAG_GAMEOBJECT_ITEM
};
```
