# vehicle_seat_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Additional vehicle-seat behavior and attachment settings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SeatEntry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: VehicleSeatEntry.dbc identifier |
| 2 | `SeatOrientation` | `float` | YES | `0` | — | — | Database comment: Seat Orientation override value |
| 3 | `ExitParamX` | `float` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `ExitParamY` | `float` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ExitParamZ` | `float` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `ExitParamO` | `float` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `ExitParamValue` | `tinyint(1)` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SeatEntry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:3641](../../../src/server/game/Globals/ObjectMgr.cpp#L3641)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SeatEntry` | `uint32 seatID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3653) |
| `SeatOrientation` | `float orientation = fields[1].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3654) |
| `ExitParamX` | `float exitX = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3655) |
| `ExitParamY` | `float exitY = fields[3].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3656) |
| `ExitParamZ` | `float exitZ = fields[4].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3657) |
| `ExitParamO` | `float exitO = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3658) |
| `ExitParamValue` | `uint8 exitParam = fields[6].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3659) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `vehicle_seat_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/vehicle_seat_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
