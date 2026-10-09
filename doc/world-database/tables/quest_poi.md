# quest_poi

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Quest objective map-overlay blob metadata.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `QuestID` | `int` | NO | `0` | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Parent quest. |
| 2 | `BlobIndex` | `int` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `Idx1` | `int` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `ObjectiveIndex` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `QuestObjectiveID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `QuestObjectID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `MapID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `UiMapID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `Priority` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `Flags` | `int` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 11 | `WorldEffectID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 12 | `PlayerConditionID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 13 | `NavigationPlayerConditionID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 14 | `SpawnTrackingID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 15 | `AlwaysAllowMergingBlobs` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 16 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `idx` | No | `QuestID`, `BlobIndex` | BTREE |
| `PRIMARY` | Yes | `QuestID`, `BlobIndex`, `Idx1` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_poi](quest_poi.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8341](../../../src/server/game/Globals/ObjectMgr.cpp#L8341)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_poi` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_poi) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
