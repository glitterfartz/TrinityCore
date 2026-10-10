# Quest authoring hub

[World database documentation](../README.md) · [Quest table reference](../tables/quest_template.md)

Use this guide to build a quest that a player can accept, complete, and turn in. Start with the basic example, then use the sections below to change its objectives, rewards, availability, or reset behavior.

The examples target **TrinityCore master, revision 914a6f655c97 / TDB 1210.26091**. Other branches use different columns and flags. The SQL here is for you to review and run in a development database; writing this guide did not change the connected database.

## Find what you need

- [Understand the pieces](#understand-the-pieces)
- [Build a simple kill quest](#build-a-simple-kill-quest)
- [Change the objectives](#change-the-objectives)
- [Choose rewards](#choose-rewards)
- [Make it repeatable, daily, weekly, or monthly](#make-it-repeatable-daily-weekly-or-monthly)
- [Build a quest chain or branching choice](#build-a-quest-chain-or-branching-choice)
- [Control who can accept the quest](#control-who-can-accept-the-quest)
- [Add a timer](#add-a-timer)
- [Improve dialogue, maps, and presentation](#improve-dialogue-maps-and-presentation)
- [Add scripted behavior](#add-scripted-behavior)
- [Test and troubleshoot](#test-and-troubleshoot)
- [Remove the example](#remove-the-example)

## Understand the pieces

Think of a quest as a definition connected to several supporting records.

| Piece | What it does | Main table |
| --- | --- | --- |
| Quest definition | Gives the quest its ID, title, description, flags, and rewards | [quest_template](../tables/quest_template.md) |
| Objectives | Says what the player must do | [quest_objectives](../tables/quest_objectives.md) |
| Quest giver | Connects an NPC type to a quest it offers | [creature_queststarter](../tables/creature_queststarter.md) |
| Turn-in NPC | Connects an NPC type to a quest it accepts for completion | [creature_questender](../tables/creature_questender.md) |
| Extra rules | Adds prerequisites, class/skill restrictions, repetition, and scripts | [quest_template_addon](../tables/quest_template_addon.md) |
| Dialogue | Supplies progress and reward conversation text | [quest_request_items](../tables/quest_request_items.md), [quest_offer_reward](../tables/quest_offer_reward.md) |

The **world database** stores these shared definitions. The server loads them into memory and uses them to answer client requests and check progress. Each character's accepted quests, objective progress, and completion history are stored separately in the **characters database**.

Changing a world row therefore changes the definition. It does not clear a character's completion history, and it does not necessarily update an already running server's cached definition.

A few identifiers matter throughout this guide:

- **Quest ID:** identifies the quest in every supporting quest table.
- **Objective ID:** identifies one objective. It must be unique across the objective table, including objectives belonging to other quests.
- **Creature entry:** identifies an NPC or creature type in creature_template.
- **Spawn GUID:** identifies one placement of that creature type in creature.

Quest-giver and ordinary kill-objective relationships use **creature entries**. If five guards share one template, attaching a quest to that template can make all five offer it. See [creatures](creatures.md) if you need a distinct NPC type or a new placement.

## Build a simple kill quest

Our example is **Keep the Road Clear**:

> A local quest giver asks the player to defeat three creatures of a chosen type, then return for an experience reward.

Use an existing quest-giving NPC and an existing killable creature for the first version. This lets you learn the quest system without also creating NPCs, models, spawns, or combat behavior.

### 1. Choose the NPC, target, and level context

In a SQL client connected to **world**, this query finds existing quest givers and some quests they offer:

```sql
SELECT DISTINCT
    t.entry AS GiverEntry, t.name AS GiverName, c.map,
    q.ID AS ReferenceQuest, q.LogTitle, q.ContentTuningID
FROM creature_template AS t
JOIN creature AS c ON c.id = t.entry
JOIN creature_queststarter AS s ON s.id = t.entry
JOIN quest_template AS q ON q.ID = s.quest
WHERE (t.npcflag & 0x00000002) <> 0
  AND q.QuestType = 2
  AND q.ContentTuningID <> 0
  AND (q.Flags & (0x00000400 | 0x00080000)) = 0
  AND q.LogTitle NOT LIKE '[DEPRECATED]%'
LIMIT 20;
```

Choose a giver you can reach with your test character. Select a **working, ordinary quest for the intended player level and race** as the reference quest. The example borrows its level/scaling context and experience-reward settings, rather than inventing client data IDs.

ContentTuningID points to a client/hotfix record that the server uses for level requirements and scaling. It is not a quest ID. In current master, there is no MinLevel column in quest_template to copy from an older tutorial.

For the target, choose a nearby creature you have confirmed is attackable and awards normal kill credit. Record its creature_template.entry. A friendly NPC, training dummy, or scripted encounter creature may behave differently.

### 2. Set the example's identifiers

Run these assignments in the same SQL connection as the following examples. **Replace every zero** with the values you selected.

```sql
SET @quest_id = 900000;
SET @objective_id = 9000001;
SET @giver_entry = 0;       -- existing quest-giving creature entry
SET @target_entry = 0;      -- existing killable creature entry
SET @reference_quest = 0;   -- working quest with suitable tuning and race eligibility
```

The two large IDs are example candidates, not a reserved TrinityCore range. Use your project's allocation convention and check for collisions first.

Inspect the selected records:

```sql
SELECT ID, LogTitle, ContentTuningID, AllowableRaces,
       RewardXPDifficulty, RewardXPMultiplier
FROM quest_template WHERE ID = @reference_quest;

SELECT entry, name, npcflag
FROM creature_template WHERE entry = @giver_entry;

SELECT entry, name, KillCredit1, KillCredit2
FROM creature_template WHERE entry = @target_entry;
```

Each query should return the expected record. Confirm the giver has the quest-giver flag, **0x00000002**, and that the reference quest permits your test character's race. KillCredit1/KillCredit2 can provide credit for other creature entries; for this first example, use a target whose ordinary kill credit you understand.

Check that the new identities have no existing data:

```sql
SELECT
    (SELECT COUNT(*) FROM quest_template
     WHERE ID = @quest_id) AS QuestRows,
    (SELECT COUNT(*) FROM quest_template_addon
     WHERE ID = @quest_id) AS AddonRows,
    (SELECT COUNT(*) FROM quest_objectives
     WHERE ID = @objective_id OR QuestID = @quest_id) AS ObjectiveRows,
    (SELECT COUNT(*) FROM quest_request_items
     WHERE ID = @quest_id) AS ProgressTextRows,
    (SELECT COUNT(*) FROM quest_offer_reward
     WHERE ID = @quest_id) AS RewardTextRows,
    (SELECT COUNT(*) FROM creature_queststarter
     WHERE quest = @quest_id) AS StarterRows,
    (SELECT COUNT(*) FROM creature_questender
     WHERE quest = @quest_id) AS EnderRows,
    (SELECT COUNT(*) FROM gameobject_queststarter
     WHERE quest = @quest_id) AS ObjectStarterRows,
    (SELECT COUNT(*) FROM gameobject_questender
     WHERE quest = @quest_id) AS ObjectEnderRows;
```

All counts must be zero. This checks the identities used by the walkthrough; it is not a search of every possible custom script or extension table.

### 3. Create the definition and its supporting rows

The block below creates one normal, one-time quest. It copies only the reference quest's tuning, quest-log category, race mask, expansion, and experience settings. It does not copy that quest's objectives, scripts, prerequisites, or items.

Run the statements in order. If any statement fails, **stop and ROLLBACK**; do not continue to COMMIT. The seven tables used here are InnoDB in the documented installation.

```sql
START TRANSACTION;

INSERT INTO quest_template
    (ID, QuestType, ContentTuningID, QuestSortID, AllowableRaces,
     Expansion, RewardXPDifficulty, RewardXPMultiplier,
     RewardMoneyMultiplier, Flags,
     LogTitle, LogDescription, QuestDescription, QuestCompletionLog)
SELECT
    @quest_id, 2, ContentTuningID, QuestSortID, AllowableRaces,
    Expansion, RewardXPDifficulty, RewardXPMultiplier,
    0, 0,
    'Keep the Road Clear',
    'Defeat three road threats, then return to the quest giver.',
    'Travelers need this road to be safe. Defeat three of the nearby threats, then report back to me.',
    'Return to the quest giver.'
FROM quest_template
WHERE ID = @reference_quest;

INSERT INTO quest_template_addon (ID, SpecialFlags)
VALUES (@quest_id, 0);

INSERT INTO quest_objectives
    (ID, QuestID, Type, `Order`, StorageIndex, ObjectID,
     Amount, Flags, Flags2, Visible, Description)
VALUES
    (@objective_id, @quest_id, 0, 0, 0, @target_entry,
     3, 0, 0, 1, 'Road threats defeated');

INSERT INTO creature_queststarter (id, quest)
VALUES (@giver_entry, @quest_id);

INSERT INTO creature_questender (id, quest)
VALUES (@giver_entry, @quest_id);

INSERT INTO quest_request_items (ID, CompletionText)
VALUES (@quest_id, 'Have you made the road safe yet?');

INSERT INTO quest_offer_reward (ID, RewardText)
VALUES (@quest_id, 'Well done. Travelers can use the road again.');

SELECT ID, LogTitle FROM quest_template WHERE ID = @quest_id;
SELECT ID, QuestID, Type, ObjectID, Amount
FROM quest_objectives WHERE QuestID = @quest_id;

COMMIT;
```

The first INSERT must report **one inserted row**. The two inspection queries should show one quest and one objective. INSERT ... SELECT can succeed with zero inserted rows if the reference quest is missing; that is why the earlier record check matters.

Here is what the objective means:

| Field | Example | Meaning |
| --- | --- | --- |
| Type | 0 | Monster kill/credit objective |
| ObjectID | @target_entry | Creature entry whose credit advances the objective |
| Amount | 3 | Required number of credits |
| Order | 0 | First displayed objective |
| StorageIndex | 0 | First stored progress counter for this quest |
| Visible | 1 | Objective is enabled for visible presentation |

Order controls presentation, while StorageIndex controls progress storage. They are different fields. The first basic counter uses zero for both; do not give multiple stored objectives the same StorageIndex.

The two relation rows make the same NPC type both the giver and the turn-in target. You can use different entries for those roles.

### 4. Load and test the quest

Restart worldserver in your development environment so it loads the new definition and supporting records together. Check sql.sql startup messages for the quest ID and objective ID.

Use a fresh, eligible test character:

1. Speak to the chosen NPC and accept the quest through its normal interface.
2. Kill one chosen target. Progress should become 1/3.
3. Kill two more. The quest should become complete.
4. Return to the NPC and turn it in.
5. Confirm that the experience reward is appropriate for the character.
6. Confirm that the one-time quest is no longer offered after reward.

If you used a different kind of target, replace “Road threats” in the text with its actual name before publishing the content.

You now have the complete quest loop. Add one variation at a time and retest it.

## Change the objectives

Each row in quest_objectives adds a requirement. Ordinary required objectives must all be satisfied before turn-in.

| Desired requirement | Type | ObjectID | Amount |
| --- | --- | --- | --- |
| Kill a creature / receive creature credit | 0 | Creature entry | Required credits |
| Collect an item | 1 | Item ID | Required items |
| Interact with a gameobject | 2 | Gameobject template entry | Required interaction credits |
| Talk to an NPC | 3 | Creature entry | Required talk credits |
| Turn in currency | 4 | Currency ID | Required currency |
| Learn a spell | 5 | Spell ID | Required learned-spell condition |
| Reach a minimum reputation | 6 | Faction ID | Required reputation value |
| Have currency without consuming it | 16 | Currency ID | Required owned currency |
| Obtain currency after acceptance | 17 | Currency ID | Required gained currency |

These are common starting points. See [QuestObjectiveType](../reference/quest-enums.md#questobjectivetype) for the full list. The type selects how the server interprets the operand and checks progress; valid IDs alone do not guarantee an interaction awards credit.

### Collect items

To change the example into a collection quest, first select an existing item and set @item_id:

```sql
-- Set @item_id to an existing item ID first.
UPDATE quest_objectives
SET Type = 1, ObjectID = @item_id, Amount = 5,
    Description = 'Supplies collected'
WHERE ID = @objective_id AND QuestID = @quest_id;
```

Update the quest text to match. If the item should drop from creatures, configure the target's actual loot definition as described in [loot](loot.md). Adding an item objective does not automatically add the item to a drop table.

Check whether the item is consumed at turn-in and whether quest-required drops are available only while needed. Item IDs on master are supplied through client/hotfix item data; there is no world.item_template table in this schema.

### Add a second objective

Add another row with a new, globally unused objective ID. For two simple stored kill counters, use Order = 1 and StorageIndex = 1 for the second row. Keep QuestID equal to the same quest ID.

Changing Order alone does not force players to complete objectives in sequence. Sequenced behavior uses objective flags and dependencies. Some objective types use inventory or other state instead of ordinary counters, so their StorageIndex conventions differ.

### Optional objectives and progress bars

Objective Flags includes **0x0004** for an optional objective and **0x0002** for sequenced presentation. Hidden objectives and objectives contributing to a progress bar have additional flags.

A progress-bar quest uses a Type = 15 objective plus contributing objectives flagged **0x0040** and configured with ProgressBarWeight. The current core permits one progress-bar objective per quest. This is more than changing the displayed counter to a percentage: review the [objective flags](../reference/quest-enums.md#questobjectiveflags), define the contributors, and test the completion threshold.

## Choose rewards

Rewards belong mostly to quest_template. Set both the identifier and its corresponding quantity.

| Reward | Fields or table | What to remember |
| --- | --- | --- |
| Fixed item | RewardItem1–4 and RewardAmount1–4 | Every configured item is awarded |
| Player-selected item | RewardChoiceItemID1–6 and RewardChoiceItemQuantity1–6 | Player chooses from the available options |
| Experience | RewardXPDifficulty and RewardXPMultiplier | Difficulty selects a reward-table entry; it is not a raw XP amount |
| Money | RewardMoneyDifficulty and RewardMoneyMultiplier | Uses the core's reward calculation; these are not raw copper |
| Bonus money | RewardBonusMoney | Used by the money-reward calculation; do not treat it as a universal fixed-payment field |
| Currency | RewardCurrencyID1–4 and RewardCurrencyQty1–4 | Currency IDs are external client/hotfix records |
| Reputation | RewardFactionID1–5 and associated value/override/cap fields | Distinguish reward-table selectors from direct reputation overrides |
| Reward spell | RewardSpell and related spell reward configuration | Verify the actual grant/cast behavior |
| Displayed spell reward | quest_reward_display_spell | Presentation/type handling is separate from simply learning a spell |
| Mail | quest_template_addon mail fields, optionally quest_mail_sender | Mail template IDs are not item IDs |
| Housing or treasure rewards | quest_reward_house_decor, quest_reward_house_room, quest_treasure_pickers | Require matching modern client records |

For example, award two of an existing item:

```sql
-- Set @reward_item_id to an existing item ID first.
UPDATE quest_template
SET RewardItem1 = @reward_item_id, RewardAmount1 = 2
WHERE ID = @quest_id;
```

For a choice reward, configure the corresponding display information and typed choice data where required by the item/reward kind. Start with a working reward of the same kind and consult [quest_reward_choice_items](../tables/quest_reward_choice_items.md).

StartItem gives the player an item when accepting the quest. Its quantity is ProvidedItemCount in quest_template_addon. This is separate from a collection objective and from a completion reward.

Repeatable reward testing matters: a reward that is suitable once may be excessive when players can earn it continuously.

## Make it repeatable, daily, weekly, or monthly

A repeatable quest can be accepted again. A daily or weekly quest also has a completion lockout until the appropriate reset.

Two flag fields are involved:

- **quest_template.Flags** contains client-facing quest flags, including daily and weekly.
- **quest_template_addon.SpecialFlags** contains server-side flags, including repeatable and monthly.

Use bitwise operations to preserve unrelated settings.

| Behavior | quest_template.Flags | quest_template_addon.SpecialFlags |
| --- | --- | --- |
| One-time | Neither daily nor weekly | No repeatable/monthly bits |
| Immediately repeatable | Neither daily nor weekly | Repeatable: 0x01 |
| Daily | Daily: 0x00001000 | Repeatable: 0x01 |
| Weekly | Weekly: 0x00008000 | Repeatable: 0x01 |
| Monthly | Neither daily nor weekly | Repeatable + monthly: 0x01 + 0x10 |

The loader adds the repeatable bit in memory for daily, weekly, and monthly quests if it is missing. Store it explicitly so the database expresses your intention.

### Make the example immediately repeatable

```sql
UPDATE quest_template
SET Flags = Flags & ~0x00009000
WHERE ID = @quest_id;

UPDATE quest_template_addon
SET SpecialFlags = (SpecialFlags & ~0x10) | 0x01
WHERE ID = @quest_id;
```

This clears daily/weekly and monthly reset behavior while enabling repeatability. It does not clear unrelated flags.

### Make it daily

```sql
UPDATE quest_template
SET Flags = (Flags & ~0x00008000) | 0x00001000
WHERE ID = @quest_id;

UPDATE quest_template_addon
SET SpecialFlags = (SpecialFlags & ~0x10) | 0x01
WHERE ID = @quest_id;
```

A daily resets on the server's daily schedule, not 24 hours after the individual player's turn-in. Do not set the daily and weekly bits together.

### Make it weekly or monthly

For weekly, clear daily and set weekly:

```sql
UPDATE quest_template
SET Flags = (Flags & ~0x00001000) | 0x00008000
WHERE ID = @quest_id;

UPDATE quest_template_addon
SET SpecialFlags = (SpecialFlags & ~0x10) | 0x01
WHERE ID = @quest_id;
```

For monthly, clear daily/weekly and enable the monthly server flag:

```sql
UPDATE quest_template
SET Flags = Flags & ~0x00009000
WHERE ID = @quest_id;

UPDATE quest_template_addon
SET SpecialFlags = SpecialFlags | 0x11
WHERE ID = @quest_id;
```

These examples assume the addon row exists, as it does in the walkthrough. An UPDATE affecting zero rows does not create one.

ResetByScheduler is a separate field; it is not the switch used by these daily/weekly examples. Event-seasonal resets and quest-pool rotation are also separate systems.

After changing repetition rules, reload the definition through a restart and test acceptance before reward, immediately after reward, and after the relevant reset. Repeatedly removing a quest with a GM command is not proof that its scheduled lockout works.

## Build a quest chain or branching choice

### Require quest A before quest B

On **B**, set quest_template_addon.PrevQuestID to A's positive quest ID. This means the player must have **rewarded** A, not merely finished its objectives.

```sql
-- Both quests and B's addon row must already exist.
SET @quest_a = 900000;
SET @quest_b = 900001;

UPDATE quest_template_addon
SET PrevQuestID = @quest_a
WHERE ID = @quest_b;
```

If B's addon row is absent, insert one with ID and PrevQuestID instead. Check first so you do not overwrite an existing configuration.

For a smooth handoff, set A's RewardNextQuest to B:

```sql
UPDATE quest_template
SET RewardNextQuest = @quest_b
WHERE ID = @quest_a;
```

RewardNextQuest helps present the next quest after turn-in. B still needs a normal offer relationship, appropriate eligibility, and its own objectives and turn-in path.

NextQuestID in the addon table also creates a dependency on the destination quest in the loader. Choose a consistent way to express your chain rather than adding links without understanding their effects.

A **negative PrevQuestID** means a different rule: the referenced quest must be active and incomplete. Do not use a negative number to express “must not have completed.”

### Offer a choice between quests

A shared **positive ExclusiveGroup** makes quests alternatives: another active or completed/rewarded quest in the group can block acceptance. Repeatable quests have additional completion-state handling.

A negative ExclusiveGroup participates in “complete all prerequisites in this group” behavior. It is not the usual choice-between-two-quests setting. Use it only after reviewing the prerequisite evaluation.

BreadcrumbForQuestId defines a lead-in quest pointing toward another quest. A breadcrumb is not equivalent to a mandatory prerequisite.

For any chain or branch, test with characters at each stage: neither quest accepted, A active, A complete but unrewarded, A rewarded, and a competing branch selected.

## Control who can accept the quest

| Restriction | Where to configure it |
| --- | --- |
| Minimum level / level scaling | quest_template.ContentTuningID and its client/hotfix tuning record |
| Maximum level | quest_template_addon.MaxLevel; zero means no additional maximum |
| Race | quest_template.AllowableRaces |
| Class | quest_template_addon.AllowableClasses |
| Skill and rank | RequiredSkillID and RequiredSkillPoints in the addon |
| Reputation range | RequiredMinRepFaction/Value and RequiredMaxRepFaction/Value in the addon |
| Previous quest | PrevQuestID and chain relationships |
| More complex rules | Appropriate world conditions source |
| Event-only offer | game_event_creature_quest or game_event_gameobject_quest |
| Rotating availability | quest_pool_template and quest_pool_members |

Race and class fields are **bitmasks**, not plain race/class IDs. Keep modern race masks as 64-bit integers; a zero race mask does not mean “all races.” The basic example copies a known working race mask directly in SQL.

Conditions can add requirements, but their source fields depend on what is being gated. Follow [conditions](conditions.md) for source types and Boolean grouping. A condition attached to a gossip option is not automatically a quest-acceptance rule.

Quest pools select a rotating subset. They do not make every member an ordinary daily by themselves. Configure and test the quest's own repetition rules alongside the pool.

## Add a timer

TimeAllowed is measured in **seconds**. Set it to 300 for a five-minute quest:

```sql
UPDATE quest_template
SET TimeAllowed = 300
WHERE ID = @quest_id;
```

Zero removes the time limit. The server starts the quest timer on acceptance and converts it to its internal timer representation.

Test completion before expiry, expiry while active, abandonment, and reacceptance. Timed-quest acceptance also checks whether the player already has another timed quest.

## Improve dialogue, maps, and presentation

Keep these stages distinct:

| Player sees | Where to write it |
| --- | --- |
| Quest title in the log | quest_template.LogTitle |
| Short objective summary | quest_template.LogDescription |
| Full offer description | quest_template.QuestDescription |
| Text after objective completion in the log | quest_template.QuestCompletionLog |
| Objective line | quest_objectives.Description |
| Progress / request conversation | quest_request_items.CompletionText |
| Reward conversation | quest_offer_reward.RewardText |

quest_details, quest_request_items, and quest_offer_reward can also configure dialogue emotes and delays. Conditional text tables provide alternate text using their own condition-related fields; consult their schemas rather than copying the world conditions key layout.

A usable quest does not need custom map overlays for its first test. To add them later, use quest_poi and quest_poi_points. Overlay rows belong to specific quest/objective blobs, and their point identities and ordering must match. Adding descriptive text does not create map markers.

For translations, use quest_template_locale and the corresponding dialogue/objective locale tables. Objective translations use the **objective ID**. See [localization](localization.md) for parent keys, locales, and fallback behavior.

For a gameobject quest giver, use gameobject_queststarter/gameobject_questender with a suitable quest-giving object template. Attaching a relation to an arbitrary decorative object does not give it the required interaction behavior.

## Add scripted behavior

Simple kills, item collection, and supported interactions can work through normal quest/objective handling. Use [SmartAI](smartai.md) or a compiled C++ script when you need custom sequences such as an escort, waves of enemies, dialogue scenes, or credit awarded after a special action.

There are two jobs to keep separate:

1. The quest objective defines the required progress.
2. The interaction or script produces the credit that advances it.

For example, making an NPC perform an emote does not automatically satisfy a talk objective. The relevant interaction must award the correct credit.

SmartAI has quest-acceptance/reward events and actions for credit and encounters. Check the current enum operand layout and whether the intended player is available as an invoker/target.

ScriptName binds a registered, compiled script. Typing a new name into the database does not create that script. Attach behavior to the quest, NPC, or object according to the script's implementation.

## Test and troubleshoot

Test through the normal player interaction before using shortcuts. A quest added by a GM command can help isolate a problem, but it does not prove the giver or eligibility checks work.

Useful development commands include:

```text
.quest add 900000
.quest complete 900000
.quest remove 900000
```

These commands require the appropriate permissions and operate on the selected player or yourself. Completing through a command bypasses ordinary objective work. Use a fresh character when checking one-time completion history or reset eligibility.

### Test the full lifecycle

| Test | Expected result |
| --- | --- |
| Eligible character visits giver | Quest is offered |
| Ineligible character visits giver | Quest is unavailable as intended |
| Player accepts | Correct text, objectives, and starting items appear |
| Player makes partial progress | Only the intended objective advances |
| Player finishes objectives | Quest becomes complete |
| Player visits the intended turn-in target | Reward dialogue and choices are correct |
| Player accepts reward | Correct rewards arrive and required items/currency behave correctly |
| Player abandons and accepts again | Progress and provided-item behavior are correct |
| Player logs out with the quest active | Intended progress survives |
| Player tries again after reward | One-time/repeat/reset behavior matches the design |

Check both low and high eligible levels if the quest scales. Test actual kills or interactions after changing objective types.

### Find the failing stage

| Symptom | Check first |
| --- | --- |
| Quest is unknown to the server | Correct world database, successful INSERT, server restart, startup loader errors |
| NPC does not offer it | Starter relation uses the template entry, quest-giver flag, race/class/level rules, prerequisites, completion history, conditions, disables, events/pools |
| It accepts but kills do not count | Objective Type/ObjectID, target creature entry and kill-credit mapping, unique progress storage, group/credit behavior |
| Items do not appear | Correct loot source and definition, item ID, quest-required eligibility; an objective alone creates no drops |
| Objectives finish but turn-in fails | Ender relation, required inventory/currency, timer, other required objectives |
| Reward is wrong | Identifier/quantity pairs, reward-table selectors, scaling and repeat behavior |
| Daily stays unavailable | Server reset schedule and character completion state |
| Edits seem ignored | Cached definitions or client presentation; restart and use a fresh test character |

Keep the SQL that defines the quest in a reviewed migration, together with the chosen IDs and test notes. See [operations](operations.md) for the broader update workflow.

## Remove the example

The following removes **only the seven kinds of world rows created by the basic walkthrough**. Confirm @quest_id is still the custom quest ID and remove it from your test characters before removing its definition.

```sql
START TRANSACTION;

DELETE FROM creature_queststarter WHERE quest = @quest_id;
DELETE FROM creature_questender WHERE quest = @quest_id;
DELETE FROM quest_objectives WHERE QuestID = @quest_id;
DELETE FROM quest_request_items WHERE ID = @quest_id;
DELETE FROM quest_offer_reward WHERE ID = @quest_id;
DELETE FROM quest_template_addon WHERE ID = @quest_id;
DELETE FROM quest_template WHERE ID = @quest_id;

COMMIT;
```

If you added translations, POIs, extra reward tables, conditions, event/pool relationships, or scripted references, include those in your rollback too. This block does not erase character completion history and does not remove NPCs or target creatures.

## Source checks for this guide

The seven SELECT examples passed read-only EXPLAIN against the connected database, and the discovery query returned candidate quest givers. Table and column identifiers in the 27 INSERT/UPDATE/DELETE examples were checked against the captured schema. Flags, prerequisites, and timer units were checked against this checkout's implementation. Database writes and in-game quest behavior were not executed as part of writing the guide.

- [QuestDef.h](../../../src/server/game/Quests/QuestDef.h): objective types and flags, quest flags, and repetition helpers.
- [QuestDef.cpp](../../../src/server/game/Quests/QuestDef.cpp): quest fields and supporting-table loaders.
- [ObjectMgr.cpp](../../../src/server/game/Globals/ObjectMgr.cpp): quest load-time validation, repeatable normalization, and dependency construction.
- [Player.cpp](../../../src/server/game/Entities/Player/Player.cpp): eligibility, objective/completion handling, timers, and reset checks.
- [cs_quest.cpp](../../../src/server/scripts/Commands/cs_quest.cpp): quest development commands.
