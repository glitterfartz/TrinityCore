# game_event

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Calendar and progression definitions for world events.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: Entry of the game event |
| 2 | `start_time` | `timestamp` | YES | NULL / absent; see conventions | — | — | Database comment: Absolute start date, the event will never start before |
| 3 | `end_time` | `timestamp` | YES | NULL / absent; see conventions | — | — | Database comment: Absolute end date, the event will never start after |
| 4 | `occurence` | `bigint unsigned` | NO | `5184000` | — | — | Database comment: Delay in minutes between occurences of the event |
| 5 | `length` | `bigint unsigned` | NO | `2592000` | — | — | Database comment: Length in minutes of the event |
| 6 | `holiday` | `int unsigned` | NO | `0` | — | — | Database comment: Client side holiday id |
| 7 | `holidayStage` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `WorldStateId` | `int` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `description` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Description text; its runtime role depends on the owning table. |
| 10 | `world_event` | `tinyint unsigned` | NO | `0` | — | — | Database comment: 0 if normal event, 1 if world event |
| 11 | `announce` | `tinyint unsigned` | YES | `2` | — | — | Database comment: 0 dont announce, 1 announce, 2 value from config |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `eventEntry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_prerequisite](game_event_prerequisite.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Dependent event.
- [game_event_prerequisite](game_event_prerequisite.md).`prerequisite_event` → [game_event](game_event.md).`eventEntry`: Prerequisite event.
- [game_event_quest_condition](game_event_quest_condition.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_arena_seasons](game_event_arena_seasons.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_gameobject](game_event_gameobject.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_model_equip](game_event_model_equip.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_condition](game_event_condition.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_creature](game_event_creature.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_npcflag](game_event_npcflag.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_gameobject_quest](game_event_gameobject_quest.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_prerequisite](game_event_prerequisite.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_pool](game_event_pool.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_npc_vendor](game_event_npc_vendor.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_creature_quest](game_event_creature_quest.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.
- [game_event_seasonal_questrelation](game_event_seasonal_questrelation.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:221](../../../src/server/game/Events/GameEventMgr.cpp#L221)
- [src/server/game/Events/GameEventMgr.cpp:957](../../../src/server/game/Events/GameEventMgr.cpp#L957)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
