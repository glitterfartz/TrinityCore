# game_event_gameobject

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Gameobject spawn participation in world events.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Logical reference to [gameobject.guid](gameobject.md). Event-controlled object spawn. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid`, `eventEntry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_gameobject](game_event_gameobject.md).`guid` → [gameobject](gameobject.md).`guid`: Event-controlled object spawn.
- [game_event_gameobject](game_event_gameobject.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:452](../../../src/server/game/Events/GameEventMgr.cpp#L452)
- [src/server/game/Globals/ObjectMgr.cpp:2485](../../../src/server/game/Globals/ObjectMgr.cpp#L2485)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:32](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L32)
- [src/server/scripts/Commands/cs_gobject.cpp:225](../../../src/server/scripts/Commands/cs_gobject.cpp#L225)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `eventEntry` | `int16 event_id = fields[1].GetInt8()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L464) |
| `guid` | `ObjectGuid::LowType guid = fields[0].GetUInt64()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L463) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_gameobject` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_gameobject) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
