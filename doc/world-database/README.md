# TrinityCore world database

Documentation for the connected **master** world database, captured **2026-10-09**. Core: `914a6f655c973d57c392ae78c92c14c5376f8e38`; database: **TDB 1210.26091**; cache ID: **26091**. The database version row matches the inspected checkout.

Coverage: **246 base tables, 3 views, 1,994 columns**. Every object has a page containing exact captured SQL types, nullability, default metadata, indexes, inspection SQL, and available runtime evidence. This is complete schema coverage; independently unresolved field meanings are marked explicitly rather than guessed.

## Start here

- [Conventions and version scope](conventions.md)
- [Logical relationships](relationships.md)
- [Creatures and spawns](guides/creatures.md)
- [Gameobjects](guides/gameobjects.md)
- [Quest authoring hub](guides/quests.md)
- [Loot](guides/loot.md)
- [Gossip, vendors, and trainers](guides/npc-interaction.md)
- [SmartAI](guides/smartai.md)
- [Conditions](guides/conditions.md)
- [Movement, events, pools, and phasing](guides/world-content.md)
- [Spells, professions, and rewards](guides/spells-and-rewards.md)
- [Localization](guides/localization.md)
- [Operations and troubleshooting](guides/operations.md)
- [Sources and evidence limits](sources.md)
- [Maintenance and regeneration](maintenance.md)
- [Captured schema metadata](schema-snapshot.md)
- [Coverage report](coverage.md)
- [Verification and repeatable checks](verification.md)

## Enum and data references

- [Conditions Enums](reference/conditions-enums.md)
- [Smartai Enums](reference/smartai-enums.md)
- [Quest Enums](reference/quest-enums.md)
- [Areatrigger Enums](reference/areatrigger-enums.md)
- [Spawn Enums](reference/spawn-enums.md)
- [Loot Enums](reference/loot-enums.md)
- [Disable Enums](reference/disable-enums.md)
- [Spell Enums](reference/spell-enums.md)
- [World Enums](reference/world-enums.md)
- [Gameobject Data0–Data34 layouts](reference/gameobject-data.md)

## Table index

### Achievements

| Object | Purpose |
| --- | --- |
| [achievement_dbc](tables/achievement_dbc.md) | Server-side achievement records supplementing client achievement data. |
| [achievement_reward](tables/achievement_reward.md) | Defines titles and mail rewards granted for achievements. |
| [achievement_reward_locale](tables/achievement_reward_locale.md) | Localized text for achievement_reward. Parent identity fields and locale jointly select each translation. |
| [achievement_scripts](tables/achievement_scripts.md) | Binds achievement checks to compiled C++ scripts. |
| [criteria_data](tables/criteria_data.md) | Additional typed requirements for achievement criteria. |

### Area triggers

| Object | Purpose |
| --- | --- |
| [areatrigger](tables/areatrigger.md) | Persistent area-trigger spawn placements. |
| [areatrigger_create_properties](tables/areatrigger_create_properties.md) | Shape, motion, and timing properties for spell-created area triggers. |
| [areatrigger_create_properties_orbit](tables/areatrigger_create_properties_orbit.md) | Orbital motion configuration for an area-trigger creation property. |
| [areatrigger_create_properties_polygon_vertex](tables/areatrigger_create_properties_polygon_vertex.md) | Ordered polygon vertices for an area-trigger creation property. |
| [areatrigger_create_properties_spline_point](tables/areatrigger_create_properties_spline_point.md) | Ordered spline control points for an area-trigger creation property. |
| [areatrigger_involvedrelation](tables/areatrigger_involvedrelation.md) | Connects client area triggers to quest exploration/completion credit. |
| [areatrigger_scripts](tables/areatrigger_scripts.md) | Binds client area-trigger handling to compiled scripts. |
| [areatrigger_tavern](tables/areatrigger_tavern.md) | Marks client area triggers as resting locations. |
| [areatrigger_teleport](tables/areatrigger_teleport.md) | Teleport destinations and requirements for client area triggers. |
| [areatrigger_template](tables/areatrigger_template.md) | Defines an area trigger's shape and base behavior. |
| [areatrigger_template_actions](tables/areatrigger_template_actions.md) | Actions associated with an area-trigger template. |

### Conversations and scenes

| Object | Purpose |
| --- | --- |
| [conversation_actors](tables/conversation_actors.md) | Actor slots and creature references for conversations. |
| [conversation_line_template](tables/conversation_line_template.md) | Timing and actor information for conversation lines. |
| [conversation_template](tables/conversation_template.md) | Conversation definitions, initial lines, texture kits, and script bindings. |
| [scene_template](tables/scene_template.md) | Scene package configuration and compiled scene script bindings. |

### Creatures

| Object | Purpose |
| --- | --- |
| [creature](tables/creature.md) | Persistent NPC spawns: template, placement, phase, difficulty, and per-spawn overrides. |
| [creature_addon](tables/creature_addon.md) | Per-spawn path, appearance, emote, and aura configuration. |
| [creature_classlevelstats](tables/creature_classlevelstats.md) | Base creature combat statistics by class and level. |
| [creature_equip_template](tables/creature_equip_template.md) | Named equipment sets for creature templates. |
| [creature_formations](tables/creature_formations.md) | Leader/member associations and follow geometry for creature formations. |
| [creature_immunities](tables/creature_immunities.md) | Reusable sets of school, mechanic, effect, and other creature immunities. |
| [creature_model_info](tables/creature_model_info.md) | Display-model collision dimensions and gender/model relationships. |
| [creature_movement_info](tables/creature_movement_info.md) | Movement speed/timing information. |
| [creature_movement_override](tables/creature_movement_override.md) | Per-spawn overrides of creature movement capabilities. |
| [creature_onkill_reputation](tables/creature_onkill_reputation.md) | Faction reputation awarded when a creature is killed. |
| [creature_quest_currency](tables/creature_quest_currency.md) | Currency relevant to a creature's quest interactions. |
| [creature_questender](tables/creature_questender.md) | Creature templates that accept a quest turn-in. |
| [creature_questitem](tables/creature_questitem.md) | Quest-related item annotations for creature templates. |
| [creature_queststarter](tables/creature_queststarter.md) | Creature templates that offer quests. |
| [creature_static_flags_override](tables/creature_static_flags_override.md) | Difficulty-specific static creature flag overrides. |
| [creature_summon_groups](tables/creature_summon_groups.md) | Groups of creatures summoned together by a typed summoner. |
| [creature_summoned_data](tables/creature_summoned_data.md) | Template data specific to summoned creatures. |
| [creature_template](tables/creature_template.md) | Base NPC definitions shared by creature spawns and summoned creatures. |
| [creature_template_addon](tables/creature_template_addon.md) | Template-level defaults for paths, appearance, emotes, and auras. |
| [creature_template_difficulty](tables/creature_template_difficulty.md) | Difficulty-specific creature tuning, loot references, and static flags. |
| [creature_template_gossip](tables/creature_template_gossip.md) | Menus available to a creature template. |
| [creature_template_locale](tables/creature_template_locale.md) | Localized text for creature_template. Parent identity fields and locale jointly select each translation. |
| [creature_template_model](tables/creature_template_model.md) | Weighted display-model choices for creature templates. |
| [creature_template_movement](tables/creature_template_movement.md) | Template-level movement capabilities. |
| [creature_template_resistance](tables/creature_template_resistance.md) | Creature template resistance by spell school. |
| [creature_template_sparring](tables/creature_template_sparring.md) | Sparring behavior and health limits for creature templates. |
| [creature_template_spell](tables/creature_template_spell.md) | Spells assigned to creature template slots. |
| [creature_text](tables/creature_text.md) | Groups of NPC speech lines, probabilities, emotes, sounds, and broadcast-text references. |
| [creature_text_locale](tables/creature_text_locale.md) | Localized text for creature_text. Parent identity fields and locale jointly select each translation. |
| [creature_trainer](tables/creature_trainer.md) | Connects NPC templates and gossip selections to trainer definitions. |

### Diagnostic views

| Object | Purpose |
| --- | --- |
| [vw_conditions_with_labels](tables/vw_conditions_with_labels.md) | Custom diagnostic view replacing condition/source numbers with labels; its CASE definitions require auditing. |
| [vw_disables_with_labels](tables/vw_disables_with_labels.md) | Custom diagnostic view replacing disable source numbers with labels. |
| [vw_smart_scripts_with_labels](tables/vw_smart_scripts_with_labels.md) | Custom diagnostic view replacing SmartAI event/action/target numbers with labels; some mappings are older than this core. |

### Gameobjects

| Object | Purpose |
| --- | --- |
| [gameobject](tables/gameobject.md) | Persistent gameobject spawns and their placements, rotations, phases, and difficulty settings. |
| [gameobject_addon](tables/gameobject_addon.md) | Per-spawn gameobject addon configuration. |
| [gameobject_overrides](tables/gameobject_overrides.md) | Per-spawn gameobject faction and flag overrides. |
| [gameobject_questender](tables/gameobject_questender.md) | Gameobject templates that accept quest turn-ins. |
| [gameobject_questitem](tables/gameobject_questitem.md) | Quest-related item annotations for gameobject templates. |
| [gameobject_queststarter](tables/gameobject_queststarter.md) | Gameobject templates that offer quests. |
| [gameobject_template](tables/gameobject_template.md) | Shared object definitions; Data0–Data34 are interpreted according to object type. |
| [gameobject_template_addon](tables/gameobject_template_addon.md) | Template-level gameobject faction, flags, art, and other addon defaults. |
| [gameobject_template_locale](tables/gameobject_template_locale.md) | Localized text for gameobject_template. Parent identity fields and locale jointly select each translation. |

### Garrisons

| Object | Purpose |
| --- | --- |
| [garrison_follower_class_spec_abilities](tables/garrison_follower_class_spec_abilities.md) | Ability choices for garrison follower class specializations. |
| [garrison_plot_finalize_info](tables/garrison_plot_finalize_info.md) | Faction-specific plot completion positions and animations. |

### Guilds and rewards

| Object | Purpose |
| --- | --- |
| [guild_rewards](tables/guild_rewards.md) | Items available as guild rewards and their requirements. |
| [guild_rewards_req_achievements](tables/guild_rewards_req_achievements.md) | Achievement requirements for guild reward items. |

### Instances and scenarios

| Object | Purpose |
| --- | --- |
| [instance_spawn_groups](tables/instance_spawn_groups.md) | Controls spawn groups using instance boss-state conditions. |
| [instance_template](tables/instance_template.md) | Instance map parent relationships and compiled instance scripts. |
| [lfg_dungeon_rewards](tables/lfg_dungeon_rewards.md) | Quest rewards for dungeon-finder completion by level. |
| [lfg_dungeon_template](tables/lfg_dungeon_template.md) | Dungeon-finder entry locations and custom dungeon settings. |
| [scenario_poi](tables/scenario_poi.md) | Scenario map-overlay blob metadata. |
| [scenario_poi_points](tables/scenario_poi_points.md) | Ordered coordinates composing scenario POI blobs. |
| [scenarios](tables/scenarios.md) | Map/difficulty scenario assignments. |

### Items

| Object | Purpose |
| --- | --- |
| [item_random_bonus_list_template](tables/item_random_bonus_list_template.md) | Weighted item bonus-list selections. |
| [item_script_names](tables/item_script_names.md) | Compiled item-use script bindings. |
| [item_template_addon](tables/item_template_addon.md) | Server-only item behavior supplementing client/hotfix item definitions. |
| [page_text](tables/page_text.md) | Chained readable pages used by items and other content. |
| [page_text_locale](tables/page_text_locale.md) | Localized text for page_text. Parent identity fields and locale jointly select each translation. |

### Loot

| Object | Purpose |
| --- | --- |
| [creature_loot_template](tables/creature_loot_template.md) | Loot rows for creature sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [disenchant_loot_template](tables/disenchant_loot_template.md) | Loot rows for disenchant sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [fishing_loot_template](tables/fishing_loot_template.md) | Loot rows for fishing sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [gameobject_loot_template](tables/gameobject_loot_template.md) | Loot rows for gameobject sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [item_loot_template](tables/item_loot_template.md) | Loot rows for item sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [mail_loot_template](tables/mail_loot_template.md) | Loot rows for mail sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [milling_loot_template](tables/milling_loot_template.md) | Loot rows for milling sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [pickpocketing_loot_template](tables/pickpocketing_loot_template.md) | Loot rows for pickpocketing sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [prospecting_loot_template](tables/prospecting_loot_template.md) | Loot rows for prospecting sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [reference_loot_template](tables/reference_loot_template.md) | Loot rows for reference sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [skinning_loot_template](tables/skinning_loot_template.md) | Loot rows for skinning sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |
| [spell_loot_template](tables/spell_loot_template.md) | Loot rows for spell sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide. |

### Movement

| Object | Purpose |
| --- | --- |
| [script_spline_chain_meta](tables/script_spline_chain_meta.md) | Sequence and timing metadata for scripted spline chains. |
| [script_spline_chain_waypoints](tables/script_spline_chain_waypoints.md) | Ordered coordinates for scripted spline chains. |
| [waypoint_path](tables/waypoint_path.md) | Reusable waypoint paths and movement configuration. |
| [waypoint_path_node](tables/waypoint_path_node.md) | Ordered positions, orientation, and pause delays for waypoint paths. |

### NPC interaction

| Object | Purpose |
| --- | --- |
| [gossip_menu](tables/gossip_menu.md) | NPC dialogue menus and their NPC-text records. |
| [gossip_menu_addon](tables/gossip_menu_addon.md) | Additional menu-level gossip configuration. |
| [gossip_menu_option](tables/gossip_menu_option.md) | Selectable gossip options and their navigation, interaction, and confirmation settings. |
| [gossip_menu_option_locale](tables/gossip_menu_option_locale.md) | Localized text for gossip_menu_option. Parent identity fields and locale jointly select each translation. |
| [npc_spellclick_spells](tables/npc_spellclick_spells.md) | Spells cast when players interact with spell-click NPCs. |
| [npc_text](tables/npc_text.md) | Weighted broadcast-text choices used by gossip menus. |
| [npc_vendor](tables/npc_vendor.md) | NPC vendor stock, prices, conditions, and item/currency offerings. |
| [trainer](tables/trainer.md) | Trainer identity, category, requirements, and greeting. |
| [trainer_locale](tables/trainer_locale.md) | Localized text for trainer. Parent identity fields and locale jointly select each translation. |
| [trainer_spell](tables/trainer_spell.md) | Spells offered by trainers, costs, and prerequisite skills/spells/levels. |

### Phasing

| Object | Purpose |
| --- | --- |
| [phase_area](tables/phase_area.md) | Phases applied within specific areas. |
| [phase_name](tables/phase_name.md) | Human-readable phase names for authoring and diagnostics. |
| [terrain_swap_defaults](tables/terrain_swap_defaults.md) | Default terrain replacement maps. |
| [terrain_worldmap](tables/terrain_worldmap.md) | World-map presentation for terrain swaps. |

### Player choices

| Object | Purpose |
| --- | --- |
| [playerchoice](tables/playerchoice.md) | Player-choice windows and presentation settings. |
| [playerchoice_locale](tables/playerchoice_locale.md) | Localized text for playerchoice. Parent identity fields and locale jointly select each translation. |
| [playerchoice_response](tables/playerchoice_response.md) | Responses offered by player-choice windows. |
| [playerchoice_response_locale](tables/playerchoice_response_locale.md) | Localized text for playerchoice_response. Parent identity fields and locale jointly select each translation. |
| [playerchoice_response_maw_power](tables/playerchoice_response_maw_power.md) | Maw-power presentation/configuration for player-choice responses. |
| [playerchoice_response_reward](tables/playerchoice_response_reward.md) | Base rewards attached to player-choice responses. |
| [playerchoice_response_reward_currency](tables/playerchoice_response_reward_currency.md) | Currency rewards for a player-choice response. |
| [playerchoice_response_reward_faction](tables/playerchoice_response_reward_faction.md) | Faction reputation rewards for a player-choice response. |
| [playerchoice_response_reward_item](tables/playerchoice_response_reward_item.md) | Fixed item rewards for a player-choice response. |
| [playerchoice_response_reward_item_choice](tables/playerchoice_response_reward_item_choice.md) | Selectable item rewards for a player-choice response. |

### Players

| Object | Purpose |
| --- | --- |
| [character_template](tables/character_template.md) | Named character creation presets. |
| [character_template_class](tables/character_template_class.md) | Race, faction, and class combinations for character presets. |
| [player_classlevelstats](tables/player_classlevelstats.md) | Base player class statistics by level. |
| [player_factionchange_achievement](tables/player_factionchange_achievement.md) | Alliance/Horde mappings for achievement during player faction changes. |
| [player_factionchange_quests](tables/player_factionchange_quests.md) | Alliance/Horde mappings for quests during player faction changes. |
| [player_factionchange_reputations](tables/player_factionchange_reputations.md) | Alliance/Horde mappings for reputations during player faction changes. |
| [player_factionchange_spells](tables/player_factionchange_spells.md) | Alliance/Horde mappings for spells during player faction changes. |
| [player_factionchange_titles](tables/player_factionchange_titles.md) | Alliance/Horde mappings for titles during player faction changes. |
| [player_racestats](tables/player_racestats.md) | Base racial statistics. |
| [player_xp_for_level](tables/player_xp_for_level.md) | Experience required to advance from each player level. |
| [playercreateinfo](tables/playercreateinfo.md) | Starting map and position by race and class. |
| [playercreateinfo_action](tables/playercreateinfo_action.md) | Starting action-bar buttons by race and class. |
| [playercreateinfo_cast_spell](tables/playercreateinfo_cast_spell.md) | Spells cast during character creation. |
| [playercreateinfo_item](tables/playercreateinfo_item.md) | Additional starting items by race and class. |
| [playercreateinfo_spell_custom](tables/playercreateinfo_spell_custom.md) | Custom starting spells selected by race/class masks. |

### Professions

| Object | Purpose |
| --- | --- |
| [skill_discovery_template](tables/skill_discovery_template.md) | Random recipe discovery chances during crafting. |
| [skill_extra_item_template](tables/skill_extra_item_template.md) | Extra-item creation chances for profession specializations. |
| [skill_fishing_base_level](tables/skill_fishing_base_level.md) | Required base fishing skill by area. |
| [skill_perfect_item_template](tables/skill_perfect_item_template.md) | Perfect-result crafting substitutions and probabilities. |
| [skill_tiers](tables/skill_tiers.md) | Skill tier thresholds. |

### PvP and pets

| Object | Purpose |
| --- | --- |
| [battle_pet_breeds](tables/battle_pet_breeds.md) | Allowed breeds for battle-pet species. |
| [battle_pet_quality](tables/battle_pet_quality.md) | Quality configuration for battle-pet species. |
| [battlefield_template](tables/battlefield_template.md) | Configuration and script bindings for battlefield systems. |
| [battleground_scripts](tables/battleground_scripts.md) | Compiled script bindings for battleground types. |
| [battleground_template](tables/battleground_template.md) | Battleground team sizes, level limits, and starting locations. |
| [battlemaster_entry](tables/battlemaster_entry.md) | Maps NPC templates to the battleground types they offer. |
| [pet_levelstats](tables/pet_levelstats.md) | Base pet statistics by creature and level. |
| [pet_name_generation](tables/pet_name_generation.md) | Name fragments used to generate pet names. |

### Quests

| Object | Purpose |
| --- | --- |
| [quest_completion_log_conditional](tables/quest_completion_log_conditional.md) | Condition-specific quest completion-log text. |
| [quest_description_conditional](tables/quest_description_conditional.md) | Condition-specific quest description text. |
| [quest_details](tables/quest_details.md) | Emotes and delays shown when offering quest details. |
| [quest_greeting](tables/quest_greeting.md) | Creature/gameobject quest greeting text and emotes. |
| [quest_greeting_locale](tables/quest_greeting_locale.md) | Localized text for quest_greeting. Parent identity fields and locale jointly select each translation. |
| [quest_mail_sender](tables/quest_mail_sender.md) | Overrides the sender of a quest's reward mail. |
| [quest_objectives](tables/quest_objectives.md) | Typed objective requirements and progress storage for quests. |
| [quest_objectives_completion_effect](tables/quest_objectives_completion_effect.md) | Effects played when quest objectives complete. |
| [quest_objectives_locale](tables/quest_objectives_locale.md) | Localized text for quest_objectives. Parent identity fields and locale jointly select each translation. |
| [quest_offer_reward](tables/quest_offer_reward.md) | Reward-dialogue text and emotes. |
| [quest_offer_reward_conditional](tables/quest_offer_reward_conditional.md) | Condition-specific reward-dialogue text. |
| [quest_offer_reward_locale](tables/quest_offer_reward_locale.md) | Localized text for quest_offer_reward. Parent identity fields and locale jointly select each translation. |
| [quest_poi](tables/quest_poi.md) | Quest objective map-overlay blob metadata. |
| [quest_poi_points](tables/quest_poi_points.md) | Ordered coordinates composing quest POI blobs. |
| [quest_pool_members](tables/quest_pool_members.md) | Quest membership in rotating quest pools. |
| [quest_pool_template](tables/quest_pool_template.md) | Rotating quest-pool definitions and selection settings. |
| [quest_request_items](tables/quest_request_items.md) | Progress-dialogue text and emotes for incomplete/complete objectives. |
| [quest_request_items_conditional](tables/quest_request_items_conditional.md) | Condition-specific quest progress-dialogue text. |
| [quest_request_items_locale](tables/quest_request_items_locale.md) | Localized text for quest_request_items. Parent identity fields and locale jointly select each translation. |
| [quest_reward_choice_items](tables/quest_reward_choice_items.md) | Additional typed choice rewards for quests. |
| [quest_reward_display_spell](tables/quest_reward_display_spell.md) | Spells displayed as quest rewards. |
| [quest_reward_house_decor](tables/quest_reward_house_decor.md) | Housing decoration rewards for quests. |
| [quest_reward_house_room](tables/quest_reward_house_room.md) | Housing room rewards for quests. |
| [quest_template](tables/quest_template.md) | Quest identity, presentation, reward, race eligibility, and flag data. |
| [quest_template_addon](tables/quest_template_addon.md) | Server-side prerequisites, chain relationships, skills, scripts, and other quest settings. |
| [quest_template_locale](tables/quest_template_locale.md) | Localized text for quest_template. Parent identity fields and locale jointly select each translation. |
| [quest_treasure_pickers](tables/quest_treasure_pickers.md) | Treasure-picker rewards attached to quests. |
| [quest_visual_effect](tables/quest_visual_effect.md) | Visual effects attached to quests. |

### Reputation

| Object | Purpose |
| --- | --- |
| [reputation_reward_rate](tables/reputation_reward_rate.md) | Faction-specific reputation rate multipliers by reward source. |
| [reputation_spillover_template](tables/reputation_spillover_template.md) | Reputation spillover destinations, rates, and rank limits. |

### Spawns

| Object | Purpose |
| --- | --- |
| [pool_members](tables/pool_members.md) | Typed creature, gameobject, or child-pool membership and selection chances. |
| [pool_template](tables/pool_template.md) | Spawn-pool definitions and maximum active member counts. |
| [spawn_group](tables/spawn_group.md) | Associates typed spawn IDs with spawn-group templates. |
| [spawn_group_template](tables/spawn_group_template.md) | Spawn-group names and behavior flags. |
| [spawn_tracking](tables/spawn_tracking.md) | Associates typed spawns with tracking definitions. |
| [spawn_tracking_quest_objective](tables/spawn_tracking_quest_objective.md) | Quest objectives associated with spawn tracking. |
| [spawn_tracking_state](tables/spawn_tracking_state.md) | State configuration for spawn tracking. |
| [spawn_tracking_template](tables/spawn_tracking_template.md) | Reusable spawn-tracking definitions. |

### Spells

| Object | Purpose |
| --- | --- |
| [serverside_spell](tables/serverside_spell.md) | Server-only spell definitions not supplied by client spell data. |
| [serverside_spell_effect](tables/serverside_spell_effect.md) | Effect definitions for server-only spells. |
| [spell_area](tables/spell_area.md) | Area, quest, race, gender, and aura requirements for applying spells. |
| [spell_custom_attr](tables/spell_custom_attr.md) | Server-specific spell attribute masks. |
| [spell_enchant_proc_data](tables/spell_enchant_proc_data.md) | Proc chances and conditions for enchantment spells. |
| [spell_group](tables/spell_group.md) | Spells and nested groups used for aura stacking rules. |
| [spell_group_stack_rules](tables/spell_group_stack_rules.md) | Stacking rules applied to spell groups. |
| [spell_learn_spell](tables/spell_learn_spell.md) | Secondary spells taught by learning a source spell. |
| [spell_linked_spell](tables/spell_linked_spell.md) | Typed cast/hit/aura links between spells, including signed removal semantics. |
| [spell_pet_auras](tables/spell_pet_auras.md) | Pet auras selected by owner spell and pet entry. |
| [spell_proc](tables/spell_proc.md) | Overrides spell proc filters, chances, cooldowns, and charges. |
| [spell_required](tables/spell_required.md) | Required prerequisite spells for learning spells. |
| [spell_script_names](tables/spell_script_names.md) | Compiled spell/aura script bindings. |
| [spell_target_position](tables/spell_target_position.md) | Fixed positional targets for spell effects. |
| [spell_threat](tables/spell_threat.md) | Spell threat additions, multipliers, and attack-power scaling. |
| [spell_totem_model](tables/spell_totem_model.md) | Totem display model by spell and race. |

### Vehicles

| Object | Purpose |
| --- | --- |
| [vehicle_accessory](tables/vehicle_accessory.md) | Per-spawn NPC passengers/accessories for vehicles. |
| [vehicle_seat_addon](tables/vehicle_seat_addon.md) | Additional vehicle-seat behavior and attachment settings. |
| [vehicle_template](tables/vehicle_template.md) | Server-specific vehicle configuration. |
| [vehicle_template_accessory](tables/vehicle_template_accessory.md) | Template-level NPC passengers/accessories for vehicles. |

### World events

| Object | Purpose |
| --- | --- |
| [game_event](tables/game_event.md) | Calendar and progression definitions for world events. |
| [game_event_arena_seasons](tables/game_event_arena_seasons.md) | Connects scheduled game events to arena seasons. |
| [game_event_condition](tables/game_event_condition.md) | Progress targets used by world-event conditions. |
| [game_event_creature](tables/game_event_creature.md) | Creature spawn participation in world events. |
| [game_event_creature_quest](tables/game_event_creature_quest.md) | Creature quest availability during a world event. |
| [game_event_gameobject](tables/game_event_gameobject.md) | Gameobject spawn participation in world events. |
| [game_event_gameobject_quest](tables/game_event_gameobject_quest.md) | Gameobject quest availability during a world event. |
| [game_event_model_equip](tables/game_event_model_equip.md) | Event-specific creature model and equipment overrides. |
| [game_event_npc_vendor](tables/game_event_npc_vendor.md) | Vendor offerings enabled during a world event. |
| [game_event_npcflag](tables/game_event_npcflag.md) | Event-specific NPC interaction flag overrides. |
| [game_event_pool](tables/game_event_pool.md) | Spawn pools controlled by world events. |
| [game_event_prerequisite](tables/game_event_prerequisite.md) | Prerequisite world events for progression events. |
| [game_event_quest_condition](tables/game_event_quest_condition.md) | Quest contributions to world-event progress. |
| [game_event_seasonal_questrelation](tables/game_event_seasonal_questrelation.md) | Associates seasonal quests with events for reset tracking. |

### World systems and administration

| Object | Purpose |
| --- | --- |
| [access_requirement](tables/access_requirement.md) | Restricts instance entry by map and difficulty, level, items, quests, and achievements. |
| [blackmarket_template](tables/blackmarket_template.md) | Defines possible black-market auction offerings. |
| [class_expansion_requirement](tables/class_expansion_requirement.md) | Expansion eligibility for playable classes. |
| [command](tables/command.md) | Database overrides for chat-command help text. |
| [conditions](tables/conditions.md) | Reusable typed predicates that gate spells, gossip, loot, quests, spawns, and other content. |
| [destructible_hitpoint](tables/destructible_hitpoint.md) | Health configuration for destructible gameobjects. |
| [disables](tables/disables.md) | Typed switches disabling specific content or map-processing features. |
| [event_script_names](tables/event_script_names.md) | Compiled script bindings for game event identifiers. |
| [event_scripts](tables/event_scripts.md) | Legacy database command sequences triggered by events. |
| [exploration_basexp](tables/exploration_basexp.md) | Base exploration experience by player level. |
| [game_tele](tables/game_tele.md) | Named destinations used by game-master teleport commands. |
| [game_weather](tables/game_weather.md) | Zone weather probabilities by season. |
| [graveyard_zone](tables/graveyard_zone.md) | Associates zones and teams with resurrection locations. |
| [jump_charge_params](tables/jump_charge_params.md) | Motion parameters for jump and charge effects. |
| [linked_respawn](tables/linked_respawn.md) | Typed dependencies between creature and gameobject respawn schedules. |
| [mail_level_reward](tables/mail_level_reward.md) | Mail rewards sent when characters reach configured levels. |
| [mount_definitions](tables/mount_definitions.md) | Server-side mount definitions and associated spell data. |
| [outdoorpvp_template](tables/outdoorpvp_template.md) | Compiled script bindings for outdoor PvP systems. |
| [points_of_interest](tables/points_of_interest.md) | Map markers shown by gossip and navigation interactions. |
| [points_of_interest_locale](tables/points_of_interest_locale.md) | Localized text for points_of_interest. Parent identity fields and locale jointly select each translation. |
| [race_unlock_requirement](tables/race_unlock_requirement.md) | Playable race expansion and achievement requirements. |
| [smart_scripts](tables/smart_scripts.md) | Typed event/action/target programs for SmartAI and related script sources. |
| [transports](tables/transports.md) | Transport gameobject definitions and script bindings. |
| [trinity_string](tables/trinity_string.md) | Server messages and their locale variants. |
| [ui_map_quest](tables/ui_map_quest.md) | Quest associations with UI maps. |
| [ui_map_quest_line](tables/ui_map_quest_line.md) | Quest-line associations with UI maps. |
| [updates](tables/updates.md) | History and checksums of SQL migrations applied by the database updater. |
| [updates_include](tables/updates_include.md) | Directories and states controlling discovery of SQL migrations. |
| [version](tables/version.md) | Installed database release, core revision, and cache version. |
| [world_safe_locs](tables/world_safe_locs.md) | Safe locations used for resurrection and teleports. |
| [world_state](tables/world_state.md) | Server world-state defaults and configuration. |
