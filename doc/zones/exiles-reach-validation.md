# Exile's Reach: validation and troubleshooting

This checklist accompanies the [zone overview](exiles-reach.md) and [ship-to-beach walkthrough](exiles-reach-ship-to-beach.md). It separates observed source/database facts from failures that still need to be reproduced.

Snapshot: 2026-10-09, core `914a6f655c97`, `TDB 1210.26091`. All database inspection for this documentation was read-only. No client playthrough or server content changes were performed.

## Findings and open questions

| Finding | Evidence | Practical interpretation |
| --- | --- | --- |
| Both faction starts are configured | NPE creation rows, transport GUIDs 29/30, scene templates 2236/2486 exist | Opening infrastructure is present |
| Three-quest chains are connected | Previous-quest IDs, giver/ender relationships, objective and reward-spell records inspected | Quest graph supports the documented opening |
| Ship actors and movement paths exist | Four warming-up leader StringIds, twelve storm crew StringIds, fourteen pet StringIds, and 22 enumerated paths found | No missing record in this checked dependency set; visibility and geometry remain untested |
| Jaina/Thrall use historical identifiers | Live template names differ from source class names while IDs and bindings connect | Name mismatch is not itself a defect |
| Intro skip has a continuation callback | Intro scene handles both complete and cancel by casting 295600 | Intended skip route exists; downstream spell behavior still needs testing |
| Beach scene lacks a cancel continuation | Crash script only casts arrival spell on completion; flags 16 omit NotCancelable | Confirmed script gap; player-facing progression impact is unproven |
| Actor lookup failures are silent | Warming-up returns if either leader is missing; storm spawning skips absent transport/actors; arrival clone requires a nearby leader | Missing dialogue/movement can occur without a clear script log |
| Runtime transport lookup has no explicit fallback in creation block | Player creation only attaches/transforms if transport lookup succeeds | Investigate runtime loading if a player starts off-ship; not a reproduced spawn bug |
| First-login state is marked before intro finishes | Login handler sets cinematic state before playing NPE scene | Reconnect replay/recovery is unverified |
| Spell-effect bridge remains unverified | Relevant hotfix spell-effect query returned no rows; baseline DB2 records not decoded | Do not infer missing spells; inspect extracted client data and test reward/movie/teleport chain |
| Whole-zone completion is unverified | Later sections inventoried; no full client run | Do not describe the zone as complete based on the opening audit |

## Read-only database checks

Run these against the world database used by the active worldserver. They are inspection queries, not repair SQL. Compare IDs and bindings with the walkthrough rather than copying values from an older expansion's database.

### Starting ships and scenes

```sql
SELECT race, class, npe_map, npe_transport_guid,
       npe_position_x, npe_position_y, npe_position_z,
       npe_orientation, npe_intro_scene_id
FROM playercreateinfo
WHERE npe_map IS NOT NULL
ORDER BY race, class;

SELECT * FROM transports WHERE guid IN (29, 30);
SELECT * FROM gameobject_template WHERE entry IN (333479, 349879);
SELECT * FROM scene_template WHERE SceneId IN (2236, 2486, 2334, 2487);
```

For the ships' type-15 gameobject templates, `Data0` identifies taxi paths `7748`/`8099`, and `Data6` identifies passenger maps `2261`/`2369`. Taxi-path records and scene packages also depend on compatible client data. The inspected transport rows had empty `ScriptName`; transport behavior does not require a bespoke ship C++ script here.

### Quest progression and reward spells

```sql
SELECT ID, LogTitle, RewardSpell, Flags
FROM quest_template
WHERE ID IN (56775, 58209, 58208, 59926, 59927, 59928);

SELECT * FROM quest_template_addon
WHERE ID IN (56775, 58209, 58208, 59926, 59927, 59928);

SELECT * FROM quest_objectives
WHERE QuestID IN (56775, 58209, 58208, 59926, 59927, 59928);

SELECT * FROM creature_queststarter
WHERE quest IN (56775, 58209, 58208, 59926, 59927, 59928);
SELECT * FROM creature_questender
WHERE quest IN (56775, 58209, 58208, 59926, 59927, 59928);
```

Expected reward spells: Warming Up `0`; Stand Your Ground `316454`; Brace for Impact Alliance `305425`, Horde `325131`. Brace for Impact has no objective rows in this snapshot. Both sparring quests use objective credit entry `155607`.

### Actors and bindings

```sql
SELECT guid, id, map, StringId, phaseId, phaseGroup
FROM creature
WHERE StringId LIKE 'q56775_%'
   OR StringId LIKE 'q59926_%'
   OR StringId LIKE 'q58208_%'
   OR StringId LIKE 'q59928_%'
   OR StringId IN ('q58209_cole', 'q59927_throg');

SELECT entry, name, AIName, ScriptName
FROM creature_template
WHERE entry IN (156280, 166573, 166824, 166827,
                160664, 166583, 157051, 166814, 156626, 166782);

SELECT * FROM spell_script_names
WHERE spell_id IN (290901, 303065, 325108, 305445, 305464, 325136);

SELECT * FROM conversation_template
WHERE Id IN (12798, 12818, 14422, 14423, 14424);
```

Source actors may be hidden by phases and still be deliberately selected through an ignore-phase lookup. Personal clones can use a different AI branch from the public source creature. Also, `AIName = SmartAI` does not guarantee SmartAI runs: a C++ `ScriptName` returning an AI takes precedence in the creature AI selector.

### Ship movement paths

```sql
SELECT PathId, COUNT(*) AS nodes
FROM waypoint_path_node
WHERE PathId IN (
  10501450, 10501451, 10501900, 10501901,
  10501460, 10501870, 10505890, 10505891,
  10501910, 10501911, 10501461, 10501871,
  10501770, 10501800, 10501790, 10501780,
  10502010, 10501990, 10501980, 10502000,
  10501510, 10502020
)
GROUP BY PathId ORDER BY PathId;
```

All 22 paths had nodes in the audit. Several valid paths contain only one node. Node existence alone does not validate orientation, motion on a moving transport, or collision.

### Hotfix spell effects: understand an empty result

```sql
SELECT SpellID, EffectIndex, Effect, EffectTriggerSpell,
       EffectMiscValue1, EffectMiscValue2, TargetNodeGraph, VerifiedBuild
FROM hotfixes.spell_effect
WHERE SpellID IN (295600, 305425, 325131,
                  305446, 325133, 305464, 325136)
ORDER BY SpellID, EffectIndex;
```

This returned no rows. It checks overrides only; it does not inspect the baseline `SpellEffect` DB2 store. To close the transition audit, inspect the actual loaded spell effects for the matching client build and follow any triggered spells/target graphs. Verify movie IDs `895`/`931`, transport removal and beach destination, and scenes `2334`/`2487`. A missing `spell_target_position` row or `spell_script_names` row alone does not prove a teleport spell is broken.

## In-game acceptance tests

Use newly created test characters for the normal path. GM quest-completion commands can bypass objective, scene, and status transitions and should not substitute for this test.

1. **Alliance normal run:** select an NPE-supported race/class and Exile's Reach. Confirm attachment to transport 29 on map 2175, intro scene, tutorial continuation, Jaina's quest, dummy credit, personal leader movement, sparring credit, storm actors, turn-in, crash movie, beach knockdown, personal greeting, and availability of the next quest.
2. **Horde normal run:** repeat with transport 30, Thrall, quests 59926/59927/59928, movie 931, and Horde beach leader 166782.
3. **Skip behavior:** skip each faction's intro. Confirm tutorial and quests remain available. Separately attempt to skip/cancel the movie and beach scene; record whether the movie acknowledgement and beach completion/cancel callbacks occur and whether the player can progress.
4. **Disconnect recovery:** disconnect during the intro, after the first quest reward, during sparring, after Brace for Impact becomes complete, during the movie, and during the beach scene. Reconnect and check location, transport attachment, quest status, phase, stuns, and next-step availability.
5. **Abandon and retry:** abandon and retake Stand Your Ground and Brace for Impact at supported stages. Check that personal actors do not duplicate and combat/phase state is restored.
6. **Two-player isolation:** run two same-faction characters together with different progression speeds. Each should see and interact with their own personal actors without receiving the other's scripted credit.
7. **Hunter variation:** test representative pet variants. Check pet actor selection and ship pathing without affecting the player's persistent pet state.
8. **Full-zone completion:** continue both factions through all island quests, class-specific tutorials, vehicles, Darkmaul Citadel, zone departure, and capital handoff. Record blockers separately from optional missing presentation.

For each failure record character race/class/faction, client build, server revision, quest status (`NONE`, `INCOMPLETE`, `COMPLETE`, `REWARDED`), current map and transport, last scene/movie, nearby actor IDs/StringIds, and relevant startup/runtime logs. Those observations identify which boundary failed.

## Troubleshooting by symptom

| Symptom | First checks |
| --- | --- |
| Character starts at the racial starting zone | NPE selection and valid NPE creation row for that race/class; loader rejection logs |
| Character is off-ship or falling | Runtime transport 29/30 availability, correct map, transport-relative offsets, client transport data |
| Intro does not play | Cinematic state, NPE creation mode, intro scene template and compatible package |
| No tutorial after intro | Complete/cancel scene callback, spell 295600 effects and conversation data |
| No Jaina/Thrall quest | Correct stage's template, questgiver flag, starter relations, previous quest and phases |
| Leader does not move after Warming Up | Quest must be rewarded; both lower/upper StringId sources must be within the script's ranges |
| Sparring never completes | Summon/selection effects, personal owner, objective credit 155607, quest status and lethal-hit handling |
| Missing storm crew | Direct transport pointer, exact StringIds, search range, personal clone AI and paths |
| No crash movie | Brace turn-in/reward spell, loaded movie effect and valid Movie record |
| Movie ends but player stays on ship | Stored movie ID and acknowledgement, OnMovieComplete registration, spells 305446/325133 and downstream effects |
| Player reaches beach without greeting | Scene completed versus cancelled, arrival spell effect 0, static leader within 50 yards |
| Player remains stunned | Scene trigger/removal sequence for 305445 and follow-up 344889; inspect aura state and loaded effects |

These guides document findings; they do not apply speculative fixes. Reproduce a failure and trace its boundary before altering spells, phases, personal actors, or character state.
