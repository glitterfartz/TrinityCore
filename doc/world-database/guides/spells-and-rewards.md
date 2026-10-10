# Spells, professions, and rewards

[Database documentation](../README.md)

## Spell supplements

Most spell definitions originate in client DB2/hotfix data. World tables supplement behavior: spell_proc for proc filters/rates, spell_custom_attr for server masks, spell_threat for threat, spell_target_position for fixed destinations, and spell_script_names for compiled spell/aura scripts.

spell_group and spell_group_stack_rules govern stacking associations. Group members can have signed/nested-group conventions; inspect SpellMgr before treating every member as a positive spell ID.

spell_linked_spell has signed cast/hit/aura/removal semantics selected by its type; do not normalize negative values. spell_learn_spell and spell_required affect learning dependencies. spell_area applies spells under area/quest/aura/race/gender conditions. spell_pet_auras and spell_totem_model support pet/totem behavior.

serverside_spell and serverside_spell_effect define server-only spell records. Effect type, aura, targets, scaling, and flags still follow current core spell definitions. A world SQL row alone cannot guarantee client presentation for a spell absent from client data.

See [spell enums](../reference/spell-enums.md) and the table-specific source sites.

## Professions

skill_discovery_template defines discovery chance. skill_extra_item_template configures specialization extra output. skill_perfect_item_template defines perfect-output substitutions. skill_fishing_base_level and skill_tiers supply area/threshold data.

Each profession table's probability and prerequisite interpretation is implementation-specific. Read its loader and crafting/fishing consumer before combining probabilities. Milling, prospecting, disenchanting, and fishing reward data use the typed loot tables.

## Players, pets, and character presets

playercreateinfo and its extensions establish starting position, actions, items, and spells. Race/class masks are distinct from plain race/class IDs. player_classlevelstats, player_racestats, player_xp_for_level, and pet_levelstats supply base stats/experience.

player_factionchange tables map faction counterparts. Counterparts should be validated against the proper external/client or quest records, not assumed to exist because IDs are nonzero.

character_template and character_template_class describe creation presets. race_unlock_requirement and class_expansion_requirement gate eligibility. Battle-pet tables constrain species breed/quality data.

## Rewards and choices

achievement_reward adds titles and mail. criteria_data and achievement_scripts add requirements or script checks. guild_rewards and guild_rewards_req_achievements configure guild offerings. mail_level_reward supplies level-triggered mail; mail_loot_template supplies mail reward loot.

playerchoice defines choice UI; playerchoice_response and reward extensions define selectable responses and rewards. Include the full choice/response identity when joining currency, faction, fixed-item, or item-choice rewards. Maw-power data augments a response's presentation/behavior.

reputation_reward_rate and reputation_spillover_template configure rate multipliers and spillover, while creature_onkill_reputation configures kill rewards. Rank caps and masks follow the current reputation code.

## Common validation issues

Check external spell/item/currency/faction/title/achievement existence, registered scripts, signed/nested relationships, type-specific flag sets, prerequisites, player eligibility, and reward delivery. Test both qualifying and nonqualifying characters. Inspect startup validation logs before debugging UI symptoms.
