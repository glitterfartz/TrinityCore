# areatrigger_create_properties_polygon_vertex

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ordered polygon vertices for an area-trigger creation property.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `AreaTriggerCreatePropertiesId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 2 | `IsCustom` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Idx` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `VerticeX` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `VerticeY` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `VerticeTargetX` | `float` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `VerticeTargetY` | `float` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `AreaTriggerCreatePropertiesId`, `IsCustom`, `Idx` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/AreaTriggerDataStore.cpp:113](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L113)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `IsCustom` | `AreaTriggerCreatePropertiesId createPropertiesId = { verticeFields[0].GetUInt32(), verticeFields[1].GetBool() }` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L118) |
| `VerticeY` | `verticesByCreateProperties[createPropertiesId].emplace_back(verticeFields[3].GetFloat(), verticeFields[4].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L120) |
| `VerticeTargetY` | `verticesTargetByCreateProperties[createPropertiesId].emplace_back(verticeFields[5].GetFloat(), verticeFields[6].GetFloat())` | [loader](../../../src/server/game/Globals/AreaTriggerDataStore.cpp#L123) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `areatrigger_create_properties_polygon_vertex` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/areatrigger_create_properties_polygon_vertex) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
