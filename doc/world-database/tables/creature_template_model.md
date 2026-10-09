# creature_template_model

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Weighted display-model choices for creature templates.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Template extension. |
| 2 | `Idx` | `int unsigned` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `CreatureDisplayID` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Logical reference to [creature_model_info.DisplayID](creature_model_info.md). Display model metadata. |
| 4 | `DisplayScale` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Probability` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureID`, `Idx` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_model](creature_template_model.md).`CreatureDisplayID` → [creature_model_info](creature_model_info.md).`DisplayID`: Display model metadata.
- [creature_template_model](creature_template_model.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:612](../../../src/server/game/Globals/ObjectMgr.cpp#L612)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `CreatureID` | `uint32 creatureId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L625) |
| `CreatureDisplayID` | `uint32 creatureDisplayId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L626) |
| `DisplayScale` | `float displayScale = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L627) |
| `Probability` | `float probability = fields[3].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L628) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template_model` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template_model) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
