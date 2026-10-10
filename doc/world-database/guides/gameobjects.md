# Gameobjects

[Database documentation](../README.md)

[gameobject_template](../tables/gameobject_template.md) defines an object type, display, name, size, AI/script binding, and type-specific data. [gameobject](../tables/gameobject.md) defines persistent placements. Spawn GUIDs and template entries are different identity spaces.

## Interpreting Data0–Data34

The type column selects a C++ union layout. Count the fields of that type's block from Data0 using the [source-derived layout reference](../reference/gameobject-data.md). Do not copy a Data field interpretation from another type: a slot used for loot in one type may be a lock, spell, event, quest, or timing value in another.

Follow client references such as lock/display IDs into the corresponding client DB2/hotfix data. World schema cannot enumerate those external records.

## Placement and addon settings

A placement includes map-space position, orientation, quaternion components, spawn difficulty IDs, phase settings, and respawn/state information. Inspect gameobject_template_addon, gameobject_addon, and gameobject_overrides to understand template/spawn precedence.

Quaternions represent rotation; their components are not degrees or orientation values. Preserve known-good rotation conventions for the object.

Quest starter and ender tables refer to gameobject template identity. Event and spawn-group membership refer to spawn identity. Loot references are type-dependent Data slots, rather than a universal gameobject_template loot column.

## Inspection

```sql
SET @object_entry = 0; -- replace with an existing template
SELECT * FROM gameobject_template WHERE entry = @object_entry;
SELECT * FROM gameobject WHERE id = @object_entry LIMIT 20;

SELECT g.guid, g.id, g.map
FROM gameobject AS g
LEFT JOIN gameobject_template AS t ON t.entry = g.id
WHERE t.entry IS NULL
LIMIT 100;
```

## Troubleshooting

An object that is present but unusable may have the wrong type, flags, lock requirements, script binding, state, or conditions. An object that is absent may be gated by difficulty, phase, terrain, event, group, pool, or instance state. Wrong geometry can be a display/rotation issue. Validate the selected Data layout before changing a seemingly unrelated integer.

For scripted interaction see [SmartAI](smartai.md); for world visibility see [world content](world-content.md).
