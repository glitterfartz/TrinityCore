# AGENTS.md — src/server/scripts

Guidance for AI coding agents working on TrinityCore content scripts. Read this before adding or debugging a script. Repo-wide build/DB instructions are in the root [`AGENTS.md`](../../../AGENTS.md) and [`sql/AGENTS.md`](../../../sql/AGENTS.md).

## What this tree is

~842 `.cpp` / ~131 `.h` files across 26 module directories. It is the *content* layer: bosses, dungeons, zones, quests, spells, chat commands, battlegrounds. The engine they plug into is `src/server/game` (see `src/server/game/AGENTS.md`).

Every direct child directory of this folder is a **script module**, auto-discovered by CMake:

`Argus Battlefield Battlegrounds BrokenIsles Commands Custom Draenor DragonIsles EasternKingdoms Events ExilesReach Kalimdor Karesh KhazAlgar KulTiras Maelstrom Northrend OutdoorPvP Outland Pandaria Pet QuelThalas Shadowlands Spells World Zandalar`

Largest modules (cpp files): EasternKingdoms 198, Northrend 167, Kalimdor 117, Outland 101, Commands 44, Battlegrounds 42, Spells 19, Events 15, World 15.

## The loader chain (read this first)

Scripts are **not** registered by namespace-scope/static initializers. Construction must happen inside a call chain started by `ScriptMgr::Initialize()`:

1. Each module has a hand-maintained loader, e.g. `EasternKingdoms/eastern_kingdoms_script_loader.cpp`. It forward-declares every `AddSC_*()` in that module and calls them from one exported function named exactly `Add<Directory>Scripts()` (`AddEasternKingdomsScripts()`, `AddSpellsScripts()`, `AddCommandsScripts()` — note the plural).
2. CMake generates `build/src/server/scripts/gen_scriptloader/static/ScriptLoader.cpp` from `ScriptLoader.cpp.in.cmake`. It declares each `Add<Module>Scripts()` and defines `AddScripts()` to call them.
3. `worldserver/Main.cpp` calls `sScriptMgr->SetScriptLoader(AddScripts)`; `ScriptMgr::Initialize()` (`src/server/game/Scripting/ScriptMgr.cpp`) invokes it. Only then do the `AddSC_*` functions construct script objects.
4. A script base-class constructor calls `ScriptRegistry<T>::Instance()->AddScript(this)`, which binds the object to its name / script id.

Consequences:

- Registering a script at namespace scope (or from any code that runs before step 3) asserts.
- A module whose `Add<Dir>Scripts()` is missing/wrong fails to link (static) or fails to `dlopen` (dynamic).
- `AddSC_*` is never called by the engine directly; if you add a file but forget to add `AddSC_my_thing()` to that module's loader, it silently does nothing.

## Registration API

Base class: `ScriptObject` (`src/server/game/Scripting/ScriptMgr.h`). Real registration macros and what they expect:

| Macro | Class must derive from | Constructor |
|---|---|---|
| `RegisterCreatureAI(ai)` | `CreatureAI` | `ai(Creature*)` |
| `RegisterCreatureAIWithFactory(ai, fn)` | `CreatureAI` | factory `ai*(Creature*)` |
| `RegisterGameObjectAI(ai)` | `GameObjectAI` | `ai(GameObject*)` |
| `RegisterGameObjectAIWithFactory(ai, fn)` | `GameObjectAI` | factory `ai*(GameObject*)` |
| `RegisterAreaTriggerAI(ai)` | `AreaTriggerAI` | `ai(AreaTrigger*)` |
| `RegisterConversationAI(ai)` | `ConversationAI` | `ai(Conversation*)` |
| `RegisterSpellScript(cls)` | `SpellScript` **or** `AuraScript` | default-constructible |
| `RegisterSpellScriptWithArgs(cls, name, ...)` | `SpellScript`/`AuraScript` | args forwarded |
| `RegisterSpellAndAuraScriptPair(spell, aura)` | one of each | default-constructible |
| `RegisterBattlegroundMapScript(cls, mapId)` | `BattlegroundScript` | `cls(BattlegroundMap*)` |

These macros do **not** exist in this tree (old docs/examples may claim otherwise): `RegisterInstanceScript`, `RegisterCommandScript`, `RegisterWorldScript`, `RegisterPlayerScript`, `RegisterAreaTriggerScript`, `RegisterConditionScript`, `RegisterAuraScript`. Construct those directly with `new` inside `AddSC_*`, e.g. `new instance_blackrock_caverns();`, `new my_commandscript();`, `new my_worldscript();`, `new my_playerscript();`, `new my_conditionscript();`. An aura-only script is registered with `RegisterSpellScript(my_aura)`.

Other script bases (all in `ScriptMgr.h`): `WorldScript`, `ServerScript`, `FormulaScript`, `WorldMapScript`, `InstanceMapScript`, `BattlegroundMapScript`, `ItemScript`, `UnitScript`, `CreatureScript` (legacy `GetAI()` form), `GameObjectScript` (legacy), `AreaTriggerScript`, `BattlefieldScript`, `OutdoorPvPScript`, `CommandScript`, `WeatherScript`, `AuctionHouseScript`, `ConditionScript`, `VehicleScript`, `DynamicObjectScript`, `TransportScript`, `AchievementScript`, `AchievementCriteriaScript`, `PlayerScript`, `AccountScript`, `GuildScript`, `GroupScript`, `AreaTriggerEntityScript`, `ConversationScript`, `SceneScript`, `QuestScript`, `WorldStateScript`, `EventScript`, `PlayerChoiceScript`, `SpellScriptLoader`.

Two registry flavors matter:
- **DB-bound** (`CreatureScript`, `GameObjectScript`, `InstanceMapScript`, `SpellScriptLoader`, `QuestScript`, `AreaTriggerScript`, `ConditionScript`, …): keyed by the numeric script id from `ObjectMgr::GetScriptId(name)`. Two scripts with the same name in one registry **abort startup**.
- **Global/fan-out** (`WorldScript`, `PlayerScript`, `CommandScript`, …): every registered script receives the hook; no DB name lookup.

## Adding a script file

1. Pick the module directory, e.g. `World/` or `EasternKingdoms/BlackrockMountain/BlackrockCaverns/`.
2. Define the class and `void AddSC_my_thing() { RegisterCreatureAI(my_ai); /* or new ... */ }`.
3. Add `void AddSC_my_thing();` plus a call inside `Add<Module>Scripts()` in that module's loader `.cpp`.
4. Re-run CMake. Sources are collected with `file(GLOB ...)` **without** `CONFIGURE_DEPENDS`, so a configure pass is required after adding/removing files or module dirs.
5. If the script is DB-bound, put the exact name (the constructor/macro string) in the right DB column — see below.

Adding a **new module directory**: create `src/server/scripts/NewZone/` with `new_zone_script_loader.cpp` defining `AddNewZoneScripts()`. No CMake edit is needed; re-run CMake. Optionally select it with `-DSCRIPTS_NEWZONE=static|dynamic|disabled`.

## Content layout and naming

- Expansion/continent module → `zone_*.cpp` at module root for open-world content; one subdirectory per dungeon/raid (sometimes grouped, e.g. `EasternKingdoms/BlackrockMountain/{BlackrockCaverns,BlackrockDepths,...}`, `Kalimdor/CavernsOfTime/...`).
- File prefixes (observed): `boss_` (~410), `instance_` (~115), `zone_` (~74), `cs_` (44, chat commands), `spell_` (21), `arena_` (20), `battleground_` (12), `pet_` (7), law `npc_`/`npcs_`, `go_`, `areatrigger_`, `quest_`, `worldboss_`, `*_chapter_N_*.cpp`.
- There is **no `sq_` prefix** and no `sQuestMgr`. Quest scripts are `quest_*` classes deriving `QuestScript`.
- Filenames are organizational only; the functional identity is the constructor/macro string (the DB `ScriptName`).
- Coverage is partial. A dungeon directory may contain only `instance_*.cpp`; do not assume every boss is scripted.

## Dungeon wiring, end to end

1. `<dungeon>.h`: `#define XScriptName "instance_x"` (must match DB `instance_template.script`), `#define DataHeader "XX"` (save-format version), `EncounterCount`, `DATA_*` boss indices, `NPC_*`/`GO_*` entries, and the factory helpers:
   `GetXAI` → `GetInstanceAI<AI>(obj, XScriptName)` and `#define RegisterXCreatureAI(ai) RegisterCreatureAIWithFactory(ai, GetXAI)`.
2. `instance_<dungeon>.cpp`: an `InstanceMapScript(XScriptName, mapId)` plus the nested `InstanceScript`. Its constructor calls `SetHeaders(DataHeader)`, `SetBossNumber(EncounterCount)`, `LoadObjectData(...)`, `LoadDoorData(...)`, `LoadMinionData(...)`, `LoadDungeonEncounterData(...)`.
3. `boss_<name>.cpp`: modern form `struct boss_x : public BossAI { boss_x(Creature* c) : BossAI(c, DATA_X) {} ... }`. `BossAI` bridges the AI to the `InstanceScript` (encounter state, doors, minions, journal). Use plain `ScriptedAI` only for adds/trash/custom AIs; use `CreatureScript`+`GetAI()` only for legacy files.
4. Encounter spell/aura/areatrigger scripts usually live in the same boss file and are registered from the same `AddSC_*`.
5. Add every `AddSC_*` to the module loader.
6. DB: `instance_template.script = XScriptName` for the map; `creature_template.ScriptName = boss/NPC script name`; `spell_script_names`, `areatrigger_scripts`/`areatrigger_create_properties.ScriptName`, `quest_template_addon.ScriptName`, `gameobject_template.ScriptName` as applicable.

Important:
- `SetHeaders(DataHeader)` is instance-save format versioning. Change the `DATA_*` layout → bump it, or old instance saves fail to load.
- In a dungeon module prefer the module's `Register<Zone>CreatureAI` factory macro over bare `RegisterCreatureAI`. `GetInstanceAI` only attaches the AI when the creature is inside an instance whose `InstanceScript` name matches; a plain registration attaches it globally.
- `DATA_*` values are boss indices, not creature entries.

## DB binding (script names are exact and case-sensitive)

| Script kind | Where the name lives |
|---|---|
| Creature AI | `creature_template.ScriptName`; per-spawn override `creature.ScriptName` (wins) |
| GameObject | `gameobject_template.ScriptName`; per-spawn `gameobject.ScriptName` |
| Instance | `instance_template.script` |
| Spell / aura | `spell_script_names.spell_id` → `ScriptName` (negative `spell_id` = all ranks) |
| Quest | `quest_template_addon.ScriptName` |
| Area trigger | `areatrigger_scripts.ScriptName`, `areatrigger_create_properties.ScriptName` |
| Scene / conversation | `scene_template.ScriptName`, `conversation_template.ScriptName` |
| Condition | `conditions.ScriptName` |
| Event / achievement / item | `event_script_names`, `achievement_scripts`, `item_script_names` |
| Battleground / battlefield / OutdoorPvP | `battleground_scripts`, `battlefield_template.ScriptName`, `outdoorpvp_template.ScriptName` |

There is **no generic `script_names` table** in the 12.x world DB. Unknown DB names are logged at startup ("Script 'X' is referenced by the database, but does not exist in the core!"); a C++ name with no DB row simply never runs. Both are silent in-game, so always check both sides.

Finding the script behind a content id:

```bash
# creature
grep -rn '"npc_some_name"' src/server/scripts
grep -rnE '(class|struct) npc_some_name' src/server/scripts
# instance
grep -rn 'instance_some_dungeon' src/server/scripts
# spell
grep -rn 'spell_some_name' src/server/scripts
```

or query `world`/`hotfixes` through the local MariaDB MCP (see root AGENTS.md) before grepping SQL files.

## Commands (`Commands/`)

- Files `cs_<topic>.cpp`; class `<topic>_commandscript : public CommandScript` constructed with a name like `"bg_commandscript"`.
- `GetCommands()` returns a `static ChatCommandTable` of `ChatCommandBuilder` entries: `{ "bg start", &Handler, LANG_COMMAND_BG_START_HELP, rbac::RBAC_PERM_COMMAND_BG_START, Console::No }`. The command path is the full subcommand path; the handler is `static bool Handler(ChatHandler* handler, ...)`.
- Register via `AddSC_<topic>_commandscript()` in `Commands/cs_script_loader.cpp`; module loader is `AddCommandsScripts()`.
- New RBAC permissions are appended to `enum RBACPermissions` in `src/server/game/Accounts/RBAC.h` before `RBAC_PERM_MAX` (never reuse retired numbers) and need matching `rbac_permissions` / `rbac_linked_permissions` rows in the **auth** DB (normally an `sql/updates/auth/...` file). No DB row stores the command name; the C++ table is authoritative.

## Spells (`Spells/`)

- One file per class family (`spell_dk.cpp`, `spell_druid.cpp`, …), plus `spell_generic.cpp`, `spell_item.cpp`, `spell_quest.cpp`, `spell_pet.cpp`, `spell_azerite.cpp`. Naming contract in file headers: `spell_dk_*`, `npc_pet_<class>_*`, etc.
- Prefer `RegisterSpellScript` / `RegisterSpellAndAuraScriptPair` over `SpellScriptLoader` subclasses.
- `Validate()` returning false disables the script at load; a `ScriptName` absent from `spell_script_names` means it never runs.
- Expansion-owned spell scripts may live outside this folder (e.g. `Shadowlands/spell_covenant.cpp`, `Shadowlands/Torghast/spell_torghast.cpp`).

## SmartAI vs C++

DB-driven `smart_scripts` (creature SAI) is an alternative to a C++ `CreatureAI`. A creature uses it when `creature_template.AIName = 'SmartAI'`; `ScriptName` (C++) takes precedence if both are set. `smart_scripts.entryorguid` is a template entry when positive, a spawn `guid` when negative. Do not add a C++ AI that duplicates existing SAI rows.

## Custom module

`Custom/` contains only `custom_script_loader.cpp` with an empty `AddCustomScripts()`. It is a normal module and is compiled by default, but `-DSCRIPTS=minimal-static|minimal-dynamic` whitelists only `Commands` and `Spells`, disabling `Custom` (and `World`, and every expansion) unless `-DSCRIPTS_CUSTOM=...` is passed. Put user SQL in `sql/custom/world/`, not here.

## Build configuration

- `SCRIPTS=none|static|dynamic|minimal-static|minimal-dynamic` (default `static`). Per-module overrides: `-DSCRIPTS_<UPPERDIR>=default|disabled|static|dynamic`.
- `minimal-*` enables only `Commands` and `Spells`.
- **Any module built `dynamic` forces `WITH_DYNAMIC_LINKING` and therefore `BUILD_SHARED_LIBS=ON` for the entire project.** Dynamic modules are `scripts_<module>` shared libs installed under `bin/scripts`; they enable hot-swap.
- Static is the default and is what this checkout uses. In static builds the hot-swap config (`HotSwap.*`) is inert and `ScriptReloadMgr` is a no-op.
- `USE_SCRIPTPCH` (default ON) force-includes `ScriptPCH.h` via CMake. **Do not `#include "ScriptPCH.h"` in a `.cpp`** — but do include what you use so `-DUSE_SCRIPTPCH=0` still compiles. Editing `ScriptPCH.h` rebuilds every script module.

## Gotchas

1. No static registration; only construct scripts from `AddSC_*` reachable from `Add<Module>Scripts()`.
2. Duplicate DB-bound names abort startup — they are not last-wins.
3. Missing `AddSC_*` call = script silently never loads.
4. Exact, case-sensitive `ScriptName` matching on both the DB and C++ side.
5. Re-run CMake after adding/removing files or module directories.
6. `instance_template.script` and the `InstanceMapScript` constructor `mapId` must both be correct; a name-only fix leaves the wrong map scripted.
7. Hot reload only applies to `dynamic` modules and only to DB templates that call `NotifyScriptIDUpdate`; compiled C++ changes need a rebuild/restart.
8. `doc/HowToScript.txt` and several `doc/*.dox` pages are stale (they mention `scripts_STAT_SRCS` and `RegisterAuraScript`). Trust `ScriptMgr.h/.cpp` and the CMake over those docs.
