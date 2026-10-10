# areatrigger_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Defines an area trigger's shape and base behavior.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `IsCustom` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Flags` | `int unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 4 | `ActionSetId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ActionSetFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id`, `IsCustom` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/AreaTriggerDataStore.cpp:152](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L152)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `areaTriggerTemplate.Id.Id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L159) |
| `IsCustom` | `areaTriggerTemplate.Id.IsCustom = fields[1].GetBool()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L160) |
| `Flags` | `areaTriggerTemplate.Flags = AreaTriggerFlag(fields[2].GetUInt32())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L161) |
| `ActionSetId` | `areaTriggerTemplate.ActionSetId = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L162) |
| `ActionSetFlags` | `areaTriggerTemplate.ActionSetFlags = AreaTriggerActionSetFlag(fields[4].GetUInt32())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L163) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `areatrigger_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/areatrigger_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
