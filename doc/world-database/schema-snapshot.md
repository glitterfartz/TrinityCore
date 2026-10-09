# World schema snapshot

Captured through the read-only MySQL MCP connection on 2026-10-09. This machine-readable metadata is embedded in Markdown so the reference can be rebuilt without database credentials. Row data and connection secrets are excluded. See [maintenance](maintenance.md) before regenerating.

```json
{
  "captured": "2026-10-09",
  "version": [
    {
      "core_version": "TrinityCore rev. 914a6f655c97 2026-10-08 14:01:54 +0200 (master branch) (Windows, AMD64, Release, Static)",
      "core_revision": "914a6f655c97",
      "db_version": "TDB 1210.26091",
      "cache_id": 26091
    }
  ],
  "tables": [
    {
      "TABLE_NAME": "access_requirement",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "MyISAM",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Access Requirements"
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "MyISAM",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "MyISAM",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_scripts",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_involvedrelation",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Trigger System"
    },
    {
      "TABLE_NAME": "areatrigger_scripts",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_tavern",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Trigger System"
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Trigger System"
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_quality",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlefield_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlemaster_entry",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template_class",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "command",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Chat System"
    },
    {
      "TABLE_NAME": "conditions",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Condition System"
    },
    {
      "TABLE_NAME": "conversation_actors",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature System"
    },
    {
      "TABLE_NAME": "creature_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "creature_model_info",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature System (Model related info)"
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature OnKill Reputation gain"
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questender",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature System"
    },
    {
      "TABLE_NAME": "creature_questitem",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature System"
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature System"
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "MyISAM",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_trainer",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Achievment system"
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "This table contains data about destructible building health"
    },
    {
      "TABLE_NAME": "disables",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "event_script_names",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "exploration_basexp",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Exploration System"
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "game_event",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_condition",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_creature",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_pool",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Player System"
    },
    {
      "TABLE_NAME": "game_tele",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Tele Command"
    },
    {
      "TABLE_NAME": "game_weather",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Weather System"
    },
    {
      "TABLE_NAME": "gameobject",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Gameobject System"
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Gameobject System"
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Trigger System"
    },
    {
      "TABLE_NAME": "guild_rewards",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Item Random Enchantment System"
    },
    {
      "TABLE_NAME": "item_script_names",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "linked_respawn",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Creature Respawn Link System"
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Mail System"
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "mount_definitions",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Npc System"
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "OutdoorPvP Templates"
    },
    {
      "TABLE_NAME": "page_text",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Item System"
    },
    {
      "TABLE_NAME": "page_text_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Stores pet levels stats."
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_area",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_name",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Helper table to store names for phases"
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Stores levels stats."
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_racestats",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Stores race stats."
    },
    {
      "TABLE_NAME": "player_xp_for_level",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_mail_sender",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Quest System"
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Reputation spillover reputation gain"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenarios",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Skill Discovery System"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Skill Specialization System"
    },
    {
      "TABLE_NAME": "skill_fishing_base_level",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Fishing system"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Crafting Perfection System"
    },
    {
      "TABLE_NAME": "skill_tiers",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "smart_scripts",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_custom_attr",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "SpellInfo custom attributes"
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Spell enchant proc data"
    },
    {
      "TABLE_NAME": "spell_group",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Spell System"
    },
    {
      "TABLE_NAME": "spell_group_stack_rules",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Item System"
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Spell System"
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Loot System"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_required",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Spell Additinal Data"
    },
    {
      "TABLE_NAME": "spell_script_names",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Spell System"
    },
    {
      "TABLE_NAME": "spell_threat",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_locale",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Transports"
    },
    {
      "TABLE_NAME": "trinity_string",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "updates",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "List of all applied updates in this database."
    },
    {
      "TABLE_NAME": "updates_include",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "List of directories where we want to include sql updates."
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "version",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": "Version Notes"
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "TABLE_TYPE": "VIEW",
      "ENGINE": null,
      "TABLE_COLLATION": null,
      "TABLE_COMMENT": "VIEW"
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "TABLE_TYPE": "VIEW",
      "ENGINE": null,
      "TABLE_COLLATION": null,
      "TABLE_COMMENT": "VIEW"
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "TABLE_TYPE": "VIEW",
      "ENGINE": null,
      "TABLE_COLLATION": null,
      "TABLE_COMMENT": "VIEW"
    },
    {
      "TABLE_NAME": "waypoint_path",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "TABLE_TYPE": "BASE TABLE",
      "ENGINE": "InnoDB",
      "TABLE_COLLATION": "utf8mb4_unicode_ci",
      "TABLE_COMMENT": ""
    }
  ],
  "columns": [
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "mapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "difficulty",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "level_min",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "level_max",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "item",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "item2",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "quest_done_A",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "quest_done_H",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "completed_achievement",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "quest_failed_text",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "requiredFaction",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "mapID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "points",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "count",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "refAchievement",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "TitleA",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "TitleH",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "ItemID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "Sender",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "Subject",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "Body",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "MailTemplateID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "Locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "Subject",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "Body",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_scripts",
      "COLUMN_NAME": "AchievementId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "achievement_scripts",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "SpawnId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "MapId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "SpawnDifficulties",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PosX",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PosY",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PosZ",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "Orientation",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PhaseUseFlags",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PhaseId",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "PhaseGroup",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "AreaTriggerId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "IsAreatriggerCustom",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "MoveCurveId",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ScaleCurveId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "MorphCurveId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "FacingCurveId",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "AnimId",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "AnimKitId",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "DecalPropertiesId",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "SpellForVisuals",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "PositionalSoundKitId",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "TimeToTargetScale",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Speed",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "SpeedIsTime",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Shape",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData0",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData1",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData2",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData3",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData4",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData5",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData6",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ShapeData7",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Roll",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Pitch",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Yaw",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "TargetRoll",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "TargetPitch",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "TargetYaw",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "ExtraTimeForBlending",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "CircleRadius",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "BlendFromRadius",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "InitialAngle",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "ZOffset",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "CounterClockwise",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "CanLoop",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "VerticeX",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "VerticeY",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "VerticeTargetX",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "VerticeTargetY",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "X",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "Y",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "Z",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_involvedrelation",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Identifier"
    },
    {
      "TABLE_NAME": "areatrigger_involvedrelation",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "areatrigger_scripts",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_scripts",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_tavern",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Identifier"
    },
    {
      "TABLE_NAME": "areatrigger_tavern",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "COLUMN_NAME": "PortLocID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "ActionSetId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "ActionSetFlags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "AreaTriggerId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "IsCustom",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "ActionType",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "ActionParam",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "TargetType",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "COLUMN_NAME": "speciesId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "COLUMN_NAME": "breedId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_quality",
      "COLUMN_NAME": "speciesId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battle_pet_quality",
      "COLUMN_NAME": "quality",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlefield_template",
      "COLUMN_NAME": "TypeId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlefield_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlefield_template",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "COLUMN_NAME": "MapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "COLUMN_NAME": "BattlemasterListId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "AllianceStartLoc",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "HordeStartLoc",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "StartMaxDist",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "Weight",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(32)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "battlemaster_entry",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of a creature"
    },
    {
      "TABLE_NAME": "battlemaster_entry",
      "COLUMN_NAME": "bg_template",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Battleground template id"
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "marketId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "sellerNpc",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "itemEntry",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "quantity",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "minBid",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "duration",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "chance",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "bonusListIDs",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(70)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template",
      "COLUMN_NAME": "Description",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template",
      "COLUMN_NAME": "Level",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "TemplateId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "FactionGroup",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "3 - Alliance, 5 - Horde"
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "Class",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "ClassID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "RaceID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "ActiveExpansionLevel",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "AccountExpansionLevel",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "command",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(50)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "command",
      "COLUMN_NAME": "help",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceTypeOrReferenceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceGroup",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceEntry",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ElseGroup",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionTypeOrReference",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionTarget",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue1",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue2",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue3",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionStringValue1",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "NegativeCondition",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ErrorType",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ErrorTextId",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "ConversationId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "ConversationActorId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "ConversationActorGuid",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "CreatureId",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "CreatureDisplayInfoId",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "NoActorObject",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "ActivePlayerObject",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "UiCameraID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "ActorIdx",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "ChatType",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "FirstLineId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "TextureKitId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": "Creature Identifier"
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": "Map Identifier"
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "zoneId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Zone Identifier"
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "areaId",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Area Identifier"
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "spawnDifficulties",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "phaseUseFlags",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "PhaseId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "PhaseGroup",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "terrainSwapMap",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "modelid",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "equipment_id",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "spawntimesecs",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "120",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "wander_distance",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "currentwaypoint",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "curHealthPct",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "MovementType",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "npcflag",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "unit_flags",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "unit_flags2",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "unit_flags3",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "StringId",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "PathId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "mount",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "MountCreatureID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "StandState",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "AnimTier",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "VisFlags",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "SheathState",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "PvPFlags",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "emote",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "aiAnimKit",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "movementAnimKit",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "meleeAnimKit",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "visibilityDistanceType",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "auras",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "level",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "class",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "basemana",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "attackpower",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "rangedattackpower",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemID1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "AppearanceModID1",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemVisual1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemID2",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "AppearanceModID2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemVisual2",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemID3",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "AppearanceModID3",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ItemVisual3",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "leaderGUID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "memberGUID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "dist",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "angle",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "groupAI",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "point_1",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "point_2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "SchoolMask",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "DispelTypeMask",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "MechanicsMask",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "bigint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "Effects",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "Auras",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "ImmuneAoE",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "ImmuneChain",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "DisplayID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "BoundingRadius",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "CombatReach",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "DisplayID_Other_Gender",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "COLUMN_NAME": "MovementID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "creature_template.movementId value"
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "COLUMN_NAME": "WalkSpeed",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "COLUMN_NAME": "RunSpeed",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "SpawnId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "HoverInitiallyEnabled",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "Chase",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "Random",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "InteractionPauseTimer",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Time (in milliseconds) during which creature will not move after interaction with player"
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "creature_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Creature Identifier"
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "RewOnKillRepFaction1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "RewOnKillRepFaction2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "MaxStanding1",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "IsTeamAward1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "RewOnKillRepValue1",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "MaxStanding2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "IsTeamAward2",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "RewOnKillRepValue2",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "TeamDependent",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "COLUMN_NAME": "CreatureId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "COLUMN_NAME": "CurrencyId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questender",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Identifier"
    },
    {
      "TABLE_NAME": "creature_questender",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "creature_questender",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "CreatureEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "DifficultyID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "ItemId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Identifier"
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "SpawnId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "DifficultyId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags2",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags3",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags4",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags5",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags6",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags7",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "StaticFlags8",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "summonerId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "summonerType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "groupId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "summonType",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "summonTime",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summon_groups",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "CreatureIDVisibleToSummoner",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "GroundMountDisplayID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "FlyingMountDisplayID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "DespawnOnQuestsRemoved",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "KillCredit1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "KillCredit2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "femaleName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "subname",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "TitleAlt",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "IconName",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "RequiredExpansion",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "VignetteID",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "faction",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "npcflag",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "speed_walk",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Result of 2.5/2.5, most common value"
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "speed_run",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1.14286",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Result of 8.0/7.0, most common value"
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "scale",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "Classification",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "dmgschool",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "BaseAttackTime",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "RangeAttackTime",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "BaseVariance",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "RangeVariance",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "unit_class",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "unit_flags",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "unit_flags2",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "unit_flags3",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "family",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "trainer_class",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "VehicleId",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "AIName",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "MovementType",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "ExperienceModifier",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "RacialLeader",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "movementId",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "WidgetSetID",
      "ORDINAL_POSITION": 35,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "WidgetSetUnitConditionID",
      "ORDINAL_POSITION": 36,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "RegenHealth",
      "ORDINAL_POSITION": 37,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "CreatureImmunitiesId",
      "ORDINAL_POSITION": 38,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "flags_extra",
      "ORDINAL_POSITION": 39,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 40,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "StringId",
      "ORDINAL_POSITION": 41,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 42,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "PathId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "mount",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "MountCreatureID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "StandState",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "AnimTier",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "VisFlags",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "SheathState",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "PvPFlags",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "emote",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "aiAnimKit",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "movementAnimKit",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "meleeAnimKit",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "visibilityDistanceType",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "auras",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "DifficultyID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "LevelScalingDeltaMin",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "LevelScalingDeltaMax",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "ContentTuningID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "HealthScalingExpansion",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "HealthModifier",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "ManaModifier",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "ArmorModifier",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "DamageModifier",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "CreatureDifficultyID",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "TypeFlags",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "TypeFlags2",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "TypeFlags3",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "LootID",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "PickPocketLootID",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "SkinLootID",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "GoldMin",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "GoldMax",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags1",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags2",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags3",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags4",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags5",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags6",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags7",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "StaticFlags8",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "NameAlt",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "Title",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "TitleAlt",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "CreatureDisplayID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "DisplayScale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "Probability",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "CreatureId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "HoverInitiallyEnabled",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "Chase",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "Random",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "InteractionPauseTimer",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Time (in milliseconds) during which creature will not move after interaction with player"
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "School",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "Resistance",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "COLUMN_NAME": "NoNPCDamageBelowHealthPct",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "Spell",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "GroupID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Type",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Language",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Probability",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Emote",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Duration",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "Sound",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "SoundPlayType",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "BroadcastTextId",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "TextRange",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "GroupID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "Locale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "CreatureID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "TrainerID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "OptionID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "criteria_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "value1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "value2",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "COLUMN_NAME": "IntactNumHits",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "COLUMN_NAME": "DamagedNumHits",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "sourceType",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "params_0",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "params_1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_script_names",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_script_names",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "delay",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "command",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "datalong",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "datalong2",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "dataint",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "x",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "y",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "z",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "o",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "event_scripts",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "exploration_basexp",
      "COLUMN_NAME": "level",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "exploration_basexp",
      "COLUMN_NAME": "basexp",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "start_time",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "timestamp",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Absolute start date, the event will never start before"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "end_time",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "timestamp",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Absolute end date, the event will never start after"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "occurence",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "5184000",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Delay in minutes between occurences of the event"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "length",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "2592000",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Length in minutes of the event"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "holiday",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Client side holiday id"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "holidayStage",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "WorldStateId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Description of the event displayed in console"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "world_event",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "0 if normal event, 1 if world event"
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "announce",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "2",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "0 dont announce, 1 announce, 2 value from config"
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "COLUMN_NAME": "season",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Arena season number"
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "condition_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "req_num",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "max_world_state_field",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "done_world_state_field",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(25)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_creature",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event. Put negative entry to remove during event."
    },
    {
      "TABLE_NAME": "game_event_creature",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event."
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event. Put negative entry to remove during event."
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event."
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "COLUMN_NAME": "modelid",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "COLUMN_NAME": "equipment_id",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event."
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "slot",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "item",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "maxcount",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "incrtime",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "ExtendedCost",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "BonusListIDs",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "IgnoreFiltering",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "COLUMN_NAME": "npcflag",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_pool",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event. Put negative entry to remove during event."
    },
    {
      "TABLE_NAME": "game_event_pool",
      "COLUMN_NAME": "pool_entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Id of the pool"
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "COLUMN_NAME": "prerequisite_event",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event."
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "COLUMN_NAME": "condition_id",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "COLUMN_NAME": "num",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "COLUMN_NAME": "questId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "COLUMN_NAME": "eventEntry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Entry of the game event"
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "auto_increment",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "zone",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "spring_rain_chance",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "spring_snow_chance",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "spring_storm_chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "summer_rain_chance",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "summer_snow_chance",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "summer_storm_chance",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "fall_rain_chance",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "fall_snow_chance",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "fall_storm_chance",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "winter_rain_chance",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "winter_snow_chance",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "winter_storm_chance",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "25",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Gameobject Identifier"
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Map Identifier"
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "zoneId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Zone Identifier"
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "areaId",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Area Identifier"
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "spawnDifficulties",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "phaseUseFlags",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "PhaseId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "PhaseGroup",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "terrainSwapMap",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "rotation0",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "rotation1",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "rotation2",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "rotation3",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "spawntimesecs",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "animprogress",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "state",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "StringId",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "parent_rotation0",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "parent_rotation1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "parent_rotation2",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "parent_rotation3",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "invisibilityType",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "invisibilityValue",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "WorldEffectID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "AIAnimKitID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "COLUMN_NAME": "spawnId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "COLUMN_NAME": "faction",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "GameObjectEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "ItemId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "COLUMN_NAME": "quest",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest Identifier"
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "displayId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(200)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "IconName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "castBarCaption",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "unk1",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "size",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data0",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data1",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data2",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data3",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data4",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data5",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data6",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data7",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data8",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data9",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data10",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data11",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data12",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data13",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data14",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data15",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data16",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data17",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data18",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data19",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data20",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data21",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data22",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data23",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data24",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data25",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data26",
      "ORDINAL_POSITION": 35,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data27",
      "ORDINAL_POSITION": 36,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data28",
      "ORDINAL_POSITION": 37,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data29",
      "ORDINAL_POSITION": 38,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data30",
      "ORDINAL_POSITION": 39,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data31",
      "ORDINAL_POSITION": 40,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data32",
      "ORDINAL_POSITION": 41,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data33",
      "ORDINAL_POSITION": 42,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "Data34",
      "ORDINAL_POSITION": 43,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "ContentTuningId",
      "ORDINAL_POSITION": 44,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "RequiredLevel",
      "ORDINAL_POSITION": 45,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "AIName",
      "ORDINAL_POSITION": 46,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 47,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "StringId",
      "ORDINAL_POSITION": 48,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 49,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "faction",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "mingold",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "maxgold",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "artkit0",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "artkit1",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "artkit2",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "artkit3",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "artkit4",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "WorldEffectID",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "AIAnimKitID",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "castBarCaption",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "unk1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "COLUMN_NAME": "classSpecId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "COLUMN_NAME": "abilityId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "garrPlotInstanceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeGameObjectId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeX",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeY",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeZ",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeO",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "hordeAnimKitId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceGameObjectId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceX",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceY",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceZ",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceO",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "allianceAnimKitId",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu",
      "COLUMN_NAME": "TextID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "COLUMN_NAME": "FriendshipFactionID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "COLUMN_NAME": "LfgDungeonsID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "GossipOptionID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OptionID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OptionNpc",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OptionText",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OptionBroadcastTextID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "Language",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "ActionMenuID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "ActionPoiID",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "GossipNpcOptionID",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "BoxCoded",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "BoxMoney",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "BoxText",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "BoxBroadcastTextID",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OverrideIconID",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "MenuID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "OptionID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "Locale",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "OptionText",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "BoxText",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "COLUMN_NAME": "GhostZone",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards",
      "COLUMN_NAME": "ItemID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards",
      "COLUMN_NAME": "MinGuildRep",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards",
      "COLUMN_NAME": "RaceMask",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards",
      "COLUMN_NAME": "Cost",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "COLUMN_NAME": "ItemID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "COLUMN_NAME": "AchievementRequired",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "instanceMapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "bossStateId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "bossStates",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "spawnGroupId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_template",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_template",
      "COLUMN_NAME": "parent",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "instance_template",
      "COLUMN_NAME": "script",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(128)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "COLUMN_NAME": "BonusListID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_script_names",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_script_names",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "FlagsCu",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "FoodType",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "MinMoneyLoot",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "MaxMoneyLoot",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "SpellPPMChance",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "RandomBonusListTemplateId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "QuestLogItemId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "speed",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "42",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "treatSpeedAsMoveTimeSeconds",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "unlimitedSpeed",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "minHeight",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "maxHeight",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "spellVisualId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "progressCurveId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "parabolicCurveId",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "triggerSpellId",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "dungeonId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Dungeon entry from dbc"
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "maxLevel",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Max level at which this reward is rewarded"
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "firstQuestId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest id with rewards for first dungeon this day"
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "otherQuestId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Quest id with rewards for Nth dungeon this day"
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "dungeonId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Unique id from LFGDungeons.dbc"
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "requiredItemLevel",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "linked_respawn",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "linked_respawn",
      "COLUMN_NAME": "linkedGuid",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "linked_respawn",
      "COLUMN_NAME": "linkType",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "level",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "raceMask",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "mailTemplateId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "senderEntry",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mount_definitions",
      "COLUMN_NAME": "spellId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "mount_definitions",
      "COLUMN_NAME": "otherFactionSpellId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "npc_entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "reference to creature_template"
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "spell_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "spell which should be casted "
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "cast_flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "first bit defines caster: 1=player, 0=creature; second bit defines target, same mapping as caster bit"
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "user_type",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "relation with summoner: 0-no 1-friendly 2-raid 3-party player can click"
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability0",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability2",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability3",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability4",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability5",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability6",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "Probability7",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID0",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID1",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID2",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID3",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID4",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID5",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID6",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "BroadcastTextID7",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "slot",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "maxcount",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "incrtime",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "ExtendedCost",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "BonusListIDs",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "IgnoreFiltering",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "COLUMN_NAME": "TypeId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "NextPageID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "creature_entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "level",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "hp",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "mana",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "armor",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "str",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "agi",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "sta",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "inte",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "spi",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "COLUMN_NAME": "word",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "COLUMN_NAME": "half",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_area",
      "COLUMN_NAME": "AreaId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_area",
      "COLUMN_NAME": "PhaseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_area",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_name",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "phase_name",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "class",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "level",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "str",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "strength"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "agi",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "agility"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "sta",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "stamina"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "inte",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "intellect"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "spi",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "spirit"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "COLUMN_NAME": "alliance_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "COLUMN_NAME": "horde_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "alliance_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "horde_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "COLUMN_NAME": "alliance_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "COLUMN_NAME": "horde_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "COLUMN_NAME": "alliance_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "COLUMN_NAME": "horde_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "COLUMN_NAME": "alliance_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "COLUMN_NAME": "horde_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "race",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "str",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "strength"
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "agi",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "agility"
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "sta",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "stamina"
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "inte",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "intellect"
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "spi",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "spirit"
    },
    {
      "TABLE_NAME": "player_xp_for_level",
      "COLUMN_NAME": "Level",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "player_xp_for_level",
      "COLUMN_NAME": "Experience",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "UiTextureKitId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "SoundKitId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "CloseSoundKitId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "Duration",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "bigint",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "PendingChoiceText",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "Question",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "HideWarboardHeader",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "KeepOpenAfterChoice",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ShowChoicesAsList",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "RequiresSelection",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ShowChoicesAsGrid",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "HideAnswerArt",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ShowChoicesAsColumns",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "MaxResponses",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "InfiniteRange",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "Question",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ChoiceArtFileId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "WidgetSetID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "UiTextureAtlasElementID",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "SoundKitID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "GroupID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "UiTextureKitID",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Header",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "varchar(511)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "SubHeader",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ButtonTooltip",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "varchar(400)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Answer",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(511)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Description",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "varchar(2047)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "Confirmation",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "varchar(127)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "RewardQuestID",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "Header",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(511)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "SubHeader",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "ButtonTooltip",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(400)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "Answer",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(511)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "Description",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "varchar(2047)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "Confirmation",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "varchar(127)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "TypeArtFileID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "Rarity",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "MaxStacks",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "TitleId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "PackageId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "SkillLineId",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "SkillPointCount",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "ArenaPointCount",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "HonorPointCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "Money",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "Xp",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "CurrencyId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "Quantity",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "FactionId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "Quantity",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "ItemId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "BonusListIDs",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "Quantity",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "ChoiceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "ResponseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "ItemId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "BonusListIDs",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "Quantity",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "race",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "class",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "position_x",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "position_y",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "position_z",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "orientation",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_map",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_position_x",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_position_y",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_position_z",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_orientation",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_transport_guid",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "intro_movie_id",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "intro_scene_id",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "npe_intro_scene_id",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "race",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "class",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "button",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "action",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "raceMask",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "classMask",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "createMode",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "spell",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "note",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "race",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "class",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "itemid",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "amount",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "racemask",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "classmask",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "Spell",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "Note",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "PositionX",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "PositionY",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "PositionZ",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "Icon",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "Importance",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "WMOGroupID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "Name",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "spawnId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "poolSpawnId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "pool_template",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Pool entry"
    },
    {
      "TABLE_NAME": "pool_template",
      "COLUMN_NAME": "max_limit",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Max number of objects (0) is no limit"
    },
    {
      "TABLE_NAME": "pool_template",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "Emote1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "Emote2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "Emote3",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "Emote4",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "EmoteDelay1",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "EmoteDelay2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "EmoteDelay3",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "EmoteDelay4",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "Type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "GreetEmoteType",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "GreetEmoteDelay",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "Greeting",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "Greeting",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_mail_sender",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_mail_sender",
      "COLUMN_NAME": "RewardMailSenderEntry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Type",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Order",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "StorageIndex",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ObjectID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Amount",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ConditionalAmount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Flags2",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ProgressBarWeight",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ParentObjectiveID",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Visible",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "Description",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "ObjectiveID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "GameEventID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "ConversationID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "UpdatePhaseShift",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "UpdateZoneAuras",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "StorageIndex",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "Description",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "Emote1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "Emote2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "Emote3",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "Emote4",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "EmoteDelay1",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "EmoteDelay2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "EmoteDelay3",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "EmoteDelay4",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "RewardText",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "RewardText",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "BlobIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "Idx1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "ObjectiveIndex",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "QuestObjectiveID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "QuestObjectID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "MapID",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "UiMapID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "Priority",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "WorldEffectID",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "NavigationPlayerConditionID",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "SpawnTrackingID",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "AlwaysAllowMergingBlobs",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Idx1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Idx2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "X",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Y",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Z",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "COLUMN_NAME": "questId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "COLUMN_NAME": "poolId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "COLUMN_NAME": "poolIndex",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Multiple quests with the same index will always spawn together!"
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "COLUMN_NAME": "poolId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "COLUMN_NAME": "numActive",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Number of indices to have active at any time"
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "EmoteOnComplete",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "EmoteOnIncomplete",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "EmoteOnCompleteDelay",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "EmoteOnIncompleteDelay",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "CompletionText",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "Text",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "CompletionText",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type3",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type4",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type5",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "Type6",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "Idx",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "Type",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "HouseDecorID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "HouseRoomID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "2",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestPackageID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ContentTuningID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestSortID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestInfoID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "SuggestedGroupNum",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardNextQuest",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardXPDifficulty",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardXPMultiplier",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardMoneyDifficulty",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardMoneyMultiplier",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardBonusMoney",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardDisplaySpell1",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardDisplaySpell2",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardDisplaySpell3",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardSpell",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardHonor",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardKillHonor",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "StartItem",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardArtifactXPDifficulty",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardArtifactXPMultiplier",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardArtifactCategoryID",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "FlagsEx",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "FlagsEx2",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "FlagsEx3",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardItem1",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardAmount1",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardItem2",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardAmount2",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardItem3",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardAmount3",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardItem4",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardAmount4",
      "ORDINAL_POSITION": 35,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDrop1",
      "ORDINAL_POSITION": 36,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDropQuantity1",
      "ORDINAL_POSITION": 37,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDrop2",
      "ORDINAL_POSITION": 38,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDropQuantity2",
      "ORDINAL_POSITION": 39,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDrop3",
      "ORDINAL_POSITION": 40,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDropQuantity3",
      "ORDINAL_POSITION": 41,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDrop4",
      "ORDINAL_POSITION": 42,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ItemDropQuantity4",
      "ORDINAL_POSITION": 43,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID1",
      "ORDINAL_POSITION": 44,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity1",
      "ORDINAL_POSITION": 45,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID1",
      "ORDINAL_POSITION": 46,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID2",
      "ORDINAL_POSITION": 47,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity2",
      "ORDINAL_POSITION": 48,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID2",
      "ORDINAL_POSITION": 49,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID3",
      "ORDINAL_POSITION": 50,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity3",
      "ORDINAL_POSITION": 51,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID3",
      "ORDINAL_POSITION": 52,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID4",
      "ORDINAL_POSITION": 53,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity4",
      "ORDINAL_POSITION": 54,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID4",
      "ORDINAL_POSITION": 55,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID5",
      "ORDINAL_POSITION": 56,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity5",
      "ORDINAL_POSITION": 57,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID5",
      "ORDINAL_POSITION": 58,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemID6",
      "ORDINAL_POSITION": 59,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemQuantity6",
      "ORDINAL_POSITION": 60,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardChoiceItemDisplayID6",
      "ORDINAL_POSITION": 61,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "POIContinent",
      "ORDINAL_POSITION": 62,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "POIx",
      "ORDINAL_POSITION": 63,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "POIy",
      "ORDINAL_POSITION": 64,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "POIPriority",
      "ORDINAL_POSITION": 65,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardTitle",
      "ORDINAL_POSITION": 66,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardArenaPoints",
      "ORDINAL_POSITION": 67,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardSkillLineID",
      "ORDINAL_POSITION": 68,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardNumSkillUps",
      "ORDINAL_POSITION": 69,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitGiver",
      "ORDINAL_POSITION": 70,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitGiverMount",
      "ORDINAL_POSITION": 71,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitGiverModelSceneID",
      "ORDINAL_POSITION": 72,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitTurnIn",
      "ORDINAL_POSITION": 73,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionID1",
      "ORDINAL_POSITION": 74,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionValue1",
      "ORDINAL_POSITION": 75,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionOverride1",
      "ORDINAL_POSITION": 76,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionCapIn1",
      "ORDINAL_POSITION": 77,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionID2",
      "ORDINAL_POSITION": 78,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionValue2",
      "ORDINAL_POSITION": 79,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionOverride2",
      "ORDINAL_POSITION": 80,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionCapIn2",
      "ORDINAL_POSITION": 81,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionID3",
      "ORDINAL_POSITION": 82,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionValue3",
      "ORDINAL_POSITION": 83,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionOverride3",
      "ORDINAL_POSITION": 84,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionCapIn3",
      "ORDINAL_POSITION": 85,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionID4",
      "ORDINAL_POSITION": 86,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionValue4",
      "ORDINAL_POSITION": 87,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionOverride4",
      "ORDINAL_POSITION": 88,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionCapIn4",
      "ORDINAL_POSITION": 89,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionID5",
      "ORDINAL_POSITION": 90,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionValue5",
      "ORDINAL_POSITION": 91,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionOverride5",
      "ORDINAL_POSITION": 92,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionCapIn5",
      "ORDINAL_POSITION": 93,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFactionFlags",
      "ORDINAL_POSITION": 94,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyID1",
      "ORDINAL_POSITION": 95,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyQty1",
      "ORDINAL_POSITION": 96,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyID2",
      "ORDINAL_POSITION": 97,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyQty2",
      "ORDINAL_POSITION": 98,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyID3",
      "ORDINAL_POSITION": 99,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyQty3",
      "ORDINAL_POSITION": 100,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyID4",
      "ORDINAL_POSITION": 101,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardCurrencyQty4",
      "ORDINAL_POSITION": 102,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "AcceptedSoundKitID",
      "ORDINAL_POSITION": 103,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "CompleteSoundKitID",
      "ORDINAL_POSITION": 104,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "AreaGroupID",
      "ORDINAL_POSITION": 105,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "TimeAllowed",
      "ORDINAL_POSITION": 106,
      "COLUMN_TYPE": "bigint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "AllowableRaces",
      "ORDINAL_POSITION": 107,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "Expansion",
      "ORDINAL_POSITION": 108,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ManagedWorldStateID",
      "ORDINAL_POSITION": 109,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestSessionBonus",
      "ORDINAL_POSITION": 110,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "LogTitle",
      "ORDINAL_POSITION": 111,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "LogDescription",
      "ORDINAL_POSITION": 112,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestDescription",
      "ORDINAL_POSITION": 113,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "AreaDescription",
      "ORDINAL_POSITION": 114,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitGiverText",
      "ORDINAL_POSITION": 115,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitGiverName",
      "ORDINAL_POSITION": 116,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitTurnInText",
      "ORDINAL_POSITION": 117,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "PortraitTurnInName",
      "ORDINAL_POSITION": 118,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "QuestCompletionLog",
      "ORDINAL_POSITION": 119,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ResetByScheduler",
      "ORDINAL_POSITION": 120,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 121,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "RewardFavor",
      "ORDINAL_POSITION": 122,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "MaxLevel",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "AllowableClasses",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "SourceSpellID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "PrevQuestID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "NextQuestID",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "ExclusiveGroup",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "BreadcrumbForQuestId",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RewardMailTemplateID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RewardMailDelay",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredSkillID",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredSkillPoints",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredMinRepFaction",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredMaxRepFaction",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredMinRepValue",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "RequiredMaxRepValue",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "ProvidedItemCount",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "SpecialFlags",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "LogTitle",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "LogDescription",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "QuestDescription",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "AreaDescription",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "PortraitGiverText",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "PortraitGiverName",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "PortraitTurnInText",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "PortraitTurnInName",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "QuestCompletionLog",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "COLUMN_NAME": "QuestID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "COLUMN_NAME": "TreasurePickerID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "Index",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "VisualEffect",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "COLUMN_NAME": "raceID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "COLUMN_NAME": "expansion",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "COLUMN_NAME": "achievementId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "faction",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "quest_rate",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "quest_daily_rate",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "quest_weekly_rate",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "quest_monthly_rate",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "quest_repeatable_rate",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "creature_rate",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "spell_rate",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "faction entry"
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "faction to give spillover for"
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rate_1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "the given rep points * rate"
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rank_1",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "max rank,above this will not give any spillover"
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction2",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rate_2",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rank_2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction3",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rate_3",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rank_3",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction4",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rate_4",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rank_4",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction5",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rate_5",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "rank_5",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "CriteriaTreeID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "BlobIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "Idx1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "MapID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "UiMapID",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "Priority",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "WorldEffectID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "PlayerConditionID",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "NavigationPlayerConditionID",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "CriteriaTreeID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Idx1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Idx2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "X",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Y",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Z",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "map",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "difficulty",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "scenario_A",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "scenario_H",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "SceneId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "ScriptPackageID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "Encrypted",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "chainId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "splineId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "expectedDuration",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "msUntilNext",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "velocity",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "chainId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "splineId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "wpId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "x",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "y",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "z",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "DifficultyID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CategoryId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Dispel",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Mechanic",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Attributes",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx2",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx3",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx4",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx5",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx6",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx7",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx8",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx9",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx10",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx11",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx12",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx13",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx14",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx15",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AttributesEx16",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Stances",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "StancesNot",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Targets",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "TargetCreatureType",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "RequiresSpellFocus",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "FacingCasterFlags",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CasterAuraState",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "TargetAuraState",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeCasterAuraState",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeTargetAuraState",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CasterAuraSpell",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "TargetAuraSpell",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeCasterAuraSpell",
      "ORDINAL_POSITION": 35,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeTargetAuraSpell",
      "ORDINAL_POSITION": 36,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CasterAuraType",
      "ORDINAL_POSITION": 37,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "TargetAuraType",
      "ORDINAL_POSITION": 38,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeCasterAuraType",
      "ORDINAL_POSITION": 39,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ExcludeTargetAuraType",
      "ORDINAL_POSITION": 40,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CastingTimeIndex",
      "ORDINAL_POSITION": 41,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "RecoveryTime",
      "ORDINAL_POSITION": 42,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "CategoryRecoveryTime",
      "ORDINAL_POSITION": 43,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "StartRecoveryCategory",
      "ORDINAL_POSITION": 44,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "StartRecoveryTime",
      "ORDINAL_POSITION": 45,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "InterruptFlags",
      "ORDINAL_POSITION": 46,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AuraInterruptFlags1",
      "ORDINAL_POSITION": 47,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AuraInterruptFlags2",
      "ORDINAL_POSITION": 48,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ChannelInterruptFlags1",
      "ORDINAL_POSITION": 49,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ChannelInterruptFlags2",
      "ORDINAL_POSITION": 50,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcFlags",
      "ORDINAL_POSITION": 51,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcFlags2",
      "ORDINAL_POSITION": 52,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcChance",
      "ORDINAL_POSITION": 53,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcCharges",
      "ORDINAL_POSITION": 54,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcCooldown",
      "ORDINAL_POSITION": 55,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ProcBasePPM",
      "ORDINAL_POSITION": 56,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "MaxLevel",
      "ORDINAL_POSITION": 57,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "BaseLevel",
      "ORDINAL_POSITION": 58,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellLevel",
      "ORDINAL_POSITION": 59,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "DurationIndex",
      "ORDINAL_POSITION": 60,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "RangeIndex",
      "ORDINAL_POSITION": 61,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Speed",
      "ORDINAL_POSITION": 62,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "LaunchDelay",
      "ORDINAL_POSITION": 63,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "StackAmount",
      "ORDINAL_POSITION": 64,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "EquippedItemClass",
      "ORDINAL_POSITION": 65,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "-1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "EquippedItemSubClassMask",
      "ORDINAL_POSITION": 66,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "EquippedItemInventoryTypeMask",
      "ORDINAL_POSITION": 67,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ContentTuningId",
      "ORDINAL_POSITION": 68,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellName",
      "ORDINAL_POSITION": 69,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ConeAngle",
      "ORDINAL_POSITION": 70,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ConeWidth",
      "ORDINAL_POSITION": 71,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "MaxTargetLevel",
      "ORDINAL_POSITION": 72,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "MaxAffectedTargets",
      "ORDINAL_POSITION": 73,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellFamilyName",
      "ORDINAL_POSITION": 74,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellFamilyFlags1",
      "ORDINAL_POSITION": 75,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellFamilyFlags2",
      "ORDINAL_POSITION": 76,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellFamilyFlags3",
      "ORDINAL_POSITION": 77,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SpellFamilyFlags4",
      "ORDINAL_POSITION": 78,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "DmgClass",
      "ORDINAL_POSITION": 79,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "PreventionType",
      "ORDINAL_POSITION": 80,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "AreaGroupId",
      "ORDINAL_POSITION": 81,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "SchoolMask",
      "ORDINAL_POSITION": 82,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "ChargeCategoryId",
      "ORDINAL_POSITION": 83,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "DifficultyID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "Effect",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectAura",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectAmplitude",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectAttributes",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectAuraPeriod",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectBonusCoefficient",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectChainAmplitude",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectChainTargets",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectItemType",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectMechanic",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectPointsPerResource",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectPosFacing",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectRealPointsPerLevel",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectTriggerSpell",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "BonusCoefficientFromAP",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "PvpMultiplier",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "Coefficient",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "Variance",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "ResourceCoefficient",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "GroupSizeBasePointsCoefficient",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectBasePoints",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectMiscValue1",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectMiscValue2",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectRadiusIndex1",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectRadiusIndex2",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectSpellClassMask1",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectSpellClassMask2",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectSpellClassMask3",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectSpellClassMask4",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "ImplicitTarget1",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "ImplicitTarget2",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "spellId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "SpellId of the discoverable spell"
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "reqSpell",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "spell requirement"
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "reqSkillValue",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "skill points requirement"
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "chance to discover"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "COLUMN_NAME": "spellId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "SpellId of the item creation spell"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "COLUMN_NAME": "requiredSpecialization",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Specialization spell id"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "COLUMN_NAME": "additionalCreateChance",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "chance to create add"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "COLUMN_NAME": "additionalMaxNum",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "max num of adds"
    },
    {
      "TABLE_NAME": "skill_fishing_base_level",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Area identifier"
    },
    {
      "TABLE_NAME": "skill_fishing_base_level",
      "COLUMN_NAME": "skill",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Base skill level requirement"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "COLUMN_NAME": "spellId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "SpellId of the item creation spell"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "COLUMN_NAME": "requiredSpecialization",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Specialization spell id"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "COLUMN_NAME": "perfectCreateChance",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "chance to create the perfect item instead"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "COLUMN_NAME": "perfectItemType",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "perfect item type to create instead"
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value1",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value2",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value3",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value4",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value5",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value6",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value7",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value8",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value9",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value10",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value11",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value12",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value13",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value14",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value15",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "Value16",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "entryorguid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "source_type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "link",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "Difficulties",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_type",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_phase_mask",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_chance",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_flags",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param1",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param2",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param3",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param4",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param5",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "event_param_string",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_type",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param1",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param2",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param3",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param4",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param5",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param6",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param7",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "action_param_string",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_type",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_param1",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_param2",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_param3",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_param4",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_param_string",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_x",
      "ORDINAL_POSITION": 31,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_y",
      "ORDINAL_POSITION": 32,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_z",
      "ORDINAL_POSITION": 33,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "target_o",
      "ORDINAL_POSITION": 34,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 35,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Event Comment"
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "groupId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "spawnType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "spawnId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "COLUMN_NAME": "groupId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "COLUMN_NAME": "groupName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(100)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "COLUMN_NAME": "groupFlags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnTrackingId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "QuestObjectiveIds",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "COLUMN_NAME": "SpawnTrackingId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "COLUMN_NAME": "QuestObjectiveId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "SpawnType",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "SpawnId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "State",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "Visible",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "StateSpellVisualId",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "StateAnimId",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "StateAnimKitId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "StateWorldEffects",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "SpawnTrackingId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "MapId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "PhaseId",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "PhaseGroup",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "PhaseUseFlags",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "spell",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "area",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "quest_start",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "quest_end",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "aura_spell",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "racemask",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "gender",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "2",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "3",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "quest_start_status",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "64",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "quest_end_status",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "11",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_custom_attr",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "spell id"
    },
    {
      "TABLE_NAME": "spell_custom_attr",
      "COLUMN_NAME": "attributes",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "SpellCustomAttributes"
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "EnchantID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "ProcsPerMinute",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "HitMask",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "AttributesMask",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_group",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_group",
      "COLUMN_NAME": "spell_id",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_group_stack_rules",
      "COLUMN_NAME": "group_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_group_stack_rules",
      "COLUMN_NAME": "stack_rule",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "COLUMN_NAME": "Active",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "spell_trigger",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "spell_effect",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "type",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "Entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "MUL",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "ItemType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "Item",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "QuestRequired",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "LootMode",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "GroupId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "MinCount",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "MaxCount",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "spell",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "dummy spell id"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "effectId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "pet",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "pet id; 0 = all"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "aura",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "pet aura id"
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SchoolMask",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellFamilyName",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellFamilyMask0",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellFamilyMask1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellFamilyMask2",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellFamilyMask3",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "ProcFlags",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "ProcFlags2",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellTypeMask",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellPhaseMask",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "HitMask",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "AttributesMask",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "DisableEffectsMask",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "ProcsPerMinute",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "Chance",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "Cooldown",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "Charges",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_required",
      "COLUMN_NAME": "spell_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_required",
      "COLUMN_NAME": "req_spell",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_script_names",
      "COLUMN_NAME": "spell_id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_script_names",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "EffectIndex",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "OrderIndex",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "MapID",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "PositionX",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "PositionY",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "PositionZ",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "Orientation",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_threat",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_threat",
      "COLUMN_NAME": "flatMod",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_threat",
      "COLUMN_NAME": "pctMod",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "1",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "threat multiplier for damage/healing"
    },
    {
      "TABLE_NAME": "spell_threat",
      "COLUMN_NAME": "apPctMod",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "additional threat bonus from attack power"
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "COLUMN_NAME": "SpellID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "COLUMN_NAME": "RaceID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "COLUMN_NAME": "DisplayID",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "COLUMN_NAME": "MapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "COLUMN_NAME": "TerrainSwapMap",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "COLUMN_NAME": "TerrainSwapMap",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "COLUMN_NAME": "UiMapPhaseId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer",
      "COLUMN_NAME": "Type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "2",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer",
      "COLUMN_NAME": "Greeting",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "Id",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "locale",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(4)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "Greeting_lang",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "TrainerId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "SpellId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "MoneyCost",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqSkillLine",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqSkillRank",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqAbility1",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqAbility2",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqAbility3",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "ReqLevel",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "UNI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "phaseUseFlags",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "phaseid",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "phasegroup",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_default",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc1",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc2",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc3",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc4",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc5",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc6",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc7",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "content_loc8",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "COLUMN_NAME": "UiMapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "COLUMN_NAME": "QuestId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "COLUMN_NAME": "UiMapId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "COLUMN_NAME": "QuestLineId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "COLUMN_NAME": "VerifiedBuild",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "name",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(200)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "filename with extension of the update."
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "hash",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "char(40)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "sha1 hash of the sql file."
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "state",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "enum('RELEASED','ARCHIVED')",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "RELEASED",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "defines if an update is released or archived."
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "timestamp",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "timestamp",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "CURRENT_TIMESTAMP",
      "COLUMN_KEY": "",
      "EXTRA": "DEFAULT_GENERATED",
      "COLUMN_COMMENT": "timestamp when the query was applied."
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "speed",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "time the query takes to apply in ms."
    },
    {
      "TABLE_NAME": "updates_include",
      "COLUMN_NAME": "path",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(200)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "directory to include. $ means relative to the source directory."
    },
    {
      "TABLE_NAME": "updates_include",
      "COLUMN_NAME": "state",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "enum('RELEASED','ARCHIVED')",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "RELEASED",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "defines if the directory contains released or archived updates."
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "guid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "accessory_entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "seat_id",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "minion",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "summontype",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "6",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "see enum TempSummonType"
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "summontimer",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "30000",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "timer, only relevant for certain summontypes"
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "RideSpellID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "SeatEntry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "VehicleSeatEntry.dbc identifier"
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "SeatOrientation",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Seat Orientation override value"
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "ExitParamX",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "ExitParamY",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "ExitParamZ",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "ExitParamO",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "ExitParamValue",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint(1)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template",
      "COLUMN_NAME": "creatureId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template",
      "COLUMN_NAME": "despawnDelayMs",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template",
      "COLUMN_NAME": "Pitch",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template",
      "COLUMN_NAME": "CustomFlags",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "accessory_entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "seat_id",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "minion",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "description",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "summontype",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "6",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "see enum TempSummonType"
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "summontimer",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "30000",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "timer, only relevant for certain summontypes"
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "RideSpellID",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "version",
      "COLUMN_NAME": "core_version",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(250)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": "Core revision dumped at startup."
    },
    {
      "TABLE_NAME": "version",
      "COLUMN_NAME": "core_revision",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "varchar(120)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "version",
      "COLUMN_NAME": "db_version",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(120)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Version of world DB."
    },
    {
      "TABLE_NAME": "version",
      "COLUMN_NAME": "cache_id",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "SourceTypeOrReferenceId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(50)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "SourceGroup",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "SourceEntry",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "SourceId",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ElseGroup",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ConditionTypeOrReference",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(34)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ConditionTarget",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ConditionValue1",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ConditionValue2",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ConditionValue3",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "NegativeCondition",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ErrorType",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ErrorTextId",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "sourceType",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "varchar(33)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "entry",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "params_0",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "params_1",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "entryorguid",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "bigint",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "source_type",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "id",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "link",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_type",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(35)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_phase_mask",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_chance",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "100",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_flags",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "smallint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_param1",
      "ORDINAL_POSITION": 9,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_param2",
      "ORDINAL_POSITION": 10,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_param3",
      "ORDINAL_POSITION": 11,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_param4",
      "ORDINAL_POSITION": 12,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "event_param5",
      "ORDINAL_POSITION": 13,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_type",
      "ORDINAL_POSITION": 14,
      "COLUMN_TYPE": "varchar(47)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param1",
      "ORDINAL_POSITION": 15,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param2",
      "ORDINAL_POSITION": 16,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param3",
      "ORDINAL_POSITION": 17,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param4",
      "ORDINAL_POSITION": 18,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param5",
      "ORDINAL_POSITION": 19,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "action_param6",
      "ORDINAL_POSITION": 20,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_type",
      "ORDINAL_POSITION": 21,
      "COLUMN_TYPE": "varchar(41)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_param1",
      "ORDINAL_POSITION": 22,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_param2",
      "ORDINAL_POSITION": 23,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_param3",
      "ORDINAL_POSITION": 24,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_param4",
      "ORDINAL_POSITION": 25,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_x",
      "ORDINAL_POSITION": 26,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_y",
      "ORDINAL_POSITION": 27,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_z",
      "ORDINAL_POSITION": 28,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "target_o",
      "ORDINAL_POSITION": 29,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "COLUMN_NAME": "comment",
      "ORDINAL_POSITION": 30,
      "COLUMN_TYPE": "mediumtext",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": "Event Comment"
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "PathId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "MoveType",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "Flags",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "tinyint unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "Velocity",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "PathId",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "NodeId",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "PositionX",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "PositionY",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "PositionZ",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "Orientation",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "Delay",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "0",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "MapID",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "LocX",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "LocY",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "LocZ",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "Facing",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "float",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "TransportSpawnId",
      "ORDINAL_POSITION": 7,
      "COLUMN_TYPE": "bigint unsigned",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 8,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "ID",
      "ORDINAL_POSITION": 1,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "PRI",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "DefaultValue",
      "ORDINAL_POSITION": 2,
      "COLUMN_TYPE": "int",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "MapIDs",
      "ORDINAL_POSITION": 3,
      "COLUMN_TYPE": "varchar(128)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "AreaIDs",
      "ORDINAL_POSITION": 4,
      "COLUMN_TYPE": "varchar(255)",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "ScriptName",
      "ORDINAL_POSITION": 5,
      "COLUMN_TYPE": "varchar(64)",
      "IS_NULLABLE": "NO",
      "COLUMN_DEFAULT": "",
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "Comment",
      "ORDINAL_POSITION": 6,
      "COLUMN_TYPE": "text",
      "IS_NULLABLE": "YES",
      "COLUMN_DEFAULT": null,
      "COLUMN_KEY": "",
      "EXTRA": "",
      "COLUMN_COMMENT": ""
    }
  ],
  "indexes": [
    {
      "TABLE_NAME": "access_requirement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "mapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "access_requirement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "difficulty",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "achievement_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "achievement_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AchievementId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_involvedrelation",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_tavern",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "INDEX_NAME": "name",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Name",
      "SUB_PART": null,
      "INDEX_TYPE": "FULLTEXT"
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AreaTriggerId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "IsCustom",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "speciesId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "breedId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battle_pet_quality",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "speciesId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battlefield_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "TypeId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BattlemasterListId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battleground_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "battlemaster_entry",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "marketId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "character_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "character_template_class",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "TemplateId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "character_template_class",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "FactionGroup",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "character_template_class",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ClassID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "RaceID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "command",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "name",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SourceTypeOrReferenceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "SourceGroup",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "SourceEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "SourceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 5,
      "COLUMN_NAME": "ElseGroup",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 6,
      "COLUMN_NAME": "ConditionTypeOrReference",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 7,
      "COLUMN_NAME": "ConditionTarget",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 8,
      "COLUMN_NAME": "ConditionValue1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 9,
      "COLUMN_NAME": "ConditionValue2",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 10,
      "COLUMN_NAME": "ConditionValue3",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conditions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 11,
      "COLUMN_NAME": "ConditionStringValue1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conversation_actors",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ConversationId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conversation_actors",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "conversation_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature",
      "INDEX_NAME": "idx_id",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature",
      "INDEX_NAME": "idx_map",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "map",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_formations",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "memberGUID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_immunities",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_model_info",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "DisplayID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MovementID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "creature_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "CurrencyId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_questender",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_questender",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_questitem",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_questitem",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "DifficultyID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_questitem",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "DifficultyId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "DifficultyID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_model",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_model",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "School",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "NoNPCDamageBelowHealthPct",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Index",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "GroupID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "GroupID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "Locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_trainer",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CreatureID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_trainer",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "creature_trainer",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "OptionID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "criteria_data",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "criteria_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "criteria_data",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "disables",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "sourceType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "disables",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "disenchant_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "event_script_names",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "exploration_basexp",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "fishing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "INDEX_NAME": "season",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "season",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "INDEX_NAME": "season",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_condition",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_condition",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "condition_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_creature",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_creature",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "ExtendedCost",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "INDEX_NAME": "slot",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "slot",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_pool",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "pool_entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "prerequisite_event",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "INDEX_NAME": "idx_quest",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "questId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "questId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "eventEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_tele",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "game_weather",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "zone",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "GameObjectEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "quest",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_template",
      "INDEX_NAME": "idx_name",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "name",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "classSpecId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "abilityId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "garrPlotInstanceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "TextID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "OptionID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MenuID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "OptionID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "GhostZone",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "guild_rewards",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ItemID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ItemID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "AchievementRequired",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "instanceMapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "bossStateId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "spawnGroupId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "bossStates",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "instance_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "map",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BonusListID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_script_names",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "item_template_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "dungeonId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "maxLevel",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "dungeonId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "linked_respawn",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "linked_respawn",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "linkType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "raceMask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mail_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "milling_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "mount_definitions",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "npc_entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "spell_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_text",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "ExtendedCost",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_vendor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "npc_vendor",
      "INDEX_NAME": "slot",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "slot",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "TypeId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "page_text",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "page_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "page_text_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "creature_entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "phase_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "AreaId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "phase_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "PhaseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "phase_name",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pickpocketing_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "INDEX_NAME": "alliance_uniq",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "INDEX_NAME": "horde_uniq",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "alliance_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "horde_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_racestats",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "player_xp_for_level",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Level",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ChoiceId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ResponseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "INDEX_NAME": "playercreateinfo_race_class_index",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "INDEX_NAME": "playercreateinfo_race_class_index",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "button",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "raceMask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "classMask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "createMode",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "INDEX_NAME": "playercreateinfo_race_class_index",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "INDEX_NAME": "playercreateinfo_race_class_index",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "race",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "class",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "itemid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "racemask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "classmask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "points_of_interest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pool_members",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pool_members",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "spawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "pool_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "prospecting_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "PlayerConditionId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "QuestgiverCreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "PlayerConditionId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "QuestgiverCreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_details",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_greeting",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_greeting",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_mail_sender",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_objectives",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ObjectiveID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "PlayerConditionId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "QuestgiverCreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi",
      "INDEX_NAME": "idx",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi",
      "INDEX_NAME": "idx",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BlobIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BlobIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx2",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "INDEX_NAME": "questId_id",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "questId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "poolId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "PlayerConditionId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "QuestgiverCreatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "OrderIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "OrderIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "QuestID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "TreasurePickerID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Index",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "raceID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "reference_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "faction",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "faction",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "INDEX_NAME": "idx",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CriteriaTreeID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "INDEX_NAME": "idx",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BlobIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CriteriaTreeID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "BlobIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CriteriaTreeID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "Idx1",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Idx2",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "INDEX_NAME": "questId_id",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "CriteriaTreeID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenarios",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "map",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scenarios",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "difficulty",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "scene_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SceneId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "chainId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "splineId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "chainId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "splineId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "wpId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "serverside_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "serverside_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "DifficultyID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpellID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "EffectIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "DifficultyID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "reqSpell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_fishing_base_level",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skill_tiers",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "skinning_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "smart_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entryorguid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "smart_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "source_type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "smart_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "smart_scripts",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "link",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_group",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "groupId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_group",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "spawnType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_group",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "spawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "groupId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnTrackingId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "SpawnType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "SpawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnTrackingId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "QuestObjectiveId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "SpawnId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "State",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpawnTrackingId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "area",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "quest_start",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 4,
      "COLUMN_NAME": "aura_spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 5,
      "COLUMN_NAME": "racemask",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_area",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 6,
      "COLUMN_NAME": "gender",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_custom_attr",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "EnchantID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_group",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_group",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "spell_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_group_stack_rules",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "group_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "SpellID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "INDEX_NAME": "trigger_effect_type",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spell_trigger",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "INDEX_NAME": "trigger_effect_type",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "spell_effect",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "INDEX_NAME": "trigger_effect_type",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "type",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ItemType",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_loot_template",
      "INDEX_NAME": "idx_primary",
      "NON_UNIQUE": 1,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "Item",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "effectId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "pet",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_proc",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_required",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spell_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_required",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "req_spell",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_script_names",
      "INDEX_NAME": "spell_id",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "spell_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_script_names",
      "INDEX_NAME": "spell_id",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "ScriptName",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_target_position",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_target_position",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "EffectIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_target_position",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 3,
      "COLUMN_NAME": "OrderIndex",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_threat",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SpellID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "RaceID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "MapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "TerrainSwapMap",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "TerrainSwapMap",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "UiMapPhaseId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trainer",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trainer_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "Id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trainer_locale",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "locale",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trainer_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "TrainerId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trainer_spell",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "SpellId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "transports",
      "INDEX_NAME": "idx_entry",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "transports",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "trinity_string",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "UiMapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "QuestId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "UiMapId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "QuestLineId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "updates",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "name",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "updates_include",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "path",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "guid",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "seat_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "SeatEntry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_template",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "creatureId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "entry",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "seat_id",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "version",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "core_version",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "waypoint_path",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "PathId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "PathId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 2,
      "COLUMN_NAME": "NodeId",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    },
    {
      "TABLE_NAME": "world_state",
      "INDEX_NAME": "PRIMARY",
      "NON_UNIQUE": 0,
      "SEQ_IN_INDEX": 1,
      "COLUMN_NAME": "ID",
      "SUB_PART": null,
      "INDEX_TYPE": "BTREE"
    }
  ],
  "constraints": [
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "mapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "access_requirement",
      "COLUMN_NAME": "difficulty",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "achievement_dbc",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "achievement_reward",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "achievement_reward_locale",
      "COLUMN_NAME": "Locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "achievement_scripts",
      "COLUMN_NAME": "AchievementId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger",
      "COLUMN_NAME": "SpawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_orbit",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_polygon_vertex",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "AreaTriggerCreatePropertiesId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_create_properties_spline_point",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_involvedrelation",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_scripts",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_tavern",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_teleport",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_template",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "AreaTriggerId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "areatrigger_template_actions",
      "COLUMN_NAME": "IsCustom",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "COLUMN_NAME": "speciesId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battle_pet_breeds",
      "COLUMN_NAME": "breedId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battle_pet_quality",
      "COLUMN_NAME": "speciesId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battlefield_template",
      "COLUMN_NAME": "TypeId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "COLUMN_NAME": "MapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battleground_scripts",
      "COLUMN_NAME": "BattlemasterListId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battleground_template",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "battlemaster_entry",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "blackmarket_template",
      "COLUMN_NAME": "marketId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "character_template",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "TemplateId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "FactionGroup",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "character_template_class",
      "COLUMN_NAME": "Class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "ClassID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "class_expansion_requirement",
      "COLUMN_NAME": "RaceID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "command",
      "COLUMN_NAME": "name",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceTypeOrReferenceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceGroup",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "SourceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ElseGroup",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionTypeOrReference",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionTarget",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue2",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionValue3",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conditions",
      "COLUMN_NAME": "ConditionStringValue1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "ConversationId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conversation_actors",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conversation_line_template",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "conversation_template",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_addon",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_classlevelstats",
      "COLUMN_NAME": "class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_equip_template",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_formations",
      "COLUMN_NAME": "memberGUID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_immunities",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_model_info",
      "COLUMN_NAME": "DisplayID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_movement_info",
      "COLUMN_NAME": "MovementID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_movement_override",
      "COLUMN_NAME": "SpawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_onkill_reputation",
      "COLUMN_NAME": "creature_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "COLUMN_NAME": "CreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_quest_currency",
      "COLUMN_NAME": "CurrencyId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_questender",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_questender",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "CreatureEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "DifficultyID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_questitem",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_queststarter",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "SpawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_static_flags_override",
      "COLUMN_NAME": "DifficultyId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_summoned_data",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_addon",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "Entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_difficulty",
      "COLUMN_NAME": "DifficultyID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_gossip",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_model",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_movement",
      "COLUMN_NAME": "CreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_resistance",
      "COLUMN_NAME": "School",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "COLUMN_NAME": "Entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_sparring",
      "COLUMN_NAME": "NoNPCDamageBelowHealthPct",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_template_spell",
      "COLUMN_NAME": "Index",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "GroupID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "GroupID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_text_locale",
      "COLUMN_NAME": "Locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "CreatureID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "creature_trainer",
      "COLUMN_NAME": "OptionID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "criteria_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "criteria_data",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "destructible_hitpoint",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "sourceType",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "disables",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "event_script_names",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "exploration_basexp",
      "COLUMN_NAME": "level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "COLUMN_NAME": "season",
      "CONSTRAINT_NAME": "season",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_arena_seasons",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "season",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_condition",
      "COLUMN_NAME": "condition_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_creature",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_creature",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_creature_quest",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_gameobject",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_gameobject_quest",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_model_equip",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "item",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "ExtendedCost",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npc_vendor",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_npcflag",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_pool",
      "COLUMN_NAME": "pool_entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_prerequisite",
      "COLUMN_NAME": "prerequisite_event",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_quest_condition",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "COLUMN_NAME": "questId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_event_seasonal_questrelation",
      "COLUMN_NAME": "eventEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_tele",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "game_weather",
      "COLUMN_NAME": "zone",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_addon",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_overrides",
      "COLUMN_NAME": "spawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_questender",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "GameObjectEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_questitem",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_queststarter",
      "COLUMN_NAME": "quest",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_template",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_template_addon",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gameobject_template_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "COLUMN_NAME": "classSpecId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "garrison_follower_class_spec_abilities",
      "COLUMN_NAME": "abilityId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "garrison_plot_finalize_info",
      "COLUMN_NAME": "garrPlotInstanceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu",
      "COLUMN_NAME": "TextID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_addon",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_option",
      "COLUMN_NAME": "OptionID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "MenuID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "OptionID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "gossip_menu_option_locale",
      "COLUMN_NAME": "Locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "graveyard_zone",
      "COLUMN_NAME": "GhostZone",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "guild_rewards",
      "COLUMN_NAME": "ItemID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "COLUMN_NAME": "ItemID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "guild_rewards_req_achievements",
      "COLUMN_NAME": "AchievementRequired",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "instanceMapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "bossStateId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "spawnGroupId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "instance_spawn_groups",
      "COLUMN_NAME": "bossStates",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "instance_template",
      "COLUMN_NAME": "map",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "item_random_bonus_list_template",
      "COLUMN_NAME": "BonusListID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "item_script_names",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "item_template_addon",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "jump_charge_params",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "dungeonId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "lfg_dungeon_rewards",
      "COLUMN_NAME": "maxLevel",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "lfg_dungeon_template",
      "COLUMN_NAME": "dungeonId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "linked_respawn",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "linked_respawn",
      "COLUMN_NAME": "linkType",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "mail_level_reward",
      "COLUMN_NAME": "raceMask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "mount_definitions",
      "COLUMN_NAME": "spellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "npc_entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_spellclick_spells",
      "COLUMN_NAME": "spell_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_text",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "item",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "ExtendedCost",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "npc_vendor",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "outdoorpvp_template",
      "COLUMN_NAME": "TypeId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "page_text",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "page_text_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "creature_entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pet_levelstats",
      "COLUMN_NAME": "level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pet_name_generation",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "phase_area",
      "COLUMN_NAME": "AreaId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "phase_area",
      "COLUMN_NAME": "PhaseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "phase_name",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_classlevelstats",
      "COLUMN_NAME": "level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_achievement",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "alliance_uniq",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "horde_uniq",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_quests",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_reputations",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_spells",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "COLUMN_NAME": "alliance_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_factionchange_titles",
      "COLUMN_NAME": "horde_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_racestats",
      "COLUMN_NAME": "race",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "player_xp_for_level",
      "COLUMN_NAME": "Level",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_maw_power",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_currency",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_faction",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "ChoiceId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playerchoice_response_reward_item_choice",
      "COLUMN_NAME": "ResponseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "race",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo",
      "COLUMN_NAME": "class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "race",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_action",
      "COLUMN_NAME": "button",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "raceMask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "classMask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "createMode",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_cast_spell",
      "COLUMN_NAME": "spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "race",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "class",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_item",
      "COLUMN_NAME": "itemid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "racemask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "classmask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "playercreateinfo_spell_custom",
      "COLUMN_NAME": "Spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "points_of_interest",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "points_of_interest_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pool_members",
      "COLUMN_NAME": "spawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "pool_template",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_completion_log_conditional",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_description_conditional",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_details",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_greeting",
      "COLUMN_NAME": "Type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_greeting_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_mail_sender",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_objectives",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_objectives_completion_effect",
      "COLUMN_NAME": "ObjectiveID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_objectives_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_conditional",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_offer_reward_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "BlobIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi",
      "COLUMN_NAME": "Idx1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Idx1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_poi_points",
      "COLUMN_NAME": "Idx2",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_pool_members",
      "COLUMN_NAME": "questId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_pool_template",
      "COLUMN_NAME": "poolId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "PlayerConditionId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "QuestgiverCreatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_conditional",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_request_items_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_choice_items",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_display_spell",
      "COLUMN_NAME": "Idx",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_house_decor",
      "COLUMN_NAME": "OrderIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_reward_house_room",
      "COLUMN_NAME": "OrderIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_template",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_template_addon",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_template_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "COLUMN_NAME": "QuestID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_treasure_pickers",
      "COLUMN_NAME": "TreasurePickerID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "quest_visual_effect",
      "COLUMN_NAME": "Index",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "race_unlock_requirement",
      "COLUMN_NAME": "raceID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "reputation_reward_rate",
      "COLUMN_NAME": "faction",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "reputation_spillover_template",
      "COLUMN_NAME": "faction",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "CriteriaTreeID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "BlobIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi",
      "COLUMN_NAME": "Idx1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "CriteriaTreeID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Idx1",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenario_poi_points",
      "COLUMN_NAME": "Idx2",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "map",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scenarios",
      "COLUMN_NAME": "difficulty",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "scene_template",
      "COLUMN_NAME": "SceneId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "chainId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_meta",
      "COLUMN_NAME": "splineId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "chainId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "splineId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "script_spline_chain_waypoints",
      "COLUMN_NAME": "wpId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "serverside_spell",
      "COLUMN_NAME": "DifficultyID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "SpellID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "EffectIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "serverside_spell_effect",
      "COLUMN_NAME": "DifficultyID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "spellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_discovery_template",
      "COLUMN_NAME": "reqSpell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_extra_item_template",
      "COLUMN_NAME": "spellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_fishing_base_level",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_perfect_item_template",
      "COLUMN_NAME": "spellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "skill_tiers",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "entryorguid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "source_type",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "smart_scripts",
      "COLUMN_NAME": "link",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "groupId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "spawnType",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_group",
      "COLUMN_NAME": "spawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_group_template",
      "COLUMN_NAME": "groupId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnTrackingId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnType",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking",
      "COLUMN_NAME": "SpawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "COLUMN_NAME": "SpawnTrackingId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_quest_objective",
      "COLUMN_NAME": "QuestObjectiveId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "SpawnType",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "SpawnId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_state",
      "COLUMN_NAME": "State",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spawn_tracking_template",
      "COLUMN_NAME": "SpawnTrackingId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "area",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "quest_start",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "aura_spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "racemask",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_area",
      "COLUMN_NAME": "gender",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_custom_attr",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_enchant_proc_data",
      "COLUMN_NAME": "EnchantID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_group",
      "COLUMN_NAME": "id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_group",
      "COLUMN_NAME": "spell_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_group_stack_rules",
      "COLUMN_NAME": "group_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_learn_spell",
      "COLUMN_NAME": "SpellID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "spell_trigger",
      "CONSTRAINT_NAME": "trigger_effect_type",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "spell_effect",
      "CONSTRAINT_NAME": "trigger_effect_type",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_linked_spell",
      "COLUMN_NAME": "type",
      "CONSTRAINT_NAME": "trigger_effect_type",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "effectId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_pet_auras",
      "COLUMN_NAME": "pet",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_proc",
      "COLUMN_NAME": "SpellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_required",
      "COLUMN_NAME": "spell_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_required",
      "COLUMN_NAME": "req_spell",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_script_names",
      "COLUMN_NAME": "spell_id",
      "CONSTRAINT_NAME": "spell_id",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_script_names",
      "COLUMN_NAME": "ScriptName",
      "CONSTRAINT_NAME": "spell_id",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "EffectIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_target_position",
      "COLUMN_NAME": "OrderIndex",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_threat",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "COLUMN_NAME": "SpellID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "spell_totem_model",
      "COLUMN_NAME": "RaceID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "COLUMN_NAME": "MapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "terrain_swap_defaults",
      "COLUMN_NAME": "TerrainSwapMap",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "COLUMN_NAME": "TerrainSwapMap",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "terrain_worldmap",
      "COLUMN_NAME": "UiMapPhaseId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trainer",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "Id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trainer_locale",
      "COLUMN_NAME": "locale",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "TrainerId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trainer_spell",
      "COLUMN_NAME": "SpellId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "idx_entry",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "transports",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "trinity_string",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "COLUMN_NAME": "UiMapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "ui_map_quest",
      "COLUMN_NAME": "QuestId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "COLUMN_NAME": "UiMapId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "ui_map_quest_line",
      "COLUMN_NAME": "QuestLineId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "updates",
      "COLUMN_NAME": "name",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "updates_include",
      "COLUMN_NAME": "path",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "guid",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_accessory",
      "COLUMN_NAME": "seat_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_seat_addon",
      "COLUMN_NAME": "SeatEntry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_template",
      "COLUMN_NAME": "creatureId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "entry",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "vehicle_template_accessory",
      "COLUMN_NAME": "seat_id",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "version",
      "COLUMN_NAME": "core_version",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "waypoint_path",
      "COLUMN_NAME": "PathId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "PathId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "waypoint_path_node",
      "COLUMN_NAME": "NodeId",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "world_safe_locs",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    },
    {
      "TABLE_NAME": "world_state",
      "COLUMN_NAME": "ID",
      "CONSTRAINT_NAME": "PRIMARY",
      "REFERENCED_TABLE_NAME": null,
      "REFERENCED_COLUMN_NAME": null
    }
  ],
  "views": [
    {
      "TABLE_NAME": "vw_conditions_with_labels",
      "VIEW_DEFINITION": "select (case when (`world`.`conditions`.`SourceTypeOrReferenceId` = 0) then 'CONDITION_SOURCE_TYPE_NONE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 1) then 'CONDITION_SOURCE_TYPE_CREATURE_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 2) then 'CONDITION_SOURCE_TYPE_DISENCHANT_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 3) then 'CONDITION_SOURCE_TYPE_FISHING_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 4) then 'CONDITION_SOURCE_TYPE_GAMEOBJECT_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 5) then 'CONDITION_SOURCE_TYPE_ITEM_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 6) then 'CONDITION_SOURCE_TYPE_MAIL_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 7) then 'CONDITION_SOURCE_TYPE_MILLING_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 8) then 'CONDITION_SOURCE_TYPE_PICKPOCKETING_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 9) then 'CONDITION_SOURCE_TYPE_PROSPECTING_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 10) then 'CONDITION_SOURCE_TYPE_REFERENCE_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 11) then 'CONDITION_SOURCE_TYPE_SKINNING_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 12) then 'CONDITION_SOURCE_TYPE_SPELL_LOOT_TEMPLATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 13) then 'CONDITION_SOURCE_TYPE_SPELL_IMPLICIT_TARGET' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 14) then 'CONDITION_SOURCE_TYPE_GOSSIP_MENU' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 15) then 'CONDITION_SOURCE_TYPE_GOSSIP_MENU_OPTION' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 16) then 'CONDITION_SOURCE_TYPE_CREATURE_TEMPLATE_VEHICLE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 17) then 'CONDITION_SOURCE_TYPE_SPELL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 18) then 'CONDITION_SOURCE_TYPE_SPELL_CLICK_EVENT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 19) then 'CONDITION_SOURCE_TYPE_QUEST_AVAILABLE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 21) then 'CONDITION_SOURCE_TYPE_VEHICLE_SPELL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 22) then 'CONDITION_SOURCE_TYPE_SMART_EVENT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 23) then 'CONDITION_SOURCE_TYPE_NPC_VENDOR' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 24) then 'CONDITION_SOURCE_TYPE_SPELL_PROC' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 25) then 'CONDITION_SOURCE_TYPE_TERRAIN_SWAP' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 26) then 'CONDITION_SOURCE_TYPE_PHASE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 27) then 'CONDITION_SOURCE_TYPE_GRAVEYARD' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 28) then 'CONDITION_SOURCE_TYPE_AREATRIGGER' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 29) then 'CONDITION_SOURCE_TYPE_CONVERSATION_LINE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 30) then 'CONDITION_SOURCE_TYPE_AREATRIGGER_CLIENT_TRIGGERED' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 31) then 'CONDITION_SOURCE_TYPE_TRAINER_SPELL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 32) then 'CONDITION_SOURCE_TYPE_OBJECT_ID_VISIBILITY' else `world`.`conditions`.`SourceTypeOrReferenceId` end) AS `SourceTypeOrReferenceId`,`world`.`conditions`.`SourceGroup` AS `SourceGroup`,`world`.`conditions`.`SourceEntry` AS `SourceEntry`,`world`.`conditions`.`SourceId` AS `SourceId`,`world`.`conditions`.`ElseGroup` AS `ElseGroup`,(case when (`world`.`conditions`.`SourceTypeOrReferenceId` = 0) then 'CONDITION_NONE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 1) then 'CONDITION_AURA' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 2) then 'CONDITION_ITEM' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 3) then 'CONDITION_ITEM_EQUIPPED' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 4) then 'CONDITION_ZONEID' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 5) then 'CONDITION_REPUTATION_RANK' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 6) then 'CONDITION_TEAM' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 7) then 'CONDITION_SKILL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 8) then 'CONDITION_QUESTREWARDED' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 9) then 'CONDITION_QUESTTAKEN' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 10) then 'CONDITION_DRUNKENSTATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 11) then 'CONDITION_WORLD_STATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 12) then 'CONDITION_ACTIVE_EVENT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 13) then 'CONDITION_INSTANCE_INFO' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 14) then 'CONDITION_QUEST_NONE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 15) then 'CONDITION_CLASS' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 16) then 'CONDITION_RACE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 17) then 'CONDITION_ACHIEVEMENT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 18) then 'CONDITION_TITLE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 19) then 'CONDITION_SPAWNMASK' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 20) then 'CONDITION_GENDER' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 21) then 'CONDITION_UNIT_STATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 22) then 'CONDITION_MAPID' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 23) then 'CONDITION_AREAID' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 24) then 'CONDITION_CREATURE_TYPE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 25) then 'CONDITION_SPELL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 26) then 'CONDITION_PHASEMASK' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 27) then 'CONDITION_LEVEL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 28) then 'CONDITION_QUEST_COMPLETE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 29) then 'CONDITION_NEAR_CREATURE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 30) then 'CONDITION_NEAR_GAMEOBJECT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 31) then 'CONDITION_OBJECT_ENTRY_GUID_LEGACY' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 32) then 'CONDITION_TYPE_MASK_LEGACY' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 33) then 'CONDITION_RELATION_TO' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 34) then 'CONDITION_REACTION_TO' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 35) then 'CONDITION_DISTANCE_TO' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 36) then 'CONDITION_ALIVE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 37) then 'CONDITION_HP_VAL' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 38) then 'CONDITION_HP_PCT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 39) then 'CONDITION_REALM_ACHIEVEMENT' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 40) then 'CONDITION_IN_WATER' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 41) then 'CONDITION_TERRAIN_SWAP' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 42) then 'CONDITION_STAND_STATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 43) then 'CONDITION_DAILY_QUEST_DONE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 44) then 'CONDITION_CHARMED' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 45) then 'CONDITION_PET_TYPE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 46) then 'CONDITION_TAXI' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 47) then 'CONDITION_QUESTSTATE' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 48) then 'CONDITION_QUEST_OBJECTIVE_PROGRESS' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 49) then 'CONDITION_DIFFICULTY_ID' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 50) then 'CONDITION_GAMEMASTER' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 51) then 'CONDITION_OBJECT_ENTRY_GUID' when (`world`.`conditions`.`SourceTypeOrReferenceId` = 52) then 'CONDITION_TYPE_MASK' else `world`.`conditions`.`ConditionTypeOrReference` end) AS `ConditionTypeOrReference`,`world`.`conditions`.`ConditionTarget` AS `ConditionTarget`,`world`.`conditions`.`ConditionValue1` AS `ConditionValue1`,`world`.`conditions`.`ConditionValue2` AS `ConditionValue2`,`world`.`conditions`.`ConditionValue3` AS `ConditionValue3`,`world`.`conditions`.`NegativeCondition` AS `NegativeCondition`,`world`.`conditions`.`ErrorType` AS `ErrorType`,`world`.`conditions`.`ErrorTextId` AS `ErrorTextId`,`world`.`conditions`.`ScriptName` AS `ScriptName`,`world`.`conditions`.`Comment` AS `Comment` from `world`.`conditions`",
      "CHECK_OPTION": "NONE",
      "IS_UPDATABLE": "YES",
      "SECURITY_TYPE": "DEFINER"
    },
    {
      "TABLE_NAME": "vw_disables_with_labels",
      "VIEW_DEFINITION": "select (case when (`world`.`disables`.`sourceType` = 0) then 'DISABLE_TYPE_SPELL' when (`world`.`disables`.`sourceType` = 1) then 'DISABLE_TYPE_QUEST' when (`world`.`disables`.`sourceType` = 2) then 'DISABLE_TYPE_MAP' when (`world`.`disables`.`sourceType` = 3) then 'DISABLE_TYPE_BATTLEGROUND' when (`world`.`disables`.`sourceType` = 4) then 'DISABLE_TYPE_ACHIEVEMENT_CRITERIA' when (`world`.`disables`.`sourceType` = 5) then 'DISABLE_TYPE_OUTDOORPVP' when (`world`.`disables`.`sourceType` = 6) then 'DISABLE_TYPE_VMAP' when (`world`.`disables`.`sourceType` = 7) then 'DISABLE_TYPE_MMAP' when (`world`.`disables`.`sourceType` = 8) then 'DISABLE_TYPE_LFG_MAP' else `world`.`disables`.`sourceType` end) AS `sourceType`,`world`.`disables`.`entry` AS `entry`,`world`.`disables`.`flags` AS `flags`,`world`.`disables`.`params_0` AS `params_0`,`world`.`disables`.`params_1` AS `params_1`,`world`.`disables`.`comment` AS `comment` from `world`.`disables`",
      "CHECK_OPTION": "NONE",
      "IS_UPDATABLE": "YES",
      "SECURITY_TYPE": "DEFINER"
    },
    {
      "TABLE_NAME": "vw_smart_scripts_with_labels",
      "VIEW_DEFINITION": "select `world`.`smart_scripts`.`entryorguid` AS `entryorguid`,`world`.`smart_scripts`.`source_type` AS `source_type`,`world`.`smart_scripts`.`id` AS `id`,`world`.`smart_scripts`.`link` AS `link`,(case `world`.`smart_scripts`.`event_type` when 0 then 'SMART_EVENT_UPDATE_IC' when 1 then 'SMART_EVENT_UPDATE_OOC' when 2 then 'SMART_EVENT_HEALTH_PCT' when 3 then 'SMART_EVENT_MANA_PCT' when 4 then 'SMART_EVENT_AGGRO' when 5 then 'SMART_EVENT_KILL' when 6 then 'SMART_EVENT_DEATH' when 7 then 'SMART_EVENT_EVADE' when 8 then 'SMART_EVENT_SPELLHIT' when 9 then 'SMART_EVENT_RANGE' when 10 then 'SMART_EVENT_OOC_LOS' when 11 then 'SMART_EVENT_RESPAWN' when 12 then 'SMART_EVENT_TARGET_HEALTH_PCT' when 13 then 'SMART_EVENT_VICTIM_CASTING' when 14 then 'SMART_EVENT_FRIENDLY_HEALTH' when 15 then 'SMART_EVENT_FRIENDLY_IS_CC' when 16 then 'SMART_EVENT_FRIENDLY_MISSING_BUFF' when 17 then 'SMART_EVENT_SUMMONED_UNIT' when 18 then 'SMART_EVENT_TARGET_MANA_PCT' when 19 then 'SMART_EVENT_ACCEPTED_QUEST' when 20 then 'SMART_EVENT_REWARD_QUEST' when 21 then 'SMART_EVENT_REACHED_HOME' when 22 then 'SMART_EVENT_RECEIVE_EMOTE' when 23 then 'SMART_EVENT_HAS_AURA' when 24 then 'SMART_EVENT_TARGET_BUFFED' when 25 then 'SMART_EVENT_RESET' when 26 then 'SMART_EVENT_IC_LOS' when 27 then 'SMART_EVENT_PASSENGER_BOARDED' when 28 then 'SMART_EVENT_PASSENGER_REMOVED' when 29 then 'SMART_EVENT_CHARMED' when 30 then 'SMART_EVENT_CHARMED_TARGET' when 31 then 'SMART_EVENT_SPELLHIT_TARGET' when 32 then 'SMART_EVENT_DAMAGED' when 33 then 'SMART_EVENT_DAMAGED_TARGET' when 34 then 'SMART_EVENT_MOVEMENTINFORM' when 35 then 'SMART_EVENT_SUMMON_DESPAWNED' when 36 then 'SMART_EVENT_CORPSE_REMOVED' when 37 then 'SMART_EVENT_AI_INIT' when 38 then 'SMART_EVENT_DATA_SET' when 39 then 'SMART_EVENT_WAYPOINT_START' when 40 then 'SMART_EVENT_WAYPOINT_REACHED' when 41 then 'SMART_EVENT_TRANSPORT_ADDPLAYER' when 42 then 'SMART_EVENT_TRANSPORT_ADDCREATURE' when 43 then 'SMART_EVENT_TRANSPORT_REMOVE_PLAYER' when 44 then 'SMART_EVENT_TRANSPORT_RELOCATE' when 45 then 'SMART_EVENT_INSTANCE_PLAYER_ENTER' when 46 then 'SMART_EVENT_AREATRIGGER_ONTRIGGER' when 47 then 'SMART_EVENT_QUEST_ACCEPTED' when 48 then 'SMART_EVENT_QUEST_OBJ_COPLETETION' when 49 then 'SMART_EVENT_QUEST_COMPLETION' when 50 then 'SMART_EVENT_QUEST_REWARDED' when 51 then 'SMART_EVENT_QUEST_FAIL' when 52 then 'SMART_EVENT_TEXT_OVER' when 53 then 'SMART_EVENT_RECEIVE_HEAL' when 54 then 'SMART_EVENT_JUST_SUMMONED' when 55 then 'SMART_EVENT_WAYPOINT_PAUSED' when 56 then 'SMART_EVENT_WAYPOINT_RESUMED' when 57 then 'SMART_EVENT_WAYPOINT_STOPPED' when 58 then 'SMART_EVENT_WAYPOINT_ENDED' when 59 then 'SMART_EVENT_TIMED_EVENT_TRIGGERED' when 60 then 'SMART_EVENT_UPDATE' when 61 then 'SMART_EVENT_LINK' when 62 then 'SMART_EVENT_GOSSIP_SELECT' when 63 then 'SMART_EVENT_JUST_CREATED' when 64 then 'SMART_EVENT_GOSSIP_HELLO' when 65 then 'SMART_EVENT_FOLLOW_COMPLETED' when 66 then 'SMART_EVENT_EVENT_PHASE_CHANGE' when 67 then 'SMART_EVENT_IS_BEHIND_TARGET' when 68 then 'SMART_EVENT_GAME_EVENT_START' when 69 then 'SMART_EVENT_GAME_EVENT_END' when 70 then 'SMART_EVENT_GO_LOOT_STATE_CHANGED' when 71 then 'SMART_EVENT_GO_EVENT_INFORM' when 72 then 'SMART_EVENT_ACTION_DONE' when 73 then 'SMART_EVENT_ON_SPELLCLICK' when 74 then 'SMART_EVENT_FRIENDLY_HEALTH_PCT' when 75 then 'SMART_EVENT_DISTANCE_CREATURE' when 76 then 'SMART_EVENT_DISTANCE_GAMEOBJECT' when 77 then 'SMART_EVENT_COUNTER_SET' when 78 then 'SMART_EVENT_SCENE_START' when 79 then 'SMART_EVENT_SCENE_TRIGGER' when 80 then 'SMART_EVENT_SCENE_CANCEL' when 81 then 'SMART_EVENT_SCENE_COMPLETE' when 82 then 'SMART_EVENT_SUMMONED_UNIT_DIES' else `world`.`smart_scripts`.`event_type` end) AS `event_type`,`world`.`smart_scripts`.`event_phase_mask` AS `event_phase_mask`,`world`.`smart_scripts`.`event_chance` AS `event_chance`,`world`.`smart_scripts`.`event_flags` AS `event_flags`,`world`.`smart_scripts`.`event_param1` AS `event_param1`,`world`.`smart_scripts`.`event_param2` AS `event_param2`,`world`.`smart_scripts`.`event_param3` AS `event_param3`,`world`.`smart_scripts`.`event_param4` AS `event_param4`,`world`.`smart_scripts`.`event_param5` AS `event_param5`,(case `world`.`smart_scripts`.`action_type` when 0 then 'SMART_ACTION_NONE' when 1 then 'SMART_ACTION_TALK' when 2 then 'SMART_ACTION_SET_FACTION' when 3 then 'SMART_ACTION_MORPH_TO_ENTRY_OR_MODEL' when 4 then 'SMART_ACTION_SOUND' when 5 then 'SMART_ACTION_PLAY_EMOTE' when 6 then 'SMART_ACTION_FAIL_QUEST' when 7 then 'SMART_ACTION_OFFER_QUEST' when 8 then 'SMART_ACTION_SET_REACT_STATE' when 9 then 'SMART_ACTION_ACTIVATE_GOBJECT' when 10 then 'SMART_ACTION_RANDOM_EMOTE' when 11 then 'SMART_ACTION_CAST' when 12 then 'SMART_ACTION_SUMMON_CREATURE' when 13 then 'SMART_ACTION_THREAT_SINGLE_PCT' when 14 then 'SMART_ACTION_THREAT_ALL_PCT' when 15 then 'SMART_ACTION_CALL_AREAEXPLOREDOREVENTHAPPENS' when 16 then 'SMART_ACTION_SET_INGAME_PHASE_GROUP' when 17 then 'SMART_ACTION_SET_EMOTE_STATE' when 18 then 'SMART_ACTION_SET_UNIT_FLAG' when 19 then 'SMART_ACTION_REMOVE_UNIT_FLAG' when 20 then 'SMART_ACTION_AUTO_ATTACK' when 21 then 'SMART_ACTION_ALLOW_COMBAT_MOVEMENT' when 22 then 'SMART_ACTION_SET_EVENT_PHASE' when 23 then 'SMART_ACTION_INC_EVENT_PHASE' when 24 then 'SMART_ACTION_EVADE' when 25 then 'SMART_ACTION_FLEE_FOR_ASSIST' when 26 then 'SMART_ACTION_CALL_GROUPEVENTHAPPENS' when 27 then 'SMART_ACTION_COMBAT_STOP' when 28 then 'SMART_ACTION_REMOVEAURASFROMSPELL' when 29 then 'SMART_ACTION_FOLLOW' when 30 then 'SMART_ACTION_RANDOM_PHASE' when 31 then 'SMART_ACTION_RANDOM_PHASE_RANGE' when 32 then 'SMART_ACTION_RESET_GOBJECT' when 33 then 'SMART_ACTION_CALL_KILLEDMONSTER' when 34 then 'SMART_ACTION_SET_INST_DATA' when 35 then 'SMART_ACTION_SET_INST_DATA64' when 36 then 'SMART_ACTION_UPDATE_TEMPLATE' when 37 then 'SMART_ACTION_DIE' when 38 then 'SMART_ACTION_SET_IN_COMBAT_WITH_ZONE' when 39 then 'SMART_ACTION_CALL_FOR_HELP' when 40 then 'SMART_ACTION_SET_SHEATH' when 41 then 'SMART_ACTION_FORCE_DESPAWN' when 42 then 'SMART_ACTION_SET_INVINCIBILITY_HP_LEVEL' when 43 then 'SMART_ACTION_MOUNT_TO_ENTRY_OR_MODEL' when 44 then 'SMART_ACTION_SET_INGAME_PHASE_ID' when 45 then 'SMART_ACTION_SET_DATA' when 46 then 'SMART_ACTION_ATTACK_STOP' when 47 then 'SMART_ACTION_SET_VISIBILITY' when 48 then 'SMART_ACTION_SET_ACTIVE' when 49 then 'SMART_ACTION_ATTACK_START' when 50 then 'SMART_ACTION_SUMMON_GO' when 51 then 'SMART_ACTION_KILL_UNIT' when 52 then 'SMART_ACTION_ACTIVATE_TAXI' when 53 then 'SMART_ACTION_WP_START' when 54 then 'SMART_ACTION_WP_PAUSE' when 55 then 'SMART_ACTION_WP_STOP' when 56 then 'SMART_ACTION_ADD_ITEM' when 57 then 'SMART_ACTION_REMOVE_ITEM' when 58 then 'SMART_ACTION_INSTALL_AI_TEMPLATE' when 59 then 'SMART_ACTION_SET_RUN' when 60 then 'SMART_ACTION_SET_DISABLE_GRAVITY' when 61 then 'SMART_ACTION_SET_SWIM' when 62 then 'SMART_ACTION_TELEPORT' when 63 then 'SMART_ACTION_SET_COUNTER' when 64 then 'SMART_ACTION_STORE_TARGET_LIST' when 65 then 'SMART_ACTION_WP_RESUME' when 66 then 'SMART_ACTION_SET_ORIENTATION' when 67 then 'SMART_ACTION_CREATE_TIMED_EVENT' when 68 then 'SMART_ACTION_PLAYMOVIE' when 69 then 'SMART_ACTION_MOVE_TO_POS' when 70 then 'SMART_ACTION_ENABLE_TEMP_GOBJ' when 71 then 'SMART_ACTION_EQUIP' when 72 then 'SMART_ACTION_CLOSE_GOSSIP' when 73 then 'SMART_ACTION_TRIGGER_TIMED_EVENT' when 74 then 'SMART_ACTION_REMOVE_TIMED_EVENT' when 75 then 'SMART_ACTION_ADD_AURA' when 76 then 'SMART_ACTION_OVERRIDE_SCRIPT_BASE_OBJECT' when 77 then 'SMART_ACTION_RESET_SCRIPT_BASE_OBJECT' when 78 then 'SMART_ACTION_CALL_SCRIPT_RESET' when 79 then 'SMART_ACTION_SET_RANGED_MOVEMENT' when 80 then 'SMART_ACTION_CALL_TIMED_ACTIONLIST' when 81 then 'SMART_ACTION_SET_NPC_FLAG' when 82 then 'SMART_ACTION_ADD_NPC_FLAG' when 83 then 'SMART_ACTION_REMOVE_NPC_FLAG' when 84 then 'SMART_ACTION_SIMPLE_TALK' when 85 then 'SMART_ACTION_SELF_CAST' when 86 then 'SMART_ACTION_CROSS_CAST' when 87 then 'SMART_ACTION_CALL_RANDOM_TIMED_ACTIONLIST' when 88 then 'SMART_ACTION_CALL_RANDOM_RANGE_TIMED_ACTIONLIST' when 89 then 'SMART_ACTION_RANDOM_MOVE' when 90 then 'SMART_ACTION_SET_UNIT_FIELD_BYTES_1' when 91 then 'SMART_ACTION_REMOVE_UNIT_FIELD_BYTES_1' when 92 then 'SMART_ACTION_INTERRUPT_SPELL' when 93 then 'SMART_ACTION_SEND_GO_CUSTOM_ANIM' when 94 then 'SMART_ACTION_SET_DYNAMIC_FLAG' when 95 then 'SMART_ACTION_ADD_DYNAMIC_FLAG' when 96 then 'SMART_ACTION_REMOVE_DYNAMIC_FLAG' when 97 then 'SMART_ACTION_JUMP_TO_POS' when 98 then 'SMART_ACTION_SEND_GOSSIP_MENU' when 99 then 'SMART_ACTION_GO_SET_LOOT_STATE' when 100 then 'SMART_ACTION_SEND_TARGET_TO_TARGET' when 101 then 'SMART_ACTION_SET_HOME_POS' when 102 then 'SMART_ACTION_SET_HEALTH_REGEN' when 103 then 'SMART_ACTION_SET_ROOT' when 104 then 'SMART_ACTION_SET_GO_FLAG' when 105 then 'SMART_ACTION_ADD_GO_FLAG' when 106 then 'SMART_ACTION_REMOVE_GO_FLAG' when 107 then 'SMART_ACTION_SUMMON_CREATURE_GROUP' when 108 then 'SMART_ACTION_SET_POWER' when 109 then 'SMART_ACTION_ADD_POWER' when 110 then 'SMART_ACTION_REMOVE_POWER' when 111 then 'SMART_ACTION_GAME_EVENT_STOP' when 112 then 'SMART_ACTION_GAME_EVENT_START' when 113 then 'SMART_ACTION_START_CLOSEST_WAYPOINT' when 114 then 'SMART_ACTION_MOVE_OFFSET' when 115 then 'SMART_ACTION_RANDOM_SOUND' when 116 then 'SMART_ACTION_SET_CORPSE_DELAY' when 117 then 'SMART_ACTION_DISABLE_EVADE' when 118 then 'SMART_ACTION_GO_SET_GO_STATE' when 119 then 'SMART_ACTION_SET_CAN_FLY' when 120 then 'SMART_ACTION_REMOVE_AURAS_BY_TYPE' when 121 then 'SMART_ACTION_SET_SIGHT_DIST' when 122 then 'SMART_ACTION_FLEE' when 123 then 'SMART_ACTION_ADD_THREAT' when 124 then 'SMART_ACTION_LOAD_EQUIPMENT' when 125 then 'SMART_ACTION_TRIGGER_RANDOM_TIMED_EVENT' when 126 then 'SMART_ACTION_REMOVE_ALL_GAMEOBJECTS' when 127 then 'SMART_ACTION_PAUSE_MOVEMENT' when 128 then 'SMART_ACTION_PLAY_ANIMKIT' when 129 then 'SMART_ACTION_SCENE_PLAY' when 130 then 'SMART_ACTION_SCENE_CANCEL' when 131 then 'SMART_ACTION_SPAWN_SPAWNGROUP' when 132 then 'SMART_ACTION_DESPAWN_SPAWNGROUP' when 133 then 'SMART_ACTION_RESPAWN_BY_SPAWNID' when 134 then 'SMART_ACTION_INVOKER_CAST' when 135 then 'SMART_ACTION_PLAY_CINEMATIC' when 136 then 'SMART_ACTION_SET_MOVEMENT_SPEED' when 137 then 'SMART_ACTION_PLAY_SPELL_VISUAL_KIT' when 138 then 'SMART_ACTION_OVERRIDE_LIGHT' when 139 then 'SMART_ACTION_OVERRIDE_WEATHER' when 143 then 'SMART_ACTION_CREATE_CONVERSATION' when 144 then 'SMART_ACTION_SET_IMMUNE_PC' when 145 then 'SMART_ACTION_SET_IMMUNE_NPC' when 146 then 'SMART_ACTION_SET_UNINTERACTIBLE' when 147 then 'SMART_ACTION_ACTIVATE_GAMEOBJECT' when 148 then 'SMART_ACTION_ADD_TO_STORED_TARGET_LIST' when 149 then 'SMART_ACTION_BECOME_PERSONAL_CLONE_FOR_PLAYER' else `world`.`smart_scripts`.`action_type` end) AS `action_type`,`world`.`smart_scripts`.`action_param1` AS `action_param1`,`world`.`smart_scripts`.`action_param2` AS `action_param2`,`world`.`smart_scripts`.`action_param3` AS `action_param3`,`world`.`smart_scripts`.`action_param4` AS `action_param4`,`world`.`smart_scripts`.`action_param5` AS `action_param5`,`world`.`smart_scripts`.`action_param6` AS `action_param6`,(case `world`.`smart_scripts`.`target_type` when 0 then 'SMART_TARGET_NONE' when 1 then 'SMART_TARGET_SELF' when 2 then 'SMART_TARGET_VICTIM' when 3 then 'SMART_TARGET_HOSTILE_SECOND_AGGRO' when 4 then 'SMART_TARGET_HOSTILE_LAST_AGGRO' when 5 then 'SMART_TARGET_HOSTILE_RANDOM' when 6 then 'SMART_TARGET_HOSTILE_RANDOM_NOT_TOP' when 7 then 'SMART_TARGET_ACTION_INVOKER' when 8 then 'SMART_TARGET_POSITION' when 9 then 'SMART_TARGET_CREATURE_RANGE' when 10 then 'SMART_TARGET_CREATURE_GUID' when 11 then 'SMART_TARGET_CREATURE_DISTANCE' when 12 then 'SMART_TARGET_STORED' when 13 then 'SMART_TARGET_GAMEOBJECT_RANGE' when 14 then 'SMART_TARGET_GAMEOBJECT_GUID' when 15 then 'SMART_TARGET_GAMEOBJECT_DISTANCE' when 16 then 'SMART_TARGET_INVOKER_PARTY' when 17 then 'SMART_TARGET_PLAYER_RANGE' when 18 then 'SMART_TARGET_PLAYER_DISTANCE' when 19 then 'SMART_TARGET_CLOSEST_CREATURE' when 20 then 'SMART_TARGET_CLOSEST_GAMEOBJECT' when 21 then 'SMART_TARGET_CLOSEST_PLAYER' when 22 then 'SMART_TARGET_ACTION_INVOKER_VEHICLE' when 23 then 'SMART_TARGET_OWNER_OR_SUMMONER' when 24 then 'SMART_TARGET_THREAT_LIST' when 25 then 'SMART_TARGET_CLOSEST_ENEMY' when 26 then 'SMART_TARGET_CLOSEST_FRIENDLY' when 27 then 'SMART_TARGET_LOOT_RECIPIENTS' when 28 then 'SMART_TARGET_FARTHEST' when 29 then 'SMART_TARGET_VEHICLE_PASSENGER' when 30 then 'SMART_TARGET_CLOSEST_UNSPAWNED_GAMEOBJECT' else `world`.`smart_scripts`.`target_type` end) AS `target_type`,`world`.`smart_scripts`.`target_param1` AS `target_param1`,`world`.`smart_scripts`.`target_param2` AS `target_param2`,`world`.`smart_scripts`.`target_param3` AS `target_param3`,`world`.`smart_scripts`.`target_param4` AS `target_param4`,`world`.`smart_scripts`.`target_x` AS `target_x`,`world`.`smart_scripts`.`target_y` AS `target_y`,`world`.`smart_scripts`.`target_z` AS `target_z`,`world`.`smart_scripts`.`target_o` AS `target_o`,`world`.`smart_scripts`.`comment` AS `comment` from `world`.`smart_scripts`",
      "CHECK_OPTION": "NONE",
      "IS_UPDATABLE": "YES",
      "SECURITY_TYPE": "DEFINER"
    }
  ]
}
```
