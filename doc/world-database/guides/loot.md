# Loot

[Database documentation](../README.md)

## Current master storage

All twelve loot tables share typed reward and roll fields: Entry, ItemType, Item, Chance, QuestRequired, LootMode, GroupId, MinCount, MaxCount, and Comment. This schema does **not** have the older separate Reference column. Do not paste legacy loot INSERT statements without adapting them.

Entry identifies a loot definition in that table, not necessarily a creature/item template entry. ItemType determines how Item is interpreted. Use the current [loot enum reference](../reference/loot-enums.md) and [LootMgr.cpp](../../../src/server/game/Loot/LootMgr.cpp) for reward kinds and validation.

## Sources

| Loot table | Typical consuming source |
| --- | --- |
| creature_loot_template | creature_template_difficulty loot definition |
| pickpocketing_loot_template | Creature difficulty pickpocket definition |
| skinning_loot_template | Creature difficulty skinning definition |
| gameobject_loot_template | Type-specific gameobject Data loot slot |
| item_loot_template | Item opening/use loot |
| disenchant_loot_template | Disenchant reward rules |
| fishing_loot_template | Fishing area/location rules |
| milling_loot_template | Milling input |
| prospecting_loot_template | Prospecting input |
| spell_loot_template | Spell-generated loot |
| mail_loot_template | Mail reward definition |
| reference_loot_template | Referenced reusable loot definitions |

The exact lookup and external identifier validation are source-specific. Do not assume Entry has the same identity meaning in every table.

## Roll semantics

Chance is a percentage for ordinary eligible loot selection. Zero may represent equal-chance participation in a nonzero roll group; it is not universally “never drops.” GroupId changes selection into grouped alternatives rather than independent rows. Group probabilities must follow the current LootGroup implementation.

LootMode is a bitmask; rows are eligible only for matching modes. QuestRequired gates ordinary rewards on qualifying quest needs. Counts are type-specific: item/currency rewards require positive MinCount and MaxCount at least MinCount; a tracking-quest reward requires MinCount = 1 and MaxCount = 0. Reference counts have repeat semantics, and QuestRequired is ignored for references. See LootStoreItem::IsValid and the reference-processing path before authoring typed rewards.

A zero/negative Chance copied from older documentation may use obsolete conventions. This schema has an explicit QuestRequired field and typed ItemType. Check the loader before assigning special probability values.

## References and cycles

For a reference reward, Item identifies an entry in reference_loot_template according to the current reward discriminator. References allow reuse but can create cycles or missing links. Validate the entire dependency chain; SQL does not enforce it.

The type must be identified from the current LootMgr header. A diagnostic that treats every Item value as an ordinary item ID will report false errors for currencies and references.

## Inspection

```sql
SET @loot_entry = 0; -- replace with an existing loot definition
SELECT * FROM creature_loot_template
WHERE Entry = @loot_entry ORDER BY GroupId, ItemType, Item;

SELECT Entry, ItemType, Item, MinCount, MaxCount
FROM creature_loot_template
WHERE ItemType IN (0, 2) AND MinCount > MaxCount
LIMIT 100;
```

The count query checks the item/currency range invariant only. It excludes tracking-quest and reference count conventions. It does not validate roll totals, type-specific IDs, reference cycles, eligibility, or every loot table.

## Testing

Test the actual source in the correct difficulty and loot mode with a suitable character. Check quest eligibility and loot distribution, including references, currency rewards, counts, and alternative groups. Probability changes need repeated rolls or a review of the roll algorithm; one observed drop cannot confirm the intended rate.
