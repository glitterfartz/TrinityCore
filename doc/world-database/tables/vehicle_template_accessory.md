# vehicle_template_accessory

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Template-level NPC passengers/accessories for vehicles.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `accessory_entry` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `seat_id` | `tinyint` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `minion` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `description` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Description text; its runtime role depends on the owning table. |
| 6 | `summontype` | `tinyint unsigned` | NO | `6` | — | — | Database comment: see enum TempSummonType |
| 7 | `summontimer` | `int unsigned` | NO | `30000` | — | — | Database comment: timer, only relevant for certain summontypes |
| 8 | `RideSpellID` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry`, `seat_id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:3463](../../../src/server/game/Globals/ObjectMgr.cpp#L3463)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry        = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3475) |
| `accessory_entry` | `uint32 accessory    = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3476) |
| `seat_id` | `int8   seatId       = fields[2].GetInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3477) |
| `minion` | `bool   isMinion     = fields[3].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3478) |
| `summontype` | `uint8  summonType   = fields[4].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3479) |
| `summontimer` | `uint32 summonTimer  = fields[5].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3480) |
| `RideSpellID` | `Optional<uint32> rideSpellId = fields[6].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3481) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `vehicle_template_accessory` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/vehicle_template_accessory) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
