# Creatures and spawns

[Database documentation](../README.md)

## Template versus placement

[creature_template](../tables/creature_template.md) defines an NPC type. [creature](../tables/creature.md) places an instance of that type in a map. creature.id refers to the template entry; creature.guid is the persistent spawn identifier. Multiple spawns can share the same template, and summoned NPCs can use a template without a persistent spawn row.

Template changes affect every consumer of the template. Spawn changes affect one placement, subject to instance/event/pool behavior. Distinguish these identities before editing addon, equipment, formation, or quest relation rows.

Current master splits additional data into creature_template_difficulty, creature_template_model, creature_template_spell, creature_template_resistance, creature_template_movement, creature_template_gossip, creature_immunities, and other extension tables. Older guides that place all of this in one template row are incomplete for this schema.

## Difficulty, appearance, and behavior

Use [creature_template_difficulty](../tables/creature_template_difficulty.md) for difficulty-specific tuning and loot references. LootID need not equal the NPC entry. Display choices belong to creature_template_model; creature_model_info supplies model metadata. Per-spawn model and equipment choices may override defaults according to ObjectMgr's loader.

Template addons provide reusable appearance, emote, aura, and path settings. creature_addon configures a particular spawn. NULL flag/health values on a spawn are distinct from explicit zero and can preserve default behavior. Check the loader's override logic before replacing NULLs.

AIName selects a registered AI, and ScriptName selects a compiled script. For SmartAI, inspect the corresponding smart_scripts owner and source type. Names must match registered code; assigning an arbitrary ScriptName cannot create functionality.

## Placement and visibility

Map, coordinates, orientation, spawnDifficulties, phase flags, PhaseId/PhaseGroup, and terrainSwapMap determine where and when the NPC is available. Difficulty IDs are a comma-separated list. World visibility phases are separate from SmartAI event phases.

Spawns can also be controlled by spawn groups, events, pools, instance state, and spawn tracking. Absence in-game does not imply the creature row is missing.

## Inspection

```sql
SET @creature_entry = 0; -- replace with an existing template
SELECT * FROM creature_template WHERE entry = @creature_entry;
SELECT * FROM creature_template_difficulty WHERE Entry = @creature_entry;
SELECT * FROM creature WHERE id = @creature_entry LIMIT 20;

SELECT c.guid, c.id, c.map
FROM creature AS c
LEFT JOIN creature_template AS t ON t.entry = c.id
WHERE t.entry IS NULL
LIMIT 100;
```

The last query identifies missing template associations; it is a diagnostic, not authorization to delete rows.

## Authoring sequence

1. Select or define the template and confirm required external faction/display/spell records.
2. Add the required extension rows for the intended difficulty and appearance.
3. Define AI or compiled script behavior and any text, spell-click, vendor, trainer, or quest relations.
4. Place the spawn with the correct map, phase, difficulty, and group membership.
5. Verify movement/addon precedence and event/pool dependencies.
6. Review sql.sql startup logs and test the intended interaction in-game.

For health, damage, immunities, movement, and flags, follow the linked source definitions rather than guessing from integer names. See [loot](loot.md), [NPC interaction](npc-interaction.md), and [world content](world-content.md).
