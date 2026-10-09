# Exile's Reach: from the starting ship to the beach

The short version: character creation attaches the player to the faction's ship, first login starts an intro scene, and finishing or skipping that scene starts the tutorial. The player completes **three ship quests**, not just one. Brace for Impact prepares personal storm actors; its reward spell leads into the crash movie. The movie callback casts the faction's crash spell. A separate beach scene then triggers the knockdown and personal leader greeting.

The world records and C++ callbacks below were checked against revision `914a6f655c97` and `TDB 1210.26091` on 2026-10-09. The downstream client spell effects are explicitly marked where they remain unverified.

## 1. Character creation puts the player on the ship

The character-creation request carries `UseNPE` (new-player experience). In `Player::Create`, the core uses `createPositionNPE` if the request selects NPE and valid NPE creation data exists. Otherwise it uses the normal racial start. Creating a character does not guarantee Exile's Reach unless that choice and race/class data support it.

`playercreateinfo` supplies the following installed settings:

| Setting | Alliance | Horde |
| --- | --- | --- |
| `npe_map` | `2175` | `2175` |
| `npe_transport_guid` | `29` | `30` |
| `npe_position_x` | `11.1301` | `-10.7291` |
| `npe_position_y` | `-0.417182` | `-7.14635` |
| `npe_position_z` | `5.18741` | `8.73113` |
| `npe_orientation` | `3.14843` | `1.56321` |
| `npe_intro_scene_id` | `2236` | `2486` |
| Configured race/class combinations | `57` | `58` |

These are **positions relative to the ship**, not beach coordinates. The core creates the map, looks up the transport, adds the player as a passenger, and transforms the relative position into a world position through `GetPositionWithOffset`.

The transport records are:

| Transport | Template | Taxi path | Passenger/spawn map |
| --- | --- | --- | --- |
| `29`, NPE - Alliance Ship | `333479`, Alliance Ship | `7748` | `2261` |
| `30`, NPE - Horde Transport | `349879`, Horde Transport | `8099` | `2369` |

At startup, `ObjectMgr` validates the NPE map and transport spawn. An invalid transport reference clears the NPE creation data because its position was assumed to be transport-relative. There is another runtime transport lookup in `Player::Create`; the shown block has no explicit recovery if that lookup fails. A player appearing near the map origin instead of aboard the ship warrants checking both loading and runtime transport availability.

Source: `Player::Create` in [Player.cpp](../../src/server/game/Entities/Player/Player.cpp), and `LoadPlayerInfo` NPE handling in [ObjectMgr.cpp](../../src/server/game/Globals/ObjectMgr.cpp).

## 2. First login starts the introduction

The login handler checks the character's `cinematic` state. When the introduction has not already been marked as handled, it sets that state and, for NPE creation mode, plays `introSceneIdNPE`.

| Faction | Scene ID | Scene package | Flags | Script |
| --- | --- | --- | --- | --- |
| Alliance | `2236` | `2578` | `40` (`0x28`) | `scene_alliance_and_horde_ship` |
| Horde | `2486` | `2894` | `40` (`0x28`) | `scene_alliance_and_horde_ship` |

Do not confuse scene ID `2236` with map ID `2236` (Darkmaul Citadel); they are different ID namespaces.

`scene_alliance_and_horde_ship` casts spell `295600`, `SPELL_BEGIN_TUTORIAL`, on **both completion and cancellation**. Skipping the introduction therefore has an explicit script route into the tutorial. The exact conversation/effect chain of `295600` depends on spell data and was not decoded in this audit.

The attention aura `290901` has a custom removal handler: removing its root effect casts `290903` (the source calls it Debug Look Right). This is another piece of the guided opening, separate from quest completion.

Because the cinematic state is set before the first-login sequence finishes, a reconnect is not guaranteed to rerun this block. Interruption recovery requires a real disconnect test; it is not established by the normal completion callback.

## 3. Talk to Jaina or Thrall and complete Warming Up

| Faction | Quest | Objective | Initial giver/ender |
| --- | --- | --- | --- |
| Alliance | `56775`, Warming Up | Destroy a Combat Dummy, credit entry `174954` | `156280`, Lady Jaina Proudmoore |
| Horde | `59926`, Warming Up | Destroy a Combat Dummy, credit entry `174954` | `166573`, Thrall |

The `quest_template_addon.ScriptName` bindings are `q56775_warming_up` and `q59926_warming_up`.

The shared warming-up behavior starts conversation `12818` when the quest becomes `INCOMPLETE` and conversation `12798` when it becomes `COMPLETE`. **Complete** means the objective is satisfied; **rewarded** means the player has turned in the quest. The distinction matters here: the leader's personal movement is started on `REWARDED`.

On reward, the script finds a lower-deck and upper-deck leader using these exact `creature.StringId` values:

| Role | Alliance | Horde |
| --- | --- | --- |
| Lower-deck source | `q56775_garrick_lower_deck` | `q59926_grimaxe_lower_deck` |
| Upper-deck source | `q56775_garrick_upper_deck` | `q59926_grimaxe_upper_deck` |

It searches the lower actor within 5 yards and the upper actor within 75 yards, ignoring phases. Both must be found. It creates a personal clone of the upper actor near the lower actor, and that clone runs the movement script. A personal clone belongs to one player, so separate players can see their own sequence.

The clone removes its questgiver flag, moves toward the sparring area, then goes upstairs and despawns. Its paths are `10501450`/`10501451` for Alliance and `10501900`/`10501901` for Horde. All four paths and all four source StringIds exist in the installed database.

The source's Garrick/Grimaxe names are historical identifiers. Horde uses multiple Thrall entries (`166573`, `166824`, `166827`) for different stages; the script does not require them to be one creature template.

## 4. Complete Stand Your Ground

| Faction | Quest | Giver/ender | Objective |
| --- | --- | --- | --- |
| Alliance | `58209`, Stand Your Ground | `160664` | Spar with Private Cole |
| Horde | `59927`, Stand Your Ground | `166583` | Spar with Grunt Throg |

The previous quest requirements are `56775` and `59926` respectively. Both quests bind `quest_stand_your_ground` and reward spell `316454`.

The first mate's `OnQuestAccept` casts phase-update spell `82238`, then summon spell `303064` (Alliance) or `325107` (Horde). The associated sparring-partner spell scripts (`303065`/`325108`) select nearby source actors by StringId `q58209_cole` or `q59927_throg`, within 10 yards, ignoring phases.

The personal sparring AI is a training fight. When the player's hit would be lethal, it prevents the kill, leaves the trainer at 1 health, stops combat, makes the trainer immune/uninteractive, casts `323071`, and awards the owner kill credit **`155607`**. Both quest objectives use this credit even though the actual personal sparring actors are entries `157051` and `166814`.

The script also has health-based movement and training dialogue. Its paths are `10501460` (Alliance) and `10501870` (Horde). Abandoning the quest casts `82238` and `303120` to update the training state; abandonment and retaking still need gameplay testing.

## 5. Brace for Impact prepares the storm

| Faction | Quest | Previous quest | Giver | Ender | Reward spell |
| --- | --- | --- | --- | --- | --- |
| Alliance | `58208`, Brace for Impact | `58209` | `160664` | `156280` (Jaina) | `305425` |
| Horde | `59928`, Brace for Impact | `59927` | `166583` | `166827` (Thrall) | `325131` |

Neither quest has `quest_objectives` rows in this database. The quest engine can complete quests whose requirements are already met; this is a conversation/turn-in stage rather than another combat objective. The exact client dialogue should be verified in-game.

Both bind `quest_brace_for_impact`. Its callback acts on **`QUEST_STATUS_COMPLETE`**, not `REWARDED`. It prepares personal storm actors while the player is still aboard the ship:

- Alliance: `q58208_garrick`, `richter`, `keela`, `bjorn`, `austin`, `cole` (each suffix uses the same `q58208_` prefix).
- Horde: `q59928_grimaxe`, `throg`, `mithdran`, `lana`, `bo`, `jinhake` (each suffix uses `q59928_`).

The script transforms actor offsets using the player's **direct transport**, then clones the matching source NPCs. A hunter also gets a race-specific pet actor where the source is available. Finally it casts phase-update spell `82238`.

All twelve crew StringIds and the fourteen configured faction pet StringIds were present in the database. This proves their records exist, not that phasing/range conditions always make them discoverable at runtime.

The leader, first mate, crew, and pet have timed speech/movement scripts. Relevant paths, all present with at least one node, are:

| Actor group | Alliance paths | Horde paths |
| --- | --- | --- |
| Leader | `10505890`, `10505891` | `10501910`, `10501911` |
| First mate | `10501461` | `10501871` |
| Crew | `10501770`, `10501800`, `10501790`, `10501780` | `10502010`, `10501990`, `10501980`, `10502000` |
| Pet | `10501510` | `10502020` |

## 6. Turn in the quest and advance through the crash movie

Turning in Brace for Impact rewards spell `305425` or `325131`. The general spell engine supports `SPELL_EFFECT_PLAY_MOVIE` (`45`): it reads the movie ID from the effect's misc value, validates the Movie record, and sends the movie start to the player.

The Exile's Reach script explicitly expects:

| Faction | Crash movie | Spell cast after movie completion |
| --- | --- | --- |
| Alliance | `895` | `305446` |
| Horde | `931` | `325133` |

**Verification boundary:** the installed quest reward spells and the C++ movie callback were verified. The baseline effect records proving that `305425`/`325131` start those movies, and that `305446`/`325133` perform the beach teleport/scene chain, were not decoded. Those spells had no matching rows in the queried hotfix spell-effect table. The normal flow depends on baseline DB2 records, which must be inspected or exercised in a client before calling this bridge fully verified.

`WorldSession::HandleCompleteMovie` uses the player's stored current movie ID, clears it, and calls the player-script hook. The client acknowledgement does not supply an arbitrary movie ID to this handler. `player_exiles_reach_ship_crash::OnMovieComplete` then casts the faction spell shown above.

The C++ crash callback contains no explicit beach coordinates. Changing its spell ID or adding a manual teleport without inspecting the downstream spell effects risks skipping scene, transport, or phase cleanup.

## 7. The beach scene knocks the player down and greets them

| Faction | Beach scene | Package | Flags | Script |
| --- | --- | --- | --- | --- |
| Alliance | `2334` | `2708` | `16` (`0x10`) | `scene_alliance_and_horde_crash` |
| Horde | `2487` | `2708` | `16` (`0x10`) | `scene_alliance_and_horde_crash` |

The crash scene listens for the exact client trigger string **`Begin Knockdown Aura`** and casts `305445`. Removing that spell's stun effect casts `344889`, the follow-up knockdown stun.

On normal scene completion, it casts `305464` (Alliance) or `325136` (Horde). Those spells bind `spell_crash_landed_alliance` and `spell_crash_landed_horde`, which share a C++ implementation. On effect 0's `SEND_EVENT`, the script searches within 50 yards for the faction's static beach leader:

| Faction | Beach leader entry | Installed name | Script |
| --- | --- | --- | --- |
| Alliance | `156626` | Lady Jaina Proudmoore | `npc_captain_garrick_beach` |
| Horde | `166782` | Thrall | `npc_warlord_grimaxe_beach` |

It summons a personal clone at that leader's location. The arrival clone faces the player, delivers its arrival text, and despawns after five seconds. The static leader remains available for the next beach quests. The source identifies Murloc Mania as `55122`/`59929` and Emergency First Aid as `54951`/`59930` for Alliance/Horde.

Unlike the intro script, the crash scene has **no `OnSceneCancel` override**. Scene flags `16` do not contain `NotCancelable` (`0x04`). The scene manager dispatches cancellation separately from completion, so the completion-only leader-summoning spell is not called by this script on cancellation. Whether this leaves a visible or progression problem must be tested; the static leader and other spell effects may allow the player to continue.

## Where to make changes

| Desired change | Start here |
| --- | --- |
| Starting position or which ship receives a race/class | `playercreateinfo` NPE fields and `transports`; preserve relative coordinates |
| Intro scene selection | `npe_intro_scene_id`, `scene_template`, first-login state |
| Displayed leader name | `creature_template`; review related dialogue/localization separately |
| Quest order or giver/ender | `quest_template_addon`, `creature_queststarter`, `creature_questender` |
| Dummy or sparring objective | `quest_objectives` plus scripted credit in the sparring AI |
| Personal actor selection | Exact `creature.StringId` values and script search ranges |
| Ship movement and speech | C++ event timing, `waypoint_path`/`waypoint_path_node`, `creature_text` |
| Movie/teleport transition | Quest reward spell, baseline spell effects, movie callback, beach scene |
| Skip/disconnect recovery | First-login state, movie acknowledgement, scene completion/cancel paths |

Use the [validation guide](exiles-reach-validation.md) before changing any of these dependencies. Do not rename historical identifiers independently of their database bindings.
