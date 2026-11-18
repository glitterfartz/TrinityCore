# AGENTS.md — sql/ and the TrinityCore databases

Guidance for AI coding agents doing database work on this TrinityCore checkout (branch `master`, TDB 1210.26091, core `15f2f255026b`). Repo-wide build instructions are in [`../AGENTS.md`](../AGENTS.md); script bindings are in [`../src/server/scripts/AGENTS.md`](../src/server/scripts/AGENTS.md).

> **Check the live DB first.** This environment has a MariaDB MCP connection with `world`, `auth`, `characters`, and `hotfixes` schemas. Prefer `db_list_schemas` / `db_execute_sql` over grepping the SQL files, which are history, not current state. Do not use the unrelated `acore_*` / `acworld` schemas on the same server. Never ask for or print DB passwords; connections come from the secret store.

## Schemas: the world / hotfixes split

This is the single most important architectural fact and is frequently gotten wrong:

- **`world`** — the content/authoring database. Templates, spawns, loot, quests, SmartAI, conditions, script bindings, instances, gossip, pools, events, phase/terrain, playercreateinfo. ~250 tables, ~6.9M rows.
- **`hotfixes`** — a **client-DB2 overlay**, not authoring content. It mirrors client DB2 names (`item`, `item_sparse`, `item_effect`, `spell_name`, `spell_misc`, `spell_effect`, `broadcast_text`, `journal_*`, `difficulty`, `map`, `content_tuning`, `player_condition`, …). Data is loaded from client DB2 files first, then rows here are overlaid, then `hotfix_data`/`hotfix_blob` are applied. The rows are **sparse overrides** (~2.9M rows across 482 tables; e.g. `item_sparse` ≈ 560).
- **`auth`** — accounts, BNet, RBAC, realm list (39 tables).
- **`characters`** — per-character state and instance saves (132 tables).

Consequences:

- There is **no `item_template`** anywhere in `world` or `hotfixes`. Item definitions are `hotfixes.item` / `hotfixes.item_sparse`; world only has item *auxiliary* tables such as `item_loot_template`, `item_template_addon`, `item_script_names`.
- `creature_template`, `gameobject_template`, `quest_template` are **world**-side. `definitions` of those objects are not in `hotfixes`.
- `hotfixes.creature` is the client `Creature.db2` display/model store (columns `ID`, `ItemID1-3`, `Mount`, `DisplayID1-4`, `Name`, …) and is empty here. It is **not** the spawn table; `world.creature` is.
- Only four table names overlap: `creature` (different meaning), `spell_learn_spell`, `updates`, `updates_include`. Always schema-qualify.
- Cross-schema joins you will need: `world.npc_text.BroadcastTextID0..7` → `hotfixes.broadcast_text.ID`; `world.creature_text.BroadcastTextId` → same; `world.quest_template.ContentTuningID` → `hotfixes.content_tuning`; `world.creature_template_difficulty.DifficultyID` → `hotfixes.difficulty`; loot/vendor/quest item ids → `hotfixes.item_sparse`.
- `world.serverside_spell` / `serverside_spell_effect` hold server-only spells that have no client row.

No foreign keys exist in `world`. A few tables are MyISAM. There are no cross-schema transactions.

## Table taxonomy (world)

Row counts are a live snapshot from 2026-11-16 — treat them as scale hints, not constants.

**Creatures**
- `creature_template` (~227k, key `entry`): `ScriptName`, `AIName`, faction/flags, `RequiredExpansion`, `VerifiedBuild`. No levels/models/gossip id here in 12.x.
- `creature` (~263k, key `guid`): spawns; `id` = template entry, plus map/zone/area, `spawnDifficulties`, phase columns, position, `spawntimesecs`, `MovementType`, and a per-spawn `ScriptName` override.
- `creature_template_model` (display ids), `creature_template_difficulty` (PK `Entry,DifficultyID`: level scaling, `ContentTuningID`, modifiers, `LootID`/`PickPocketLootID`/`SkinLootID`, gold), `creature_template_addon` (entry) vs `creature_addon` (guid), `creature_equip_template`, `creature_template_spell`, `creature_template_gossip`, `creature_template_movement`, `creature_movement_override`, `creature_movement_info`, `creature_classlevelstats`, `creature_immunities`, `creature_summon_groups`, `creature_formations`, `linked_respawn`, `spawn_group`/`spawn_group_template`, `instance_spawn_groups`, `creature_text`.

**GameObjects**
- `gameobject_template` (~83k, key `entry`, `Data0..Data34`, `AIName`, `ScriptName`), `gameobject` (~104k spawns, key `guid`), `gameobject_template_addon`, `gameobject_addon`, `gameobject_queststarter/questender/questitem`, `gameobject_overrides`.

**Quests**
- `quest_template` (~48k, key `ID`; inline Log/Description text, reward fields, `ContentTuningID`).
- `quest_template_addon` (chain/requirements, `SpecialFlags`, **`ScriptName`**).
- `quest_objectives` (`ID`, `QuestID`, `Type`, `Order`, `StorageIndex`, `ObjectID`, `Amount`) — objective `Type`: 0 MONSTER, 1 ITEM, 2 GAMEOBJECT, 3 TALKTO, 4 CURRENCY, 5 LEARNSPELL, 8 MONEY, 9 PLAYERKILLS, 10 AREATRIGGER, 21 KILL_WITH_LABEL.
- `quest_offer_reward`, `quest_request_items`, `quest_details`, `quest_poi`/`quest_poi_points`, `creature_queststarter`/`creature_questender`, `quest_greeting`, `quest_mail_sender`, `quest_*_conditional`, `quest_pool_template`/`quest_pool_members`.

**Loot** (all `world`)
- `creature_loot_template` (~311k), `reference_loot_template`, `gameobject_loot_template`, `pickpocketing_loot_template`, `skinning_loot_template`, `fishing_loot_template`, `disenchant_loot_template`, `milling_loot_template`, `prospecting_loot_template`, `spell_loot_template`, `mail_loot_template`, `item_loot_template`.
- `ItemType` semantics in these tables: `0` item, `1` reference (the `Item` column points at `reference_loot_template.Entry`), `2` currency, `3` tracking quest.
- **The loot key is `creature_template_difficulty.LootID`, not necessarily the creature entry.** They differ (e.g. entry 1008 → LootID 1007; 1012 and 1013 share 1011).

**Spells / server-side**
- `spell_script_names` (`spell_id`, `ScriptName`; negative `spell_id` = all ranks), `spell_proc`, `spell_group`/`spell_group_stack_rules`, `spell_area`, `spell_learn_spell`, `spell_linked_spell`, `spell_pet_auras`, `spell_required`, `spell_target_position`, `spell_threat`, `spell_custom_attr`, `spell_totem_model`, `serverside_spell`/`serverside_spell_effect`. Full spell definitions live in `hotfixes.spell_*`.

**Conditions**
- `conditions` (~17k): `SourceTypeOrReferenceId, SourceGroup, SourceEntry, SourceId, ElseGroup, ConditionTypeOrReference, ConditionTarget, ConditionValue1-3, ConditionStringValue1, NegativeCondition, ErrorType, ErrorTextId, ScriptName, Comment`.
- Positive `SourceTypeOrReferenceId` = `ConditionSourceType` (1 creature loot, 13 spell implicit target, 14 gossip menu, 15 gossip option, 17 spell, 18 spell click, 19 quest available, 22 SmartAI event, 23 vendor, 26 phase, 27 graveyard, 28 areatrigger, 29 conversation line, 33 spawn group, 34 player condition, 35 skill line ability, 36 player choice).
- **Negative values are valid and meaningful:** negative `SourceTypeOrReferenceId` declares a reusable reference-condition template (`SourceGroup = -value`); negative `ConditionTypeOrReference` references another condition id. Do not "fix" them.
- Else-groups are OR; conditions within a group are AND.

**SmartAI**
- `smart_scripts` (~55k): `entryorguid, source_type, id, link, Difficulties, event_type, event_phase_mask, event_chance, event_flags, event_param1-5, event_param_string, action_type, action_param1-7, action_param_string, target_type, target_param1-4, target_param_string, target_x/y/z/o, comment`.
- `source_type`: 0 CREATURE, 1 GAMEOBJECT, 2 AREATRIGGER, 3 EVENT, 5 QUEST, 9 TIMED_ACTIONLIST, 10 SCENE, 11 AREATRIGGER_ENTITY, 12 AREATRIGGER_ENTITY_CUSTOM.
- `entryorguid`: positive = template entry; **negative = spawn `guid`**. `id` orders rows; `link` ties actions into one batch; `Difficulties` empty = all.
- A creature uses SAI when `creature_template.AIName='SmartAI'`. C++ `ScriptName` takes precedence if both are set.

**Instances / triggers / text / social**
- `instance_template` (only `map, parent, script`), `instance_spawn_groups`, `lfg_dungeon_template`, `lfg_dungeon_rewards`, `access_requirement`, `graveyard_zone`. There is **no `instance_encounters`**; encounter metadata is `hotfixes.journal_*`.
- `areatrigger` (spawns), `areatrigger_template`, `areatrigger_create_properties`, `areatrigger_template_actions`, `areatrigger_scripts`, `areatrigger_tavern`, `areatrigger_teleport`.
- `conversation_template` / `conversation_line_template` / `conversation_actors`, `scene_template`, `playerchoice*`.
- `gossip_menu`, `gossip_menu_option`, `gossip_menu_addon`, `creature_template_gossip`, `npc_text` (references `hotfixes.broadcast_text`), `page_text` (inline text), `creature_text`, `points_of_interest`, `quest_greeting`.
- `battleground_template`, `battleground_scripts`, `battlefield_template`, `outdoorpvp_template`.
- Pools: `pool_template`, `pool_members` (type 0 creature, 1 gameobject, 2 nested pool), `game_event_pool`.
- Events: `game_event`, `game_event_creature`, `game_event_gameobject`, `game_event_condition`, etc.
- `disables` (`sourceType`: 0 spell, 1 quest, 2 map, 3 battleground, 4 criteria, 5 outdoorpvp, 6 vmap, 7 mmap, 8 lfg map, 9 phase area).
- Phase/terrain: `phase_area`, `phase_name`, `terrain_swap_defaults`, `terrain_worldmap`.
- `playercreateinfo*`, `player_classlevelstats`, `player_xp_for_level`, `player_factionchange_*`, `character_template*`.

**Script binding.** There is no generic `script_names` table. Bindings are per-object `ScriptName` columns plus dedicated tables — see the table in `src/server/scripts/AGENTS.md`.

## Creating and updating the DB

`sql/create/create_mysql.sql` creates only the `trinity` user and four empty schemas. Base schemas:

- `sql/base/auth_database.sql`, `sql/base/characters_database.sql` are real, importable base dumps.
- `sql/base/dev/{world,hotfixes}_database.sql` are **developer dumps and must not be imported** (guarded by `sql/base/dev/DO_NOT_IMPORT_THESE_FILES.txt`).
- World/hotfixes base data comes from **downloaded TDB full dumps**, named at build time in `revision_data.h` (`TDB_full_world_1210.26091_2026_09_09.sql`, `TDB_full_hotfixes_1210.26091_2026_09_09.sql`). The startup updater downloads/applies them to an empty schema when `Updates.AutoSetup=1`. Do not mix a manual import with the auto-updater.

Update workflow:

1. New files go in `sql/updates/{auth,characters,world,hotfixes}/master/`.
2. Name: `YYYY_MM_DD_NN_<db>.sql` (`NN` = per-day sequence). Files apply in lexical order, so ordering is filename ordering.
3. Use idempotent DELETE-then-INSERT patterns (this is what existing updates do).
4. Never edit an already-applied file: the updater re-hashes with `Updates.Redundancy` and can reapply or fail.
5. When a TDB is cut, files move unchanged to `sql/old/<major>.x/<db>/<TDBrev>_<date>/` and their rows become `ARCHIVED`.
6. User-local SQL belongs in `sql/custom/<db>/` (`*.sql` is gitignored), included via `updates_include`.

Tracking tables (one per schema):

- `updates`: `name varchar(200) PK` (filename+extension), `hash char(40)` SHA1, `state enum('RELEASED','ARCHIVED')`, `timestamp`, `speed`.
- `updates_include`: `path`, `state` — e.g. `$/sql/custom/world` RELEASED, `$/sql/updates/world` RELEASED, `$/sql/old/12.x/world` ARCHIVED.

Config (`worldserver.conf.dist`): `Updates.EnableDatabases` is a bitmask — LOGIN 1, CHARACTER 2, WORLD 4, HOTFIX 8 (default 15). Also `Updates.AutoSetup`, `Updates.Redundancy`, `Updates.ArchivedRedundancy`, `Updates.AllowRehash`, `Updates.CleanDeadRefMaxCount`. `SourceDirectory`/`MySQLExecutable` control where updates are found and which client applies them.

Helper scripts: `contrib/merge_updates_unix.sh` (concatenates world/hotfixes updates), `contrib/check_updates.sh <name> <branch> <db> <host>` (fails when an on-disk update is not recorded as applied; CI uses it for auth/characters).

## Query recipes

```sql
-- Creature template + per-difficulty stats
SELECT ct.entry, ct.name, ct.ScriptName, ct.AIName, ctd.DifficultyID,
       ctd.ContentTuningID, ctd.HealthModifier, ctd.DamageModifier, ctd.LootID
FROM world.creature_template ct
LEFT JOIN world.creature_template_difficulty ctd ON ctd.Entry = ct.entry
WHERE ct.entry = 1853;

-- All spawns of a template
SELECT guid, id, map, zoneId, spawnDifficulties, PhaseId, position_x, position_y,
       position_z, spawntimesecs, ScriptName
FROM world.creature WHERE id = 47747;

-- SmartAI for a template entry, then for one spawn guid
SELECT * FROM world.smart_scripts WHERE entryorguid = 47747 AND source_type = 0 ORDER BY id;
SELECT * FROM world.smart_scripts WHERE entryorguid = -361154 AND source_type = 0 ORDER BY id;

-- Quest + addon + objectives + givers
SELECT * FROM world.quest_template WHERE ID = 29547;
SELECT * FROM world.quest_template_addon WHERE ID = 29547;
SELECT ID, Type, `Order`, ObjectID, Amount, Description
FROM world.quest_objectives WHERE QuestID = 29547 ORDER BY `Order`;
SELECT id FROM world.creature_queststarter WHERE quest = 29547;

-- Correct loot lookup (via LootID)
SELECT ctd.Entry, ctd.DifficultyID, ctd.LootID, clt.*
FROM world.creature_template_difficulty ctd
JOIN world.creature_loot_template clt ON clt.Entry = ctd.LootID
WHERE ctd.Entry = 1008;

-- Conditions for a spell
SELECT * FROM world.conditions WHERE SourceTypeOrReferenceId = 17 AND SourceEntry = 3607;

-- NPC text with client text (cross-schema)
SELECT n.ID, n.BroadcastTextID0, b.Text
FROM world.npc_text n
LEFT JOIN hotfixes.broadcast_text b ON b.ID = n.BroadcastTextID0
WHERE n.ID = 1;

-- All places a script name is bound
SELECT 'creature_template' src, entry id FROM world.creature_template WHERE ScriptName = 'npc_guard_generic'
UNION ALL SELECT 'creature', guid FROM world.creature WHERE ScriptName = 'npc_guard_generic'
UNION ALL SELECT 'gameobject_template', entry FROM world.gameobject_template WHERE ScriptName = 'npc_guard_generic'
UNION ALL SELECT 'spell_script_names', spell_id FROM world.spell_script_names WHERE ScriptName = 'npc_guard_generic'
UNION ALL SELECT 'areatrigger_scripts', entry FROM world.areatrigger_scripts WHERE ScriptName = 'npc_guard_generic';

-- Update state
SELECT state, COUNT(*) FROM world.updates GROUP BY state;
SELECT name, timestamp FROM world.updates ORDER BY name DESC LIMIT 10;

-- Largest tables
SELECT table_name, table_rows FROM information_schema.tables
WHERE table_schema = 'world' ORDER BY table_rows DESC LIMIT 60;
```

## Gotchas

1. Wrong schema is the #1 error — see the split above. Always schema-qualify cross-schema joins.
2. `hotfixes.creature` is not spawns; it is the empty DB2 display store.
3. Template (`entry`) vs spawn (`guid`): `creature.id` is the template, `guid` is the spawn. `creature_template_addon` uses `entry`; `creature_addon` uses `guid`.
4. Loot keys on `creature_template_difficulty.LootID`, which can differ from the creature entry.
5. `ItemType` in loot tables is LootStoreItem semantics (0 item / 1 reference / 2 currency / 3 tracking quest), not `LootItemType`.
6. `ScriptName` is exact and case-sensitive; the DB and compiled `AddSC_*` must agree or the script silently never runs.
7. `AIName` must be a registered/db-allowed AI; invalid values are cleared at load. This DB uses mostly `SmartAI`, plus `PassiveAI`, `NullCreatureAI`, `TurretAI`, `CasterAI`.
8. Negative condition ids and negative `entryorguid` are deliberate encodings, not corruption.
9. `instance_template.script` must equal the instance script's constructor string exactly.
10. `0` usually means "none/any" (LootID 0, DifficultyID 0, ContentTuningID 0, PrevQuestID 0, RequiredExpansion 0 = base game); `VerifiedBuild=-1` is a placeholder, `-N` means parsed then manually edited.
11. `world.creature_template` is huge (~227k). Use indexed lookups; avoid unbounded scans and `SELECT *` dumps.
12. Some publisher docs are stale: `trinitycore.info` lists `spell_scripts`/`warden_checks`, which do not exist here (use `spell_script_names`), and omits several live tables/views.
