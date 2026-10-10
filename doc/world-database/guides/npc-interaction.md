# Gossip, vendors, and trainers

[Database documentation](../README.md)

## Gossip chain

creature_template_gossip associates NPC templates with menus. gossip_menu selects NPC text. npc_text selects weighted broadcast-text records. gossip_menu_option defines choices and their text, broadcast-text references, language, flags, interaction category, navigation, point of interest, optional spell, and confirmation.

MenuID and OptionID together identify an option. GossipOptionID and GossipNpcOptionID are separate modern fields; do not substitute an older option_id interpretation. OptionNpc uses its current discriminator, not arbitrary numeric values from another branch.

ActionMenuID opens a submenu and ActionPoiID selects a map marker. BoxCoded, BoxMoney, BoxText, and BoxBroadcastTextID configure confirmation. BoxMoney is copper. Conditions can control menu/option availability. SmartAI or compiled scripts may handle selections instead of simple navigation.

## Vendor stock

npc_vendor belongs to creature template entries. Review the offering NPC's interaction flags, each row's type discriminator, stock limit and replenishment time, extended cost, player condition, and bonus/context fields. Some offerings are currencies rather than ordinary item IDs.

game_event_npc_vendor adds event-dependent offerings. Existing stock may depend on game events and conditions. A valid item ID alone does not make an offering visible.

## Trainers

creature_trainer links an NPC/gossip selection to trainer. trainer_spell contains costs and prerequisites; trainer_locale translates the greeting. Trainer IDs are distinct from NPC template entries even if an existing dataset chooses matching numbers.

Validate spell existence, prerequisite spells/skills/levels, trainer category and requirements, and the interaction path that selects that trainer.

## Inspection

```sql
SET @menu_id = 0; -- replace
SELECT * FROM gossip_menu WHERE MenuID = @menu_id;
SELECT * FROM gossip_menu_option WHERE MenuID = @menu_id ORDER BY OptionID;

SET @creature_entry = 0; -- replace
SELECT * FROM npc_vendor WHERE entry = @creature_entry;
SELECT * FROM creature_trainer LIMIT 10;
SELECT * FROM trainer LIMIT 10;
```

## Common failures

Missing interaction flags, a menu not associated with the template, failing conditions, missing broadcast-text/client records, invalid typed offerings, wrong trainer selection, and unregistered scripts can all produce empty or inactive UI. Check the selected menu and option identity in SmartAI gossip events, including whether the action uses the correct invoker target.
