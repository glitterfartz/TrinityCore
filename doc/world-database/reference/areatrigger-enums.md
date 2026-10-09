# Areatrigger Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## AreaTriggerFlag

[src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h:33](../../../src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h#L33)

```cpp
enum class AreaTriggerFlag : uint32
{
    None                           = 0x00,
    IsServerSide                   = 0x01
};
```

## AreaTriggerActionTypes

[src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h:41](../../../src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h#L41)

```cpp
enum AreaTriggerActionTypes
{
    AREATRIGGER_ACTION_CAST        = 0,
    AREATRIGGER_ACTION_ADDAURA     = 1,
    AREATRIGGER_ACTION_TELEPORT    = 2,
    AREATRIGGER_ACTION_TAVERN      = 3,
    AREATRIGGER_ACTION_MAX         = 4
};
```

## AreaTriggerActionUserTypes

[src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h:50](../../../src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h#L50)

```cpp
enum AreaTriggerActionUserTypes
{
    AREATRIGGER_ACTION_USER_ANY    = 0,
    AREATRIGGER_ACTION_USER_FRIEND = 1,
    AREATRIGGER_ACTION_USER_ENEMY  = 2,
    AREATRIGGER_ACTION_USER_RAID   = 3,
    AREATRIGGER_ACTION_USER_PARTY  = 4,
    AREATRIGGER_ACTION_USER_CASTER = 5,
    AREATRIGGER_ACTION_USER_MAX    = 6
};
```

## AreaTriggerCreatePropertiesFlag

[src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h:61](../../../src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h#L61)

```cpp
enum class AreaTriggerCreatePropertiesFlag : uint32
{
    None                           = 0x0000,
    HeightIgnoresScale             = 0x0001,
    VisualAnimIsDecay              = 0x0002,
    AbsoluteOrientation            = 0x0004,
    FaceMovementDir                = 0x0008, // NYI
    FollowsTerrain                 = 0x0010, // NYI
    AlwaysExterior                 = 0x0020,
    UsesUnitRawFacing              = 0x0040  // NYI
};
```
