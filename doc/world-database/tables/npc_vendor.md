# npc_vendor

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

NPC vendor stock, prices, conditions, and item/currency offerings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Npc System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Creature template entry offering this stock. |
| 2 | `slot` | `smallint` | NO | `0` | MUL | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `item` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `maxcount` | `int unsigned` | NO | `0` | — | — | Stock limit; zero conventionally indicates unlimited stock. |
| 5 | `incrtime` | `int unsigned` | NO | `0` | — | — | Limited-stock replenishment time; inspect vendor stock code for timing. |
| 6 | `ExtendedCost` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `type` | `tinyint unsigned` | NO | `1` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `BonusListIDs` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `PlayerConditionID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `IgnoreFiltering` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry`, `item`, `ExtendedCost`, `type` | BTREE |
| `slot` | No | `slot` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [npc_vendor](npc_vendor.md).`entry` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9415](../../../src/server/game/Globals/ObjectMgr.cpp#L9415)
- [src/server/game/Globals/ObjectMgr.cpp:9470](../../../src/server/game/Globals/ObjectMgr.cpp#L9470)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:37](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L37)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:38](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L38)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:39](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L39)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry        = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9483) |
| `item` | `int32 item_id      = fields[1].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9484) |
| `maxcount` | `vItem.maxcount          = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9493) |
| `incrtime` | `vItem.incrtime          = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9494) |
| `ExtendedCost` | `vItem.ExtendedCost      = fields[4].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9495) |
| `type` | `vItem.Type              = fields[5].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9496) |
| `PlayerConditionID` | `vItem.PlayerConditionId = fields[7].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9497) |
| `IgnoreFiltering` | `vItem.IgnoreFiltering   = fields[8].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9498) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `npc_vendor` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/npc_vendor) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
