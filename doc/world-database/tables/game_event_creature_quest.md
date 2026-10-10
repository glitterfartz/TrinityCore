# game_event_creature_quest

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Creature quest availability during a world event.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint unsigned` | NO | NULL / absent; see conventions | — | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `id` | `int unsigned` | NO | `0` | PRI | — | Row identity within this table; use the complete primary key when selecting or editing. |
| 3 | `quest` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id`, `quest` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_creature_quest](game_event_creature_quest.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:556](../../../src/server/game/Events/GameEventMgr.cpp#L556)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `eventEntry` | `uint16 event_id = fields[2].GetUInt8()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L569) |
| `id` | `uint32 id       = fields[0].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L567) |
| `quest` | `uint32 quest    = fields[1].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L568) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_creature_quest` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_creature_quest) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
