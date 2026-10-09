# Exile's Reach: functionality and scripting

Exile's Reach has a substantial server implementation. Both factions have starting transports, introductory scenes, ship quests, personal NPCs, and beach-arrival scripts. **This audit does not establish that the whole zone is complete or playable end to end.** The opening's database dependencies were checked; the client spell/scene data and an actual playthrough remain necessary to confirm the transition works.

Start with [the ship-to-beach walkthrough](exiles-reach-ship-to-beach.md) for the exact sequence requested: spawn aboard, watch the introduction, talk to Jaina or Thrall, train, finish Brace for Impact, and arrive on the beach. Use [validation and troubleshooting](exiles-reach-validation.md) to investigate failures.

## What runs where?

A zone is assembled from several layers:

| Layer | Responsibility | Example here |
| --- | --- | --- |
| Character creation and login | Choose the initial position and start the first-login scene | `playercreateinfo`, `Player::Create`, login handler |
| World database | Store NPCs, quest relationships, objectives, paths, and script bindings | `creature`, `quest_template`, `scene_template` |
| C++ scripts | React to quest status, summon personal actors, move them, process scene/movie callbacks | `zone_exiles_reach.cpp` |
| Client DB2 data and hotfixes | Define spell effects and other game-data records consumed by the core | Movie/scene/teleport effects |
| Client scene packages | Present authored cameras, animation, and scene trigger events | Intro and washed-up-on-beach scenes |

A `ScriptName` connects a database record to a registered C++ script. A spell does not need a custom `spell_script_names` row when its ordinary effects already implement its behavior. Similarly, an empty hotfix table result does not mean a spell is missing: the baseline record can come from extracted DB2 files.

**A scene and a movie are different mechanisms.** A scene has a scene template/package and scene callbacks. A movie has a movie ID and a movie-completion callback. The opening uses both.

## Maps and transports

| ID | Meaning in this flow |
| --- | --- |
| Map `2175` | Exile's Reach world map, including the starting transports and beach |
| Map `2261` | Alliance transport passenger/spawn map |
| Map `2369` | Horde transport passenger/spawn map |
| Map `2236` | Darkmaul Citadel instance |
| Transport GUID `29` | Alliance starting ship, gameobject template `333479` |
| Transport GUID `30` | Horde starting ship, gameobject template `349879` |

Transport GUIDs come from `transports`. They are not interchangeable with `gameobject.guid`. Ship NPC positions are defined through passenger maps and transport-relative coordinates; the player still starts on world map `2175`.

## Jaina and Thrall versus the names in the code

The live database calls the opening Alliance leader **Lady Jaina Proudmoore** and the Horde leader **Thrall**. The source retains names such as `Garrick`, `Grimaxe`, `npc_captain_garrick`, and `q59928_grimaxe`.

Those older identifiers are still used by the live bindings. For example, entry `156280` is named Jaina but runs `npc_captain_garrick`. Renaming the C++ classes or `StringId` values merely to match display names can break those connections. A name difference by itself does not establish a scripting defect. Later island NPC names and dialogue need a separate consistency review; do not assume the whole story was updated because the ship leaders were renamed.

## Implementation inventory beyond the opening

The following sections are registered in `AddSC_zone_exiles_reach`. This is an inventory of code, not a completed gameplay test.

| Section | Server behavior represented in the source | Audit status |
| --- | --- | --- |
| Ship | Tutorial, warming up, sparring, storm actors, movie completion | Detailed source/database trace documented |
| Beach | Knockdown, personal leader greeting, survivor/first-aid behavior, murlocs, expedition search | Arrival traced; remaining quests not played through |
| Abandoned camp | Cooking quests and expedition-following area triggers | Source inventory only |
| Enhanced Combat Tactics | Personal trainers, class training, aggro checks, knockback/charge handling | Source inventory only |
| Northbound | Summoned leader, movement and linger scene handling | Source inventory only |
| Taming the Wilds | Faction quests and tutorial health behavior | Source inventory only |
| Briarpatch | Prisoners, Geolord Grekog, quilboar/ogre behavior, transition trigger | Source inventory only |
| Plains scouting | Scout-o-Matic 5000 and Choppy Booster Mk. 5 vehicles/actors | Source inventory only |
| Resizing the Situation | Guardian/boar summoning and resizing spell scripts | Source inventory only |
| Giant boar / Re-Deather | Vehicle, skeleton army scenes, objective credit and cleanup | Source inventory only |
| Westward Bound | Faction quests and personal ruins actors | Source inventory only |
| Darkmaul Citadel | Instance script and dedicated Tunk boss script | Separate encounter/content audit required |
| Zone departure and capital handoff | Not established by this opening audit | Needs quest, spell, transport and gameplay tracing |

The module loader registers `AddSC_zone_exiles_reach`, `AddSC_instance_darkmaul_citadel`, and `AddSC_boss_tunk`. The dungeon header identifies Tunk, Gorgroth, and Ravnyr; only Tunk has a dedicated boss file in this module. This alone does not prove that the other encounters are absent: database AI or another mechanism must be checked before making that claim.

## Is it complete?

The evidence supports **an implemented opening with important unverified transitions**, not a declaration of full completion. No missing starting transport, ship quest, required storm-actor StringId, or enumerated ship movement path was found in the checks described in these guides.

The key limits are:

- The reward-spell-to-movie and crash-spell-to-teleport/scene links were not independently decoded from baseline DB2 data. The queried hotfix spell-effect rows were empty.
- The beach scene has a completion handler but no script-specific cancel handler. Its configured flags do not include `NotCancelable`; cancellation needs testing.
- Several actor searches silently skip work when a transport or nearby actor is absent.
- Fresh-login, disconnect recovery, two-player isolation, the full island quest chain, dungeon, and departure have not been tested in a client.

See the [validation guide](exiles-reach-validation.md) for the difference between a confirmed code gap and a demonstrated player-facing bug.

## Sources and version scope

This guide uses local source and read-only MCP queries against the installed world database on 2026-10-09. Core and database version metadata matched revision `914a6f655c973d57c392ae78c92c14c5376f8e38`; that does not independently prove the running executable includes every script in this checkout.

- [Zone scripts](../../src/server/scripts/ExilesReach/zone_exiles_reach.cpp)
- [Module registration](../../src/server/scripts/ExilesReach/exiles_reach_script_loader.cpp)
- [Darkmaul Citadel sources](../../src/server/scripts/ExilesReach/DarkmaulCitadel/instance_darkmaul_citadel.cpp)
- [Character creation and quest engine](../../src/server/game/Entities/Player/Player.cpp)
- [First-login handler](../../src/server/game/Handlers/CharacterHandler.cpp)
- [Creation-data loader](../../src/server/game/Globals/ObjectMgr.cpp)
- [Scene manager](../../src/server/game/Entities/Player/SceneMgr.cpp)

Blizzard's [new-player starter guide](https://news.blizzard.com/en-us/article/24266319/new-players-starter-guide-welcome-to-world-of-warcraft) confirms that the retail experience begins aboard a ship with movement, NPC interaction, and class basics. It is background context, not evidence that this server implements each step correctly.
