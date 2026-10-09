# Maintenance and regeneration

Run the generator from the repository root with Python 3.12 or later:

```powershell
python -c 'from pathlib import Path; p=Path("doc/world-database/maintenance.md"); fence=chr(96)*3; exec(p.read_text(encoding="utf-8").split(fence+"python"+chr(10),1)[1].split(chr(10)+fence,1)[0])'
```

The generator overwrites table pages, relationships, indexes, source references and coverage; editorial guides remain intact. Refresh the JSON fence in schema-snapshot.md from read-only information_schema TABLES, COLUMNS, STATISTICS, KEY_COLUMN_USAGE, VIEWS, and the version row. Preserve identifier case and exclude credentials, definers and row dumps. Update hardcoded revision/date/count prose when refreshing. Review guides and logical associations against the new loaders. Source excerpts retain repository licensing (COPYING and AUTHORS). Review the generated diff before committing.

```python
from pathlib import Path
import json, re, collections
ROOT = Path(__file__).resolve().parents[2] if '__file__' in globals() else Path.cwd()
if not (ROOT/'src').exists(): ROOT = Path.cwd()
OUT = ROOT/'doc/world-database'
snapshot = json.loads((OUT/'schema-snapshot.md').read_text(encoding='utf-8').split('```json\n',1)[1].split('\n```',1)[0])
PURPOSES = json.loads("{\"access_requirement\":\"Restricts instance entry by map and difficulty, level, items, quests, and achievements.\",\"achievement_dbc\":\"Server-side achievement records supplementing client achievement data.\",\"achievement_reward\":\"Defines titles and mail rewards granted for achievements.\",\"achievement_scripts\":\"Binds achievement checks to compiled C++ scripts.\",\"areatrigger\":\"Persistent area-trigger spawn placements.\",\"areatrigger_template\":\"Defines an area trigger's shape and base behavior.\",\"areatrigger_template_actions\":\"Actions associated with an area-trigger template.\",\"areatrigger_create_properties\":\"Shape, motion, and timing properties for spell-created area triggers.\",\"areatrigger_create_properties_orbit\":\"Orbital motion configuration for an area-trigger creation property.\",\"areatrigger_create_properties_polygon_vertex\":\"Ordered polygon vertices for an area-trigger creation property.\",\"areatrigger_create_properties_spline_point\":\"Ordered spline control points for an area-trigger creation property.\",\"areatrigger_involvedrelation\":\"Connects client area triggers to quest exploration/completion credit.\",\"areatrigger_scripts\":\"Binds client area-trigger handling to compiled scripts.\",\"areatrigger_tavern\":\"Marks client area triggers as resting locations.\",\"areatrigger_teleport\":\"Teleport destinations and requirements for client area triggers.\",\"battle_pet_breeds\":\"Allowed breeds for battle-pet species.\",\"battle_pet_quality\":\"Quality configuration for battle-pet species.\",\"battlefield_template\":\"Configuration and script bindings for battlefield systems.\",\"battleground_scripts\":\"Compiled script bindings for battleground types.\",\"battleground_template\":\"Battleground team sizes, level limits, and starting locations.\",\"battlemaster_entry\":\"Maps NPC templates to the battleground types they offer.\",\"blackmarket_template\":\"Defines possible black-market auction offerings.\",\"character_template\":\"Named character creation presets.\",\"character_template_class\":\"Race, faction, and class combinations for character presets.\",\"class_expansion_requirement\":\"Expansion eligibility for playable classes.\",\"command\":\"Database overrides for chat-command help and permission settings.\",\"conditions\":\"Reusable typed predicates that gate spells, gossip, loot, quests, spawns, and other content.\",\"conversation_actors\":\"Actor slots and creature references for conversations.\",\"conversation_line_template\":\"Timing and actor information for conversation lines.\",\"conversation_template\":\"Conversation definitions, initial lines, texture kits, and script bindings.\",\"creature\":\"Persistent NPC spawns: template, placement, phase, difficulty, and per-spawn overrides.\",\"creature_addon\":\"Per-spawn path, appearance, emote, and aura configuration.\",\"creature_classlevelstats\":\"Base creature combat statistics by class and level.\",\"creature_equip_template\":\"Named equipment sets for creature templates.\",\"creature_formations\":\"Leader/member associations and follow geometry for creature formations.\",\"creature_immunities\":\"Reusable sets of school, mechanic, effect, and other creature immunities.\",\"creature_model_info\":\"Display-model collision dimensions and gender/model relationships.\",\"creature_movement_info\":\"Movement speed/timing information.\",\"creature_movement_override\":\"Per-spawn overrides of creature movement capabilities.\",\"creature_onkill_reputation\":\"Faction reputation awarded when a creature is killed.\",\"creature_quest_currency\":\"Currency relevant to a creature's quest interactions.\",\"creature_questender\":\"Creature templates that accept a quest turn-in.\",\"creature_questitem\":\"Quest-related item annotations for creature templates.\",\"creature_queststarter\":\"Creature templates that offer quests.\",\"creature_static_flags_override\":\"Difficulty-specific static creature flag overrides.\",\"creature_summon_groups\":\"Groups of creatures summoned together by a typed summoner.\",\"creature_summoned_data\":\"Template data specific to summoned creatures.\",\"creature_template\":\"Base NPC definitions shared by creature spawns and summoned creatures.\",\"creature_template_addon\":\"Template-level defaults for paths, appearance, emotes, and auras.\",\"creature_template_difficulty\":\"Difficulty-specific creature tuning, loot references, and static flags.\",\"creature_template_gossip\":\"Menus available to a creature template.\",\"creature_template_model\":\"Weighted display-model choices for creature templates.\",\"creature_template_movement\":\"Template-level movement capabilities.\",\"creature_template_resistance\":\"Creature template resistance by spell school.\",\"creature_template_sparring\":\"Sparring behavior and health limits for creature templates.\",\"creature_template_spell\":\"Spells assigned to creature template slots.\",\"creature_text\":\"Groups of NPC speech lines, probabilities, emotes, sounds, and broadcast-text references.\",\"creature_trainer\":\"Connects NPC templates and gossip selections to trainer definitions.\",\"criteria_data\":\"Additional typed requirements for achievement criteria.\",\"destructible_hitpoint\":\"Health configuration for destructible gameobjects.\",\"disables\":\"Typed switches disabling specific content or map-processing features.\",\"event_script_names\":\"Compiled script bindings for game event identifiers.\",\"event_scripts\":\"Legacy database command sequences triggered by events.\",\"exploration_basexp\":\"Base exploration experience by player level.\",\"game_event\":\"Calendar and progression definitions for world events.\",\"game_event_arena_seasons\":\"Connects scheduled game events to arena seasons.\",\"game_event_condition\":\"Progress targets used by world-event conditions.\",\"game_event_creature\":\"Creature spawn participation in world events.\",\"game_event_creature_quest\":\"Creature quest availability during a world event.\",\"game_event_gameobject\":\"Gameobject spawn participation in world events.\",\"game_event_gameobject_quest\":\"Gameobject quest availability during a world event.\",\"game_event_model_equip\":\"Event-specific creature model and equipment overrides.\",\"game_event_npc_vendor\":\"Vendor offerings enabled during a world event.\",\"game_event_npcflag\":\"Event-specific NPC interaction flag overrides.\",\"game_event_pool\":\"Spawn pools controlled by world events.\",\"game_event_prerequisite\":\"Prerequisite world events for progression events.\",\"game_event_quest_condition\":\"Quest contributions to world-event progress.\",\"game_event_seasonal_questrelation\":\"Associates seasonal quests with events for reset tracking.\",\"game_tele\":\"Named destinations used by game-master teleport commands.\",\"game_weather\":\"Zone weather probabilities by season.\",\"gameobject\":\"Persistent gameobject spawns and their placements, rotations, phases, and difficulty settings.\",\"gameobject_addon\":\"Per-spawn gameobject addon configuration.\",\"gameobject_overrides\":\"Per-spawn gameobject faction and flag overrides.\",\"gameobject_questender\":\"Gameobject templates that accept quest turn-ins.\",\"gameobject_questitem\":\"Quest-related item annotations for gameobject templates.\",\"gameobject_queststarter\":\"Gameobject templates that offer quests.\",\"gameobject_template\":\"Shared object definitions; Data0–Data34 are interpreted according to object type.\",\"gameobject_template_addon\":\"Template-level gameobject faction, flags, art, and other addon defaults.\",\"garrison_follower_class_spec_abilities\":\"Ability choices for garrison follower class specializations.\",\"garrison_plot_finalize_info\":\"Faction-specific plot completion positions and animations.\",\"gossip_menu\":\"NPC dialogue menus and their NPC-text records.\",\"gossip_menu_addon\":\"Additional menu-level gossip configuration.\",\"gossip_menu_option\":\"Selectable gossip options and their navigation, interaction, and confirmation settings.\",\"graveyard_zone\":\"Associates zones and teams with resurrection locations.\",\"guild_rewards\":\"Items available as guild rewards and their requirements.\",\"guild_rewards_req_achievements\":\"Achievement requirements for guild reward items.\",\"instance_spawn_groups\":\"Controls spawn groups using instance boss-state conditions.\",\"instance_template\":\"Instance map parent relationships and compiled instance scripts.\",\"item_random_bonus_list_template\":\"Weighted item bonus-list selections.\",\"item_script_names\":\"Compiled item-use script bindings.\",\"item_template_addon\":\"Server-only item behavior supplementing client/hotfix item definitions.\",\"jump_charge_params\":\"Motion parameters for jump and charge effects.\",\"lfg_dungeon_rewards\":\"Quest rewards for dungeon-finder completion by level.\",\"lfg_dungeon_template\":\"Dungeon-finder entry locations and custom dungeon settings.\",\"linked_respawn\":\"Typed dependencies between creature and gameobject respawn schedules.\",\"mail_level_reward\":\"Mail rewards sent when characters reach configured levels.\",\"mount_definitions\":\"Server-side mount definitions and associated spell data.\",\"npc_spellclick_spells\":\"Spells cast when players interact with spell-click NPCs.\",\"npc_text\":\"Weighted broadcast-text choices used by gossip menus.\",\"npc_vendor\":\"NPC vendor stock, prices, conditions, and item/currency offerings.\",\"outdoorpvp_template\":\"Compiled script bindings for outdoor PvP systems.\",\"page_text\":\"Chained readable pages used by items and other content.\",\"pet_levelstats\":\"Base pet statistics by creature and level.\",\"pet_name_generation\":\"Name fragments used to generate pet names.\",\"phase_area\":\"Phases applied within specific areas.\",\"phase_name\":\"Human-readable phase names for authoring and diagnostics.\",\"player_classlevelstats\":\"Base player class statistics by level.\",\"player_racestats\":\"Base racial statistics.\",\"player_xp_for_level\":\"Experience required to advance from each player level.\",\"playerchoice\":\"Player-choice windows and presentation settings.\",\"playerchoice_response\":\"Responses offered by player-choice windows.\",\"playerchoice_response_maw_power\":\"Maw-power presentation/configuration for player-choice responses.\",\"playerchoice_response_reward\":\"Base rewards attached to player-choice responses.\",\"playerchoice_response_reward_currency\":\"Currency rewards for a player-choice response.\",\"playerchoice_response_reward_faction\":\"Faction reputation rewards for a player-choice response.\",\"playerchoice_response_reward_item\":\"Fixed item rewards for a player-choice response.\",\"playerchoice_response_reward_item_choice\":\"Selectable item rewards for a player-choice response.\",\"playercreateinfo\":\"Starting map and position by race and class.\",\"playercreateinfo_action\":\"Starting action-bar buttons by race and class.\",\"playercreateinfo_cast_spell\":\"Spells cast during character creation.\",\"playercreateinfo_item\":\"Additional starting items by race and class.\",\"playercreateinfo_spell_custom\":\"Custom starting spells selected by race/class masks.\",\"points_of_interest\":\"Map markers shown by gossip and navigation interactions.\",\"pool_members\":\"Typed creature, gameobject, or child-pool membership and selection chances.\",\"pool_template\":\"Spawn-pool definitions and maximum active member counts.\",\"quest_completion_log_conditional\":\"Condition-specific quest completion-log text.\",\"quest_description_conditional\":\"Condition-specific quest description text.\",\"quest_details\":\"Emotes and delays shown when offering quest details.\",\"quest_greeting\":\"Creature/gameobject quest greeting text and emotes.\",\"quest_mail_sender\":\"Overrides the sender of a quest's reward mail.\",\"quest_objectives\":\"Typed objective requirements and progress storage for quests.\",\"quest_objectives_completion_effect\":\"Effects played when quest objectives complete.\",\"quest_offer_reward\":\"Reward-dialogue text and emotes.\",\"quest_offer_reward_conditional\":\"Condition-specific reward-dialogue text.\",\"quest_poi\":\"Quest objective map-overlay blob metadata.\",\"quest_poi_points\":\"Ordered coordinates composing quest POI blobs.\",\"quest_pool_members\":\"Quest membership in rotating quest pools.\",\"quest_pool_template\":\"Rotating quest-pool definitions and selection settings.\",\"quest_request_items\":\"Progress-dialogue text and emotes for incomplete/complete objectives.\",\"quest_request_items_conditional\":\"Condition-specific quest progress-dialogue text.\",\"quest_reward_choice_items\":\"Additional typed choice rewards for quests.\",\"quest_reward_display_spell\":\"Spells displayed as quest rewards.\",\"quest_reward_house_decor\":\"Housing decoration rewards for quests.\",\"quest_reward_house_room\":\"Housing room rewards for quests.\",\"quest_template\":\"Quest identity, presentation, reward, race eligibility, and flag data.\",\"quest_template_addon\":\"Server-side prerequisites, chain relationships, skills, scripts, and other quest settings.\",\"quest_treasure_pickers\":\"Treasure-picker rewards attached to quests.\",\"quest_visual_effect\":\"Visual effects attached to quests.\",\"race_unlock_requirement\":\"Playable race expansion and achievement requirements.\",\"reputation_reward_rate\":\"Faction-specific reputation rate multipliers by reward source.\",\"reputation_spillover_template\":\"Reputation spillover destinations, rates, and rank limits.\",\"scenario_poi\":\"Scenario map-overlay blob metadata.\",\"scenario_poi_points\":\"Ordered coordinates composing scenario POI blobs.\",\"scenarios\":\"Map/difficulty scenario assignments.\",\"scene_template\":\"Scene package configuration and compiled scene script bindings.\",\"script_spline_chain_meta\":\"Sequence and timing metadata for scripted spline chains.\",\"script_spline_chain_waypoints\":\"Ordered coordinates for scripted spline chains.\",\"serverside_spell\":\"Server-only spell definitions not supplied by client spell data.\",\"serverside_spell_effect\":\"Effect definitions for server-only spells.\",\"skill_discovery_template\":\"Random recipe discovery chances during crafting.\",\"skill_extra_item_template\":\"Extra-item creation chances for profession specializations.\",\"skill_fishing_base_level\":\"Required base fishing skill by area.\",\"skill_perfect_item_template\":\"Perfect-result crafting substitutions and probabilities.\",\"skill_tiers\":\"Skill tier thresholds.\",\"smart_scripts\":\"Typed event/action/target programs for SmartAI and related script sources.\",\"spawn_group\":\"Associates typed spawn IDs with spawn-group templates.\",\"spawn_group_template\":\"Spawn-group names and behavior flags.\",\"spawn_tracking\":\"Associates typed spawns with tracking definitions.\",\"spawn_tracking_quest_objective\":\"Quest objectives associated with spawn tracking.\",\"spawn_tracking_state\":\"State configuration for spawn tracking.\",\"spawn_tracking_template\":\"Reusable spawn-tracking definitions.\",\"spell_area\":\"Area, quest, race, gender, and aura requirements for applying spells.\",\"spell_custom_attr\":\"Server-specific spell attribute masks.\",\"spell_enchant_proc_data\":\"Proc chances and conditions for enchantment spells.\",\"spell_group\":\"Spells and nested groups used for aura stacking rules.\",\"spell_group_stack_rules\":\"Stacking rules applied to spell groups.\",\"spell_learn_spell\":\"Secondary spells taught by learning a source spell.\",\"spell_linked_spell\":\"Typed cast/hit/aura links between spells, including signed removal semantics.\",\"spell_pet_auras\":\"Pet auras selected by owner spell and pet entry.\",\"spell_proc\":\"Overrides spell proc filters, chances, cooldowns, and charges.\",\"spell_required\":\"Required prerequisite spells for learning spells.\",\"spell_script_names\":\"Compiled spell/aura script bindings.\",\"spell_target_position\":\"Fixed positional targets for spell effects.\",\"spell_threat\":\"Spell threat additions, multipliers, and attack-power scaling.\",\"spell_totem_model\":\"Totem display model by spell and race.\",\"terrain_swap_defaults\":\"Default terrain replacement maps.\",\"terrain_worldmap\":\"World-map presentation for terrain swaps.\",\"trainer\":\"Trainer identity, category, requirements, and greeting.\",\"trainer_spell\":\"Spells offered by trainers, costs, and prerequisite skills/spells/levels.\",\"transports\":\"Transport gameobject definitions and script bindings.\",\"trinity_string\":\"Server messages and their locale variants.\",\"ui_map_quest\":\"Quest associations with UI maps.\",\"ui_map_quest_line\":\"Quest-line associations with UI maps.\",\"updates\":\"History and checksums of SQL migrations applied by the database updater.\",\"updates_include\":\"Directories and states controlling discovery of SQL migrations.\",\"vehicle_accessory\":\"Per-spawn NPC passengers/accessories for vehicles.\",\"vehicle_seat_addon\":\"Additional vehicle-seat behavior and attachment settings.\",\"vehicle_template\":\"Server-specific vehicle configuration.\",\"vehicle_template_accessory\":\"Template-level NPC passengers/accessories for vehicles.\",\"version\":\"Installed database release, core revision, and cache version.\",\"waypoint_path\":\"Reusable waypoint paths and movement configuration.\",\"waypoint_path_node\":\"Ordered positions, orientation, and pause delays for waypoint paths.\",\"world_safe_locs\":\"Safe locations used for resurrection and teleports.\",\"world_state\":\"Server world-state defaults and configuration.\",\"vw_conditions_with_labels\":\"Custom diagnostic view replacing condition/source numbers with labels; its CASE definitions require auditing.\",\"vw_disables_with_labels\":\"Custom diagnostic view replacing disable source numbers with labels.\",\"vw_smart_scripts_with_labels\":\"Custom diagnostic view replacing SmartAI event/action/target numbers with labels; some mappings are older than this core.\"}")
tables = snapshot['tables']
PURPOSES['command'] = 'Database overrides for chat-command help text.'
columns = collections.defaultdict(list)
indexes = collections.defaultdict(list)
for c in snapshot['columns']: columns[c['TABLE_NAME']].append(c)
for c in snapshot['indexes']: indexes[c['TABLE_NAME']].append(c)
names = {t['TABLE_NAME'] for t in tables}
files = {}
for base in ['src/server/game','src/server/database','src/server/scripts']:
    for p in (ROOT/base).rglob('*'):
        if p.suffix in {'.h','.cpp'}:
            files[p.relative_to(ROOT).as_posix()] = p.read_text(encoding='utf-8',errors='replace')
def esc(v):
    return str(v).replace('|','&#124;').replace('\n','<br>').replace('\r','')
def write(name, body):
    p=OUT/name
    p.parent.mkdir(parents=True,exist_ok=True)
    p.write_text(body.rstrip()+'\n',encoding='utf-8')
def source_link(path,line=1,label=None,depth=1):
    return '['+(label or path+':'+str(line))+']('+('../'*(2+depth))+path+'#L'+str(line)+')'
def purpose(n):
    if n in PURPOSES: return PURPOSES[n]
    if n.endswith('_locale'): return 'Localized text for '+n.removesuffix('_locale')+'. Parent identity fields and locale jointly select each translation.'
    if n.endswith('_loot_template'):
        return 'Loot rows for '+n.removesuffix('_loot_template')+' sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide.'
    if n.startswith('player_factionchange_'):
        return 'Alliance/Horde mappings for '+n.removeprefix('player_factionchange_')+' during player faction changes.'
    raise ValueError(n)
def family(n):
    if n.startswith('vw_'): return 'Diagnostic views'
    if n.endswith('_loot_template'): return 'Loot'
    for prefix,group in [
        ('creature','Creatures'),('quest','Quests'),('gameobject','Gameobjects'),
        ('game_event','World events'),('areatrigger','Area triggers'),
        ('spell','Spells'),('serverside_spell','Spells'),('skill','Professions'),
        ('playerchoice','Player choices'),('player','Players'),('character_template','Players'),
        ('vehicle','Vehicles'),('gossip','NPC interaction'),('trainer','NPC interaction'),
        ('npc','NPC interaction'),('achievement','Achievements'),('criteria','Achievements'),
        ('spawn','Spawns'),('pool','Spawns'),('waypoint','Movement'),
        ('script_spline','Movement'),('phase','Phasing'),('terrain','Phasing'),
        ('conversation','Conversations and scenes'),('scene','Conversations and scenes'),
        ('scenario','Instances and scenarios'),('instance','Instances and scenarios'),
        ('lfg','Instances and scenarios'),('battle','PvP and pets'),('pet','PvP and pets'),
        ('guild','Guilds and rewards'),('item','Items'),('page_text','Items'),
        ('garrison','Garrisons'),('reputation','Reputation')]:
        if n.startswith(prefix): return group
    return 'World systems and administration'

# Logical links are editorial associations, never fabricated SQL foreign keys.
relations = []
def rel(a,c,b,d,note='Logical association; validate against loader.'):
    if a in names and b in names and c in {x['COLUMN_NAME'] for x in columns[a]} and d in {x['COLUMN_NAME'] for x in columns[b]}:
        relations.append((a,c,b,d,note))
for a,c,b,d,note in [
('creature','id','creature_template','entry','Template identity shared by NPC spawns.'),
('gameobject','id','gameobject_template','entry','Template identity shared by gameobject spawns.'),
('creature_addon','guid','creature','guid','Per-spawn addon; template addon provides defaults.'),
('gameobject_addon','guid','gameobject','guid','Per-spawn addon.'),
('creature_movement_override','SpawnId','creature','guid','Per-spawn movement settings.'),
('creature_template','CreatureImmunitiesId','creature_immunities','ID','Reusable immunity definition.'),
('creature_template_difficulty','LootID','creature_loot_template','Entry','Loot entry may differ from creature entry.'),
('creature_template_difficulty','PickPocketLootID','pickpocketing_loot_template','Entry','Pickpocket loot entry.'),
('creature_template_difficulty','SkinLootID','skinning_loot_template','Entry','Skinning loot entry.'),
('creature_template_model','CreatureDisplayID','creature_model_info','DisplayID','Display model metadata.'),
('creature_addon','path_id','waypoint_path','PathId','Movement path.'),
('creature_template_addon','path_id','waypoint_path','PathId','Template movement path.'),
('waypoint_path_node','PathId','waypoint_path','PathId','Ordered nodes within a path.'),
('creature_template_gossip','MenuID','gossip_menu','MenuID','Available menu.'),
('gossip_menu','TextID','npc_text','ID','NPC text for the menu.'),
('gossip_menu_option','MenuID','gossip_menu','MenuID','Menu containing the option.'),
('gossip_menu_option','ActionMenuID','gossip_menu','MenuID','Submenu navigation; zero may mean no navigation.'),
('gossip_menu_option','ActionPoiID','points_of_interest','ID','Map point shown by selection.'),
('creature_trainer','TrainerId','trainer','Id','Trainer offered by NPC/gossip selection.'),
('trainer_spell','TrainerId','trainer','Id','Spells available from trainer.'),
('quest_objectives','QuestID','quest_template','ID','Parent quest.'),
('quest_objectives','ParentObjectiveID','quest_objectives','ID','Objective dependency.'),
('quest_objectives_completion_effect','ObjectiveID','quest_objectives','ID','Objective completion effect.'),
('quest_poi_points','QuestID','quest_template','ID','Also join blob keys to quest_poi.'),
('spawn_group','groupId','spawn_group_template','groupId','Group definition.'),
('pool_members','poolSpawnId','pool_template','entry','Parent pool; member spawnId is typed.'),
('playerchoice_response','ChoiceId','playerchoice','ChoiceId','Responses belonging to a choice.'),
('page_text','NextPageID','page_text','ID','Next readable page; prevent cycles.'),
('spell_group_stack_rules','group_id','spell_group','id','Stacking rule for group.'),
('quest_pool_members','poolId','quest_pool_template','poolId','Rotating quest pool.'),
('quest_pool_members','questId','quest_template','ID','Quest selected by pool.'),
('game_event_prerequisite','eventEntry','game_event','eventEntry','Dependent event.'),
('game_event_prerequisite','prerequisite_event','game_event','eventEntry','Prerequisite event.'),
('game_event_creature','guid','creature','guid','Event-controlled NPC spawn.'),
('game_event_gameobject','guid','gameobject','guid','Event-controlled object spawn.'),
]:
    rel(a,c,b,d,note)
for n in names:
    cs={c['COLUMN_NAME'] for c in columns[n]}
    if n.startswith('creature_template_') and n!='creature_template_locale':
        for c in ['CreatureID','CreatureId','Entry','entry']: rel(n,c,'creature_template','entry','Template extension.')
    if n in ['creature_queststarter','creature_questender','creature_questitem','creature_text','creature_onkill_reputation','npc_vendor']:
        for c in ['id','entry','CreatureID']: rel(n,c,'creature_template','entry','Creature template identity, not spawn GUID.')
    if n in ['gameobject_queststarter','gameobject_questender','gameobject_questitem']:
        rel(n,'id','gameobject_template','entry','Gameobject template identity.')
    if n in ['creature_queststarter','creature_questender','gameobject_queststarter','gameobject_questender']:
        rel(n,'quest','quest_template','ID','Quest offer/turn-in relationship.')
    if n.startswith('quest_') and n not in ['quest_template','quest_objectives','quest_objectives_locale']:
        for c in ['QuestID','QuestId','questId']: rel(n,c,'quest_template','ID','Parent quest.')
    if n.startswith('game_event_'):
        rel(n,'eventEntry','game_event','eventEntry','Event identity; signed event fields require sign-aware interpretation.')
    if n.endswith('_locale'):
        parent=n.removesuffix('_locale')
        if parent in names:
            parentcs={c['COLUMN_NAME'] for c in columns[parent]}
            for c in cs & parentcs:
                if c.lower() in ['id','entry','menuid','optionid','creatureid','groupid','choiceid','responseid']:
                    rel(n,c,parent,c,'Translation parent identity; include all identity components plus locale.')
relations=list(dict.fromkeys(relations))

# Extract actual SQL usage sites and selected-column-to-C++ field mappings.
usage=collections.defaultdict(list)
mapping=collections.defaultdict(dict)
sqlpat=re.compile(r'(?P<strings>"(?:[^"\\]|\\.)*"(?:\s*(?:(?://[^\n]*\n|/\*.*?\*/)\s*)*"(?:[^"\\]|\\.)*")*)',re.S)
for path,txt in files.items():
    if 'WorldDatabase' not in txt: continue
    for match in sqlpat.finditer(txt):
        pieces=re.findall(r'"((?:[^"\\]|\\.)*)"',match.group('strings'))
        sql=''.join(pieces)
        if not re.search(r'\b(?:SELECT|INSERT|UPDATE|DELETE)\b',sql,re.I): continue
        used=re.findall(r'\b(?:FROM|JOIN|INTO|UPDATE)\s+`?([A-Za-z_][A-Za-z0-9_]*)',sql,re.I)
        line=txt.count('\n',0,match.start())+1
        for n in used:
            if n in names:
                site=(path,line,sql)
                if site not in usage[n]: usage[n].append(site)
        select=re.match(r'SELECT\s+(.*?)\s+FROM\s+`?([\w]+)`?',sql,re.I|re.S)
        if not select or select.group(2) not in names or ',' in select.group(1) and '(' in select.group(1): continue
        n=select.group(2)
        sels=[s.strip().strip('`') for s in select.group(1).split(',')]
        end=txt.find('QueryResult ',match.end())
        window=txt[match.end():min(end if end>=0 else len(txt),match.end()+20000)]
        for assignment in re.finditer(r'^([^\n;]*\b\w*[Ff]ields\[(\d+)\][^\n;]*);',window,re.M):
            i=int(assignment.group(2))
            if i<len(sels) and sels[i] in {c['COLUMN_NAME'] for c in columns[n]}:
                aline=line+txt[match.start():match.end()].count('\n')+window[:assignment.start()].count('\n')
                mapping[n].setdefault(sels[i],(path,aline,assignment.group(1).strip()))



# Resolve prepared SQL to positional/named consumers.
prepared={}
dbtxt=files['src/server/database/Database/Implementation/WorldDatabase.cpp']
for m in sqlpat.finditer(dbtxt):
    sql=''.join(re.findall(r'"((?:[^"\\]|\\.)*)"',m.group('strings')))
    sel=re.match(r'SELECT\s+(.*?)\s+FROM\s+\x60?(\w+)\x60?',sql,re.I|re.S)
    before=dbtxt[max(0,m.start()-150):m.start()]
    ident=re.search(r'PrepareStatement\((\w+),\s*$',before)
    if ident and sel and sel.group(2) in names and '(' not in sel.group(1):
        prepared[ident.group(1)]=(sel.group(2),[s.strip().strip(chr(96)) for s in sel.group(1).split(',')])
def map_block(n,sels,path,start,end):
    txt=files[path]
    block=txt[start:end]
    for m in re.finditer(r'^([^\n;]*\b\w*[Ff]ields\[(\d+)\][^\n;]*);',block,re.M):
        i=int(m.group(2))
        if i<len(sels) and sels[i] in {c['COLUMN_NAME'] for c in columns[n]}:
            mapping[n].setdefault(sels[i],(path,txt.count('\n',0,start+m.start())+1,m.group(1).strip()))
    usage[n].append((path,txt.count('\n',0,start)+1,'Prepared/structured query consumer'))
for path,txt in files.items():
    for m in re.finditer(r'GetPreparedStatement\((WORLD_\w+)\)',txt):
        if m.group(1) not in prepared: continue
        n,sels=prepared[m.group(1)]
        next_stmt=txt.find('GetPreparedStatement(',m.end())
        next_func=re.search(r'\n(?:void|bool|uint32|uint64|int32)\s+\w+::',txt[m.end():])
        ends=[len(txt),m.end()+18000]
        if next_stmt>=0: ends.append(next_stmt)
        if next_func: ends.append(m.end()+next_func.start())
        map_block(n,sels,path,m.end(),min(ends))
if 'WORLD_SEL_CREATURE_TEMPLATE' in prepared:
    n,sels=prepared['WORLD_SEL_CREATURE_TEMPLATE']
    path='src/server/game/Globals/ObjectMgr.cpp'
    txt=files[path]
    start=txt.find('void ObjectMgr::LoadCreatureTemplate(')
    if start>=0:
        end=txt.find('\nvoid ObjectMgr::',start+1)
        map_block(n,sels,path,start,end if end>=0 else start+20000)
path='src/server/game/Quests/QuestDef.cpp'
txt=files[path]
start=txt.find('Quest::Quest(')
end=txt.find('Quest::~Quest',start)
block=txt[start:end]
for c in columns['quest_template']:
    k=c['COLUMN_NAME']
    m=re.search(r'^([^\n]*questRecord\.'+re.escape(k)+r'\(\)[^\n]*)',block,re.M)
    if m: mapping['quest_template'][k]=(path,txt.count('\n',0,start+m.start())+1,m.group(1).strip())
usage['quest_template'].append((path,txt.count('\n',0,start)+1,'Structured Quest constructor'))
p='src/server/game/Loot/LootMgr.cpp'
txt=files[p]
for n in names:
    if n.endswith('_loot_template'):
        for line in [144,155,285]: usage[n].append((p,line,'Generic LootStore load/validation'))
        fields=['Entry','ItemType','Item','Chance','QuestRequired','LootMode','GroupId','MinCount','MaxCount']
        for m in re.finditer(r'^([^\n;]*fields\[(\d+)\][^\n;]*);',txt,re.M):
            if 150<=txt.count('\n',0,m.start())+1<=170:
                i=int(m.group(2))
                if i<len(fields): mapping[n][fields[i]]=(p,txt.count('\n',0,m.start())+1,m.group(1).strip())
p='src/server/game/Movement/Waypoints/WaypointManager.cpp'
txt=files[p]
for n,method in [('waypoint_path','LoadPathFromDB'),('waypoint_path_node','LoadPathNodesFromDB')]:
    start=txt.find('void WaypointMgr::'+method+'(')
    end=txt.find('\nvoid WaypointMgr::',start+1)
    block=txt[start:end if end>=0 else len(txt)]
    usage[n].append((p,txt.count('\n',0,start)+1,'Structured prepared-query consumer'))
    for c in columns[n]:
        k=c['COLUMN_NAME']
        for m in re.finditer(r'^([^\n]*fields\.'+re.escape(k)+r'\(\)[^\n]*)',block,re.M):
            mapping[n][k]=(p,txt.count('\n',0,start)+block.count('\n',0,m.start())+1,m.group(1).strip())

COMMON={
'VerifiedBuild':'Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood.',
'ScriptName':'Name of a compiled C++ script registered by this core. Text alone cannot create a script.',
'AIName':'Registered AI implementation name. SmartAI requires the corresponding SmartAI source rows.',
'StringId':'Author-defined string identifier used by object lookup and string-ID conditions.',
'locale':'Locale key (for example deDE or frFR); translates a parent record rather than creating independent gameplay content.',
'Comment':'Authoring/provenance note; do not use it as a gameplay identifier.',
'comment':'Authoring/provenance note; do not use it as a gameplay identifier.',
'description':'Description text; its runtime role depends on the owning table.',
'spawnDifficulties':'Comma-separated difficulty IDs; this is not the older spawnMask bit field.',
'Difficulties':'Difficulty filter expressed as difficulty IDs; inspect SmartScriptMgr parsing for empty-list behavior.',
'orientation':'Facing angle in radians.',
'Orientation':'Facing angle in radians; NULL may leave orientation unspecified according to the loader.',
'spawntimesecs':'Respawn delay in seconds; actual timing is also affected by spawn groups, instances, events, and linked respawns.',
'position_x':'Map-space X coordinate.',
'position_y':'Map-space Y coordinate.',
'position_z':'Map-space Z coordinate (height).',
'PositionX':'Map-space X coordinate.',
'PositionY':'Map-space Y coordinate.',
'PositionZ':'Map-space Z coordinate (height).',
'map':'Client Map record identifier; a map ID is distinct from an instance save ID.',
'zoneId':'Zone AreaTable identifier.',
'areaId':'AreaTable identifier.',
'PhaseId':'Phase identifier used for visibility; examine phaseUseFlags and PhaseGroup together.',
'PhaseGroup':'Client phase-group identifier; do not confuse with an individual phase ID.',
'phaseUseFlags':'Phase interpretation flags; see phase enums and the spawn loader.',
'terrainSwapMap':'Terrain replacement map selector; negative sentinel values are loader-specific.',
'BoxMoney':'Gossip confirmation cost in copper.',
'BoxCoded':'Whether the gossip confirmation asks for typed input.',
'BoxText':'Gossip confirmation prompt.',
'ActionMenuID':'Gossip submenu to open; see logical relationships.',
'ActionPoiID':'Point of interest displayed by gossip selection.',
'MinCount':'Type-dependent count. Item/currency use a positive minimum; tracking quest requires 1. See loot guide.',
'MaxCount':'Type-dependent count. Item/currency require at least MinCount; tracking quest requires 0. References use repeat semantics. See loot guide.',
'Chance':'Selection chance; units and zero behavior depend on the table (see loot/profession guide).',
'QuestRequired':'Loot reward is restricted to qualifying quest needs.',
'LootMode':'Loot-mode bitmask controlling eligibility.',
'GroupId':'Loot roll group; group zero and nonzero groups use different selection rules.',
'ItemType':'LootStoreItem::Type: 0 item, 1 reference, 2 currency, 3 tracking quest. See the loot guide for type-specific count rules.',
'Item':'Typed reward identifier; interpretation follows ItemType, including reference entries.',
'ElseGroup':'Conditions within an ElseGroup are ANDed; distinct groups provide OR alternatives.',
'NegativeCondition':'Negates the predicate when nonzero.',
'ConditionTarget':'Target slot to evaluate; available slots depend on the source type.',
'ConditionTypeOrReference':'Nonnegative condition enum, or negative reusable condition-reference ID.',
'SourceTypeOrReferenceId':'Nonnegative source enum, or negative ID defining a reusable reference template.',
'SourceGroup':'Source-specific group selector; interpretation depends on source type.',
'SourceEntry':'Source-specific entry selector; interpretation depends on source type.',
'SourceId':'Additional source-specific identifier; interpretation depends on source type.',
'ConditionStringValue1':'String operand used by condition types such as String ID.',
'ErrorType':'Condition failure error category; supported by only applicable source types.',
'ErrorTextId':'Client error-text identifier used when the source supports reporting failures.',
'entryorguid':'Template/source entry or negative spawn GUID where supported by source_type.',
'source_type':'SmartAI script owner category; see current SmartScriptType enum.',
'id':'Row identity within this table; use the complete primary key when selecting or editing.',
'link':'SmartAI linked row ID; linked execution uses SMART_EVENT_LINK.',
'event_type':'SmartAI event enum; determines interpretation of event parameters.',
'action_type':'SmartAI action enum; determines interpretation of action parameters.',
'target_type':'SmartAI target enum; determines interpretation of target parameters and coordinates.',
'event_phase_mask':'SmartAI internal phase bitmask; separate from world visibility phases.',
'event_chance':'Probability of executing an eligible SmartAI event, in percent.',
'event_flags':'SmartAI event behavior flags; see SmartAI enum reference.',
'Delay':'Pause/timing value; inspect the owning movement/scene loader for units.',
'Order':'Ordering value within the parent object.',
'StorageIndex':'Quest objective progress storage index; signed values can carry special meanings.',
'ObjectID':'Typed objective operand; Type determines whether this is a creature, item, currency, spell, or another record.',
'ProgressBarWeight':'Contribution of this objective to quest progress-bar completion.',
'ParentObjectiveID':'Parent quest objective identifier.',
'Flags':'Flags interpreted by the owning subsystem; use the linked enum source, not another table\'s flag constants.',
'Flags2':'Additional owning-subsystem flags.',
'FlagsEx':'Extended owning-subsystem flags.',
'FlagsEx2':'Second extended owning-subsystem flag set.',
'FlagsEx3':'Third extended owning-subsystem flag set.',
}
SPECIFIC={
('waypoint_path','PathId'):'Reusable path identity.',
('waypoint_path','MoveType'):'WaypointMoveType enum: path movement style; see spawn/movement enums.',
('waypoint_path','Velocity'):'Optional positive movement velocity; NULL uses the default, and nonpositive values are rejected/reset.',
('waypoint_path_node','NodeId'):'Ordered node identity within PathId.',
('waypoint_path_node','Delay'):'Pause delay in milliseconds; zero means no delay.',
('creature_template_difficulty','DifficultyID'):'Client difficulty ID selecting this template extension.',
('creature_template_difficulty','GoldMin'):'Minimum money drop; use copper units and keep GoldMax at least GoldMin.',
('creature_template_difficulty','GoldMax'):'Maximum money drop; the loader repairs values below GoldMin.',
('creature_template_difficulty','HealthModifier'):'Creature health scaling multiplier.',
('creature_template_difficulty','ManaModifier'):'Creature mana scaling multiplier.',
('creature_template_difficulty','ArmorModifier'):'Creature armor scaling multiplier.',
('creature_template_difficulty','DamageModifier'):'Damage scaling multiplier; the loader also applies classification scaling.',
('creature_template_difficulty','ContentTuningID'):'External content-tuning record used for level/scaling behavior.',
('creature_template_difficulty','LevelScalingDeltaMin'):'Minimum level-scaling delta loaded into DeltaLevelMin.',
('creature_template_difficulty','LevelScalingDeltaMax'):'Maximum level-scaling delta loaded into DeltaLevelMax.',
('creature_template_difficulty','HealthScalingExpansion'):'Expansion selector for health scaling; the loader validates and substitutes invalid values.',
('access_requirement','mapId'):'Client Map identifier whose instance access is restricted.',
('creature','guid'):'Persistent spawn ID; separate from creature_template.entry and the runtime object GUID.',
('creature','id'):'Creature template entry referenced by this spawn.',
('gameobject','guid'):'Persistent spawn ID; separate from gameobject_template.entry.',
('gameobject','id'):'Gameobject template entry referenced by this spawn.',
('creature','wander_distance'):'Random movement radius around the spawn location.',
('creature','MovementType'):'Default movement generator type; see MovementGeneratorType.',
('creature','curHealthPct'):'Optional starting health percentage override.',
('creature','modelid'):'Optional spawn display-model override.',
('creature','equipment_id'):'Equipment-set selector; signed sentinel values are interpreted by the spawn/equipment loaders.',
('gameobject_template','type'):'Gameobject type discriminator; determines the complete Data0–Data34 layout.',
('quest_objectives','Type'):'Quest objective type discriminator; selects ObjectID and Amount interpretation.',
('quest_objectives','Amount'):'Required progress or quantity, interpreted by objective Type.',
('quest_template','RewardNextQuest'):'Quest presented after rewarding this quest; does not by itself encode every prerequisite.',
('quest_template','TimeAllowed'):'Quest time limit; inspect QuestDef and Quest.cpp for conversion to timers.',
('quest_template','AllowableRaces'):'Race eligibility mask; modern race masks may require wider-than-32-bit arithmetic.',
('quest_template','RewardFavor'):'Reward favor value read by the current quest loader.',
('npc_vendor','entry'):'Creature template entry offering this stock.',
('npc_vendor','maxcount'):'Stock limit; zero conventionally indicates unlimited stock.',
('npc_vendor','incrtime'):'Limited-stock replenishment time; inspect vendor stock code for timing.',
}
def field_note(n,c):
    key=c['COLUMN_NAME']
    if (n,key) in SPECIFIC: return SPECIFIC[n,key]
    if n.startswith('vw_'): return 'Projected/derived view output; see the view definition and caveats below.'
    links=[r for r in relations if r[0]==n and r[1]==key]
    if links: return '; '.join('Logical reference to ['+r[2]+'.'+r[3]+']('+r[2]+'.md). '+r[4] for r in links)
    if n=='gameobject_template' and re.fullmatch(r'Data\d+',key): return 'Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type.'
    if n=='conditions' and key.startswith('ConditionValue'): return 'Typed predicate operand; exact layout is documented in [condition enums](../reference/conditions-enums.md) and ConditionMgr.cpp.'
    if n=='smart_scripts' and re.match(r'(event|action|target)_param',key): return 'Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md).'
    if n=='creature_template_difficulty' and key.startswith('StaticFlags'): return 'Creature static behavior mask for flag set '+key.removeprefix('StaticFlags')+'. See [creature static enums](../reference/spawn-enums.md).'
    if key in COMMON: return COMMON[key]
    if c['COLUMN_COMMENT']: return 'Database comment: '+c['COLUMN_COMMENT']
    if key in mapping[n]: return 'Runtime field mapping is shown below; special values and validation are governed by that loader.'
    if key.lower()=='entry' or key=='ID': return 'Record identifier; consult the complete primary key and relationships before treating it as a template ID.'
    return '**Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing.'
groups=collections.defaultdict(list)
for t in tables: groups[family(t['TABLE_NAME'])].append(t['TABLE_NAME'])
for t in tables:
    n=t['TABLE_NAME']
    b='# '+n+'\n\n[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)\n\n'+purpose(n)+'\n\n'
    b+='## Schema\n\nCaptured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **'+t['TABLE_TYPE']+'**. '
    b+='Engine: '+str(t['ENGINE'] or 'not applicable')+'. Collation: '+str(t['TABLE_COLLATION'] or 'not applicable')+'.\n\n'
    if t['TABLE_COMMENT']: b+='Database comment: '+esc(t['TABLE_COMMENT'])+'\n\n'
    b+='| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |\n| --- | --- | --- | --- | --- | --- | --- | --- |\n'
    for c in columns[n]:
        default='NULL / absent; see conventions' if c['COLUMN_DEFAULT'] is None else '`'+esc(c['COLUMN_DEFAULT'])+'`'
        if c['COLUMN_DEFAULT']=='': default='`\'\'`'
        vals=[c['ORDINAL_POSITION'],'`'+c['COLUMN_NAME']+'`','`'+c['COLUMN_TYPE']+'`',c['IS_NULLABLE'],default,c['COLUMN_KEY'] or '—',c['EXTRA'] or '—',field_note(n,c)]
        b+='| '+' | '.join(esc(v) for v in vals)+' |\n'
    b+='\n## Keys and indexes\n\n'
    ix=collections.defaultdict(list)
    for row in indexes[n]: ix[row['INDEX_NAME']].append(row)
    if ix:
        b+='| Index | Unique | Ordered columns | Method |\n| --- | --- | --- | --- |\n'
        for key,rs in ix.items():
            b+='| `'+esc(key)+'` | '+('Yes' if rs[0]['NON_UNIQUE']==0 else 'No')+' | '+', '.join('`'+str(r['COLUMN_NAME'])+'`'+(' (prefix '+str(r['SUB_PART'])+')' if r['SUB_PART'] else '') for r in rs)+' | '+rs[0]['INDEX_TYPE']+' |\n'
    else: b+='No indexes were reported in information_schema for this object.\n'
    fk=[r for r in snapshot['constraints'] if r['TABLE_NAME']==n and r['REFERENCED_TABLE_NAME']]
    b+='\n## Relationships\n\n'
    if not fk: b+='No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.\n\n'
    else:
        for r in fk: b+='- Enforced: '+r['COLUMN_NAME']+' → '+r['REFERENCED_TABLE_NAME']+'.'+r['REFERENCED_COLUMN_NAME']+'\n'
    rr=[r for r in relations if r[0]==n or r[2]==n]
    if rr:
        for a,c,d,e,note in rr:
            b+='- ['+a+']('+a+'.md).`'+c+'` → ['+d+']('+d+'.md).`'+e+'`: '+note+'\n'
    else: b+='No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.\n'
    b+='\n## Runtime evidence\n\n'
    sites=usage[n]
    if sites:
        b+='Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.\n\n'
        for path,line,sql in sorted(sites,key=lambda s:('scripts/' in s[0], 'database/' in s[0], s[0],s[1]))[:10]:
            b+='- '+source_link(path,line)+'\n'
        if len(sites)>10: b+='\nAdditional source references exist; search the repository for the exact table name.\n'
        if mapping[n]:
            b+='\n### Selected column mappings\n\nThese are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.\n\n| Column | C++ assignment / conversion | Source |\n| --- | --- | --- |\n'
            for c in columns[n]:
                k=c['COLUMN_NAME']
                if k in mapping[n]:
                    p,l,code=mapping[n][k]
                    b+='| `'+k+'` | `'+esc(code)+'` | '+source_link(p,l,'loader')+' |\n'
    else:
        b+='No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.\n'
    if t['TABLE_TYPE']=='VIEW':
        v=next(v for v in snapshot['views'] if v['TABLE_NAME']==n)
        b+='\n## View definition and caveats\n\nSecurity mode: '+v['SECURITY_TYPE']+'. MySQL reports updatable: '+v['IS_UPDATABLE']+'. Treat this as a diagnostic projection and edit the numeric base table deliberately. The definition is local database customization, not proof of an upstream standard view.\n\n'
        if n=='vw_conditions_with_labels':
            b+='**Confirmed definition error:** the CASE expression for ConditionTypeOrReference compares SourceTypeOrReferenceId instead of ConditionTypeOrReference. It can show the wrong predicate name. The view also omits ConditionStringValue1 and uses older condition names. Use the base conditions table and current ConditionMgr enums.\n\n'
        if n=='vw_smart_scripts_with_labels':
            b+='**Version drift:** older labels include event 46 as AREATRIGGER_ONTRIGGER; the current core names it AREATRIGGER_ENTER. Some projected fields omit newer Difficulties and string/seventh-action operands. Use the base smart_scripts table and current enums.\n\n'
        b+='```sql\n'+v['VIEW_DEFINITION']+'\n```\n'
    b+='\n## Inspection example\n\nThis query is read-only. Substitute explicit identity filters before using data in an update.\n\n```sql\nSELECT * FROM `'+n+'` LIMIT 5;\n```\n\n'
    if n.endswith('_loot_template'): b+='See [loot](../guides/loot.md) for typed rewards, roll groups, and reference relationships.\n\n'
    if n.endswith('_locale'): b+='Translations must match the parent\'s full identity and an accepted locale; see [localization](../guides/localization.md).\n\n'
    b+='## Further reference\n\n[Master wiki candidate page](https://trinitycore.info/database/master/world/'+n+') — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch\'s page.\n'
    write('tables/'+n+'.md',b)

# Preserve enum expressions and inline operand comments verbatim from local source.
enumsets={
'conditions-enums.md':['src/server/game/Conditions/ConditionMgr.h'],
'smartai-enums.md':['src/server/game/AI/SmartScripts/SmartScriptMgr.h'],
'quest-enums.md':['src/server/game/Quests/QuestDef.h'],
'areatrigger-enums.md':['src/server/game/Entities/AreaTrigger/AreaTriggerTemplate.h'],
'spawn-enums.md':['src/server/game/Maps/SpawnData.h','src/server/game/Movement/MovementGenerator.h','src/server/game/Movement/Waypoints/WaypointDefines.h','src/server/game/Entities/Creature/CreatureData.h'],
'loot-enums.md':['src/server/game/Loot/LootMgr.h','src/server/game/Miscellaneous/SharedDefines.h'],
'disable-enums.md':['src/server/game/Conditions/DisableMgr.h'],
'spell-enums.md':['src/server/game/Spells/SpellInfo.h','src/server/game/Spells/SpellDefines.h'],
'world-enums.md':['src/server/game/Miscellaneous/SharedDefines.h','src/server/game/Entities/Unit/UnitDefines.h','src/server/game/Entities/GameObject/GameObjectData.h'],
}
enum_counts={}
for out,paths in enumsets.items():
    b='# '+out.removesuffix('.md').replace('-',' ').title()+'\n\n[Database documentation](../README.md)\n\nSource-derived reference for revision 914a6f655c97. Explicit values, expressions, reserved values, and comments are preserved from local headers. Implicit C++ enum values increment from the preceding enumerator; do not assign a maximum/count sentinel to data. Bit masks may combine flags, while ordinary enums select one value. Inline parameter comments describe type-dependent operand order. The runtime implementation remains authoritative if a comment is incomplete.\n\n'
    count=0
    for p in paths:
        if p not in files: continue
        txt=files[p]
        for m in re.finditer(r'\benum\s+(?:class\s+)?([A-Za-z_]\w*)[^;{]*\{.*?\};',txt,re.S):
            if out=='loot-enums.md' and p.endswith('SharedDefines.h') and not re.search(r'Loot',m.group(1)): continue
            if out=='world-enums.md' and not re.search(r'GameObject|NPC|Npc|UnitFlags|Creature|Phase|Loot|TypeMask|Team|Race|Gender|SpellSchool|Reputation|Difficulty',m.group(1)): continue
            count+=1
            line=txt.count('\n',0,m.start())+1
            b+='## '+m.group(1)+'\n\n'+source_link(p,line,depth=1)+'\n\n```cpp\n'+m.group(0)+'\n```\n\n'
    write('reference/'+out,b)
    enum_counts[out]=count
p='src/server/game/Entities/GameObject/GameObjectData.h'
txt=files[p]
m=re.search(r'union\s*\{',txt)
b='# Gameobject type-dependent data layouts\n\n[gameobject_template](../tables/gameobject_template.md) · [World enums](world-enums.md)\n\nData0–Data34 are ordered storage slots in the GameObjectTemplate union. Select the block corresponding to gameobject_template.type, then count that block\'s uint32/int32 fields from Data0. A loot slot in one type may be a lock or other identifier in another. Comments include units and client record references where known. Unused slots should follow existing verified rows rather than assumptions.\n\n'+source_link(p,txt.count('\n',0,m.start())+1,depth=1)+'\n\n'
if m:
    start=m.start(); brace=txt.index('{',start); level=1; end=brace+1
    while end<len(txt) and level:
        if txt[end]=='{': level+=1
        elif txt[end]=='}': level-=1
        end+=1
    b+='```cpp\n'+txt[start:end+1]+'\n```\n'
write('reference/gameobject-data.md',b)

b='# Logical relationships\n\n[Database documentation](README.md)\n\nNo SQL foreign keys were reported for the captured world schema. The graph and catalog describe logical associations, not enforcement. Presence of a key or index does not guarantee referential integrity. Zero/signed sentinel values and polymorphic selectors need loader-specific treatment.\n\n```mermaid\nerDiagram\n    creature_template ||--o{ creature : defines\n    creature ||--o| creature_addon : configures\n    creature_template ||--o{ creature_template_difficulty : tunes\n    creature_template_difficulty }o--o{ creature_loot_template : selects\n    gameobject_template ||--o{ gameobject : defines\n    quest_template ||--o{ quest_objectives : requires\n    creature_template ||--o{ creature_queststarter : offers\n    quest_template ||--o{ creature_queststarter : offered_by\n    gossip_menu ||--o{ gossip_menu_option : contains\n    trainer ||--o{ trainer_spell : teaches\n    waypoint_path ||--o{ waypoint_path_node : contains\n```\n\n## Association catalog\n\n| From | To | Interpretation |\n| --- | --- | --- |\n'
for a,c,d,e,note in sorted(relations):
    b+='| ['+a+'.'+c+'](tables/'+a+'.md) | ['+d+'.'+e+'](tables/'+d+'.md) | '+note+' |\n'
b+='\n## Polymorphic and external relationships\n\n- conditions source fields refer to different world tables according to SourceTypeOrReferenceId; predicate operands depend on ConditionTypeOrReference.\n- smart_scripts ownership depends on source_type; negative entryorguid selects a spawn where supported. Event/action/target parameters are typed operands.\n- Loot ItemType selects an item, currency, reference entry, or another supported reward kind; do not assume every Item value is an item ID.\n- spawn_group, pool_members, linked_respawn, and spawn_tracking use type discriminators for creature/gameobject/pool IDs.\n- gameobject_template Data slots are selected by type.\n- Spell, item, faction, map, area, display, broadcast text, difficulty, and many modern quest reward IDs refer to client DB2/hotfix data. They need not have a world table with the same name.\n- Localized tables often have composite parent identities. Joining only the first key can duplicate or misassociate text.\n'
write('relationships.md',b)
b='# TrinityCore world database\n\nDocumentation for the connected **master** world database, captured **2026-10-09**. Core: `914a6f655c973d57c392ae78c92c14c5376f8e38`; database: **TDB 1210.26091**; cache ID: **26091**. The database version row matches the inspected checkout.\n\nCoverage: **246 base tables, 3 views, 1,994 columns**. Every object has a page containing exact captured SQL types, nullability, default metadata, indexes, inspection SQL, and available runtime evidence. This is complete schema coverage; independently unresolved field meanings are marked explicitly rather than guessed.\n\n## Start here\n\n- [Conventions and version scope](conventions.md)\n- [Logical relationships](relationships.md)\n- [Creatures and spawns](guides/creatures.md)\n- [Gameobjects](guides/gameobjects.md)\n- [Quests](guides/quests.md)\n- [Loot](guides/loot.md)\n- [Gossip, vendors, and trainers](guides/npc-interaction.md)\n- [SmartAI](guides/smartai.md)\n- [Conditions](guides/conditions.md)\n- [Movement, events, pools, and phasing](guides/world-content.md)\n- [Spells, professions, and rewards](guides/spells-and-rewards.md)\n- [Localization](guides/localization.md)\n- [Operations and troubleshooting](guides/operations.md)\n- [Sources and evidence limits](sources.md)\n- [Maintenance and regeneration](maintenance.md)\n- [Captured schema metadata](schema-snapshot.md)\n- [Coverage report](coverage.md)\n\n## Enum and data references\n\n'
for f in enumsets: b+='- ['+f.removesuffix('.md').replace('-',' ').title()+'](reference/'+f+')\n'
b+='- [Gameobject Data0–Data34 layouts](reference/gameobject-data.md)\n\n## Table index\n\n'
for group,ns in sorted(groups.items()):
    b+='### '+group+'\n\n| Object | Purpose |\n| --- | --- |\n'
    for n in ns: b+='| ['+n+'](tables/'+n+'.md) | '+purpose(n)+' |\n'
    b+='\n'
write('README.md',b)
unknown=[(n,c['COLUMN_NAME']) for n in names for c in columns[n] if field_note(n,c).startswith('**Meaning not')]
b='# Coverage and verification\n\n[Database documentation](README.md)\n\n## Captured inventory\n\n| Measure | Count |\n| --- | --- |\n| Base tables | 246 |\n| Views | 3 |\n| Columns | '+str(len(snapshot['columns']))+' |\n| Index column entries | '+str(len(snapshot['indexes']))+' |\n| Logical association entries | '+str(len(relations))+' |\n| Columns with extracted runtime mappings | '+str(sum(len(m) for m in mapping.values()))+' |\n| Fields whose meaning remains independently unresolved | '+str(len(unknown))+' |\n\nSchema completeness is distinct from semantic certainty. A source mapping shows what is loaded; it does not prove all allowed values, units, or sentinel behavior. Wiki candidate links are navigation aids, not individually reviewed citations.\n\n## Enum extraction\n\n'
for f,c in enum_counts.items(): b+='- ['+f+'](reference/'+f+'): '+str(c)+' enum blocks.\n'
b+='\n## Unresolved field meanings\n\nThese fields have no editorial interpretation, nonempty database comment, logical link, or extracted direct loader assignment in this pass. Investigate source references on the parent page, generic loaders, client DB2 layouts, and verified data before editing.\n\n| Table | Column |\n| --- | --- |\n'
for n,c in sorted(unknown): b+='| ['+n+'](tables/'+n+'.md) | `'+c+'` |\n'
write('coverage.md',b)
print(json.dumps({'objects':len(tables),'columns':len(snapshot['columns']),'logical_links':len(relations),'mapped_columns':sum(len(v) for v in mapping.values()),'unresolved_fields':len(unknown),'enum_blocks':enum_counts},indent=2))

```
