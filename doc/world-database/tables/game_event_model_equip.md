# game_event_model_equip

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Event-specific creature model and equipment overrides.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint` | NO | NULL / absent; see conventions | — | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `modelid` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `equipment_id` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_model_equip](game_event_model_equip.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:501](../../../src/server/game/Events/GameEventMgr.cpp#L501)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:72](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L72)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_model_equip` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_model_equip) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
