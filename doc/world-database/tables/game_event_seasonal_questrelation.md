# game_event_seasonal_questrelation

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Associates seasonal quests with events for reset tracking.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Player System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `questId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: Quest Identifier |
| 2 | `eventEntry` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `idx_quest` | No | `questId` | BTREE |
| `PRIMARY` | Yes | `questId`, `eventEntry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_seasonal_questrelation](game_event_seasonal_questrelation.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:787](../../../src/server/game/Events/GameEventMgr.cpp#L787)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `questId` | `uint32 questId  = fields[0].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L798) |
| `eventEntry` | `uint32 eventEntry = fields[1].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L799) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_seasonal_questrelation` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_seasonal_questrelation) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
