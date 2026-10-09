# vehicle_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server-specific vehicle configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `creatureId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `despawnDelayMs` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Pitch` | `float` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `CustomFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `creatureId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:3523](../../../src/server/game/Globals/ObjectMgr.cpp#L3523)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `creatureId` | `uint32 creatureId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3535) |
| `despawnDelayMs` | `vehicleTemplate.DespawnDelay = Milliseconds(fields[1].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3551) |
| `Pitch` | `vehicleTemplate.Pitch = fields[2].GetFloatOrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3552) |
| `CustomFlags` | `vehicleTemplate.CustomFlags = VehicleCustomFlags(fields[3].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3553) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `vehicle_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/vehicle_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
