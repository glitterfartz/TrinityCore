# game_event_npc_vendor

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Vendor offerings enabled during a world event.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `eventEntry` | `tinyint` | NO | NULL / absent; see conventions | — | — | Logical reference to [game_event.eventEntry](game_event.md). Event identity; signed event fields require sign-aware interpretation. |
| 2 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `slot` | `smallint` | NO | `0` | MUL | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `item` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `maxcount` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `incrtime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `ExtendedCost` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `type` | `tinyint unsigned` | NO | `1` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `BonusListIDs` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `PlayerConditionID` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 11 | `IgnoreFiltering` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid`, `item`, `ExtendedCost`, `type` | BTREE |
| `slot` | No | `slot` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [game_event_npc_vendor](game_event_npc_vendor.md).`eventEntry` → [game_event](game_event.md).`eventEntry`: Event identity; signed event fields require sign-aware interpretation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Events/GameEventMgr.cpp:828](../../../src/server/game/Events/GameEventMgr.cpp#L828)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `eventEntry` | `uint8 event_id  = fields[0].GetUInt8()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L839) |
| `guid` | `ObjectGuid::LowType guid = fields[1].GetUInt64()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L840) |
| `item` | `vItem.item              = fields[2].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L865) |
| `maxcount` | `vItem.maxcount          = fields[3].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L866) |
| `incrtime` | `vItem.incrtime          = fields[4].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L867) |
| `ExtendedCost` | `vItem.ExtendedCost      = fields[5].GetUInt32()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L868) |
| `type` | `vItem.Type              = fields[6].GetUInt8()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L869) |
| `IgnoreFiltering` | `vItem.IgnoreFiltering   = fields[9].GetBool()` | [loader](../../../src/server/game/Events/GameEventMgr.cpp#L871) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_event_npc_vendor` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_event_npc_vendor) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
