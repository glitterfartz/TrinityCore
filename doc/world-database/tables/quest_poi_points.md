# quest_poi_points

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ordered coordinates composing quest POI blobs.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `QuestID` | `int` | NO | `0` | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Also join blob keys to quest_poi.; Logical reference to [quest_template.ID](quest_template.md). Parent quest. |
| 2 | `Idx1` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Idx2` | `int` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `X` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Y` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Z` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `QuestID`, `Idx1`, `Idx2` | BTREE |
| `questId_id` | No | `QuestID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_poi_points](quest_poi_points.md).`QuestID` → [quest_template](quest_template.md).`ID`: Also join blob keys to quest_poi.
- [quest_poi_points](quest_poi_points.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8349](../../../src/server/game/Globals/ObjectMgr.cpp#L8349)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `QuestID` | `int32 QuestID             = fields[0].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8359) |
| `Idx1` | `int32 Idx1                = fields[1].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8360) |
| `X` | `int32 x                   = fields[2].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8361) |
| `Y` | `int32 y                   = fields[3].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8362) |
| `Z` | `int32 z                   = fields[4].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8363) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_poi_points` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_poi_points) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
