# Loot Enums

[Database documentation](../README.md)

Source-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.

## Type

[src/server/game/Loot/LootMgr.h:40](../../../src/server/game/Loot/LootMgr.h#L40)

```cpp
enum class Type : int8
    {
        Item            = 0,
        Reference       = 1,
        Currency        = 2,
        TrackingQuest   = 3,
    };
```

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
