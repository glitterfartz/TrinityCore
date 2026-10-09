# game_event_condition

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Progress targets used by world-event conditions.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `condition_id` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `req_num` | `float` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `max_world_state_field` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `done_world_state_field` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `description` | `varchar(25)` | NO | `''` | — | — | Description text; its runtime role depends on the owning table. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `eventEntry`, `condition_id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_condition](game_event_condition.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:669](../../../src/server/game/Events/GameEventMgr.cpp#L669)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `eventEntry` | `uint16 event_id  = fields[0].GetUInt8()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L680) |
| `condition_id` | `uint32 condition = fields[1].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L681) |
| `req_num` | `mGameEvent[event_id].conditions[condition].reqNum = fields[2].GetFloat()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L689) |
| `max_world_state_field` | `mGameEvent[event_id].conditions[condition].max_world_state = fields[3].GetUInt16()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L691) |
| `done_world_state_field` | `mGameEvent[event_id].conditions[condition].done_world_state = fields[4].GetUInt16()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L692) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_condition` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_condition) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
