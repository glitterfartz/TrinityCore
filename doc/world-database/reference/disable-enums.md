# Disable Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## DisableType

[src/server/game/Conditions/DisableMgr.h:25](../../../src/server/game/Conditions/DisableMgr.h#L25)

```cpp
enum DisableType
{
    DISABLE_TYPE_SPELL                  = 0,
    DISABLE_TYPE_QUEST                  = 1,
    DISABLE_TYPE_MAP                    = 2,
    DISABLE_TYPE_BATTLEGROUND           = 3,
    DISABLE_TYPE_CRITERIA               = 4,
    DISABLE_TYPE_OUTDOORPVP             = 5,
    DISABLE_TYPE_VMAP                   = 6,
    DISABLE_TYPE_MMAP                   = 7,
    DISABLE_TYPE_LFG_MAP                = 8,
    DISABLE_TYPE_PHASE_AREA             = 9,

    MAX_DISABLE_TYPES
};
```

## SpellDisableTypes

[src/server/game/Conditions/DisableMgr.h:41](../../../src/server/game/Conditions/DisableMgr.h#L41)

```cpp
enum SpellDisableTypes
{
    SPELL_DISABLE_PLAYER            = 0x01,
    SPELL_DISABLE_CREATURE          = 0x02,
    SPELL_DISABLE_PET               = 0x04,
    SPELL_DISABLE_DEPRECATED_SPELL  = 0x08,
    SPELL_DISABLE_MAP               = 0x10,
    SPELL_DISABLE_AREA              = 0x20,
    SPELL_DISABLE_LOS               = 0x40,
    SPELL_DISABLE_GAMEOBJECT        = 0x80,
    SPELL_DISABLE_ARENAS            = 0x100,
    SPELL_DISABLE_BATTLEGROUNDS     = 0x200,
    MAX_SPELL_DISABLE_TYPE = (  SPELL_DISABLE_PLAYER | SPELL_DISABLE_CREATURE | SPELL_DISABLE_PET |
                                SPELL_DISABLE_DEPRECATED_SPELL | SPELL_DISABLE_MAP | SPELL_DISABLE_AREA |
                                SPELL_DISABLE_LOS | SPELL_DISABLE_GAMEOBJECT | SPELL_DISABLE_ARENAS |
                                SPELL_DISABLE_BATTLEGROUNDS),
};
```

## MMapDisableTypes

[src/server/game/Conditions/DisableMgr.h:59](../../../src/server/game/Conditions/DisableMgr.h#L59)

```cpp
enum MMapDisableTypes
{
    MMAP_DISABLE_PATHFINDING    = 0x0
};
```
