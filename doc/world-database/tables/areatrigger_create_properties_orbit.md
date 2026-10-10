# areatrigger_create_properties_orbit

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Orbital motion configuration for an area-trigger creation property.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `AreaTriggerCreatePropertiesId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 2 | `IsCustom` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `ExtraTimeForBlending` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `CircleRadius` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `BlendFromRadius` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `InitialAngle` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `ZOffset` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `CounterClockwise` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `CanLoop` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `AreaTriggerCreatePropertiesId`, `IsCustom` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/AreaTriggerDataStore.cpp:351](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L351)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `IsCustom` | `AreaTriggerCreatePropertiesId createPropertiesId = { circularMovementInfoFields[0].GetUInt32(), circularMovementInfoFields[1].GetBool() }` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L356) |
| `ExtraTimeForBlending` | `orbit.ExtraTimeForBlending = circularMovementInfoFields[2].GetInt32()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L367) |
| `CircleRadius` | `VALIDATE_AND_SET_FLOAT(Radius,          circularMovementInfoFields[3].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L378) |
| `BlendFromRadius` | `VALIDATE_AND_SET_FLOAT(BlendFromRadius, circularMovementInfoFields[4].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L379) |
| `InitialAngle` | `VALIDATE_AND_SET_FLOAT(InitialAngle,    circularMovementInfoFields[5].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L380) |
| `ZOffset` | `VALIDATE_AND_SET_FLOAT(ZOffset,         circularMovementInfoFields[6].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L381) |
| `CounterClockwise` | `orbit.CounterClockwise = circularMovementInfoFields[7].GetBool()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L385) |
| `CanLoop` | `orbit.CanLoop          = circularMovementInfoFields[8].GetBool()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L386) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `areatrigger_create_properties_orbit` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/areatrigger_create_properties_orbit) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
