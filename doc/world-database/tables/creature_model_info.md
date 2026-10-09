# creature_model_info

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Display-model collision dimensions and gender/model relationships.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature System (Model related info)

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `DisplayID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `BoundingRadius` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `CombatReach` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `DisplayID_Other_Gender` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `DisplayID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_model](creature_template_model.md).`CreatureDisplayID` → [creature_model_info](creature_model_info.md).`DisplayID`: Display model metadata.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1691](../../../src/server/game/Globals/ObjectMgr.cpp#L1691)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `DisplayID` | `uint32 displayId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1709) |
| `BoundingRadius` | `modelInfo.bounding_radius        = fields[1].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1720) |
| `CombatReach` | `modelInfo.combat_reach           = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1721) |
| `DisplayID_Other_Gender` | `modelInfo.displayId_other_gender = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1722) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_model_info` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_model_info) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
