# quest_objectives

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed objective requirements and progress storage for quests.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Record identifier; consult the complete primary key and relationships before treating it as a template ID. |
| 2 | `QuestID` | `int unsigned` | NO | `0` | — | — | Logical reference to [quest_template.ID](quest_template.md). Parent quest. |
| 3 | `Type` | `tinyint unsigned` | NO | `0` | — | — | Quest objective type discriminator; selects ObjectID and Amount interpretation. |
| 4 | `Order` | `tinyint unsigned` | NO | `0` | — | — | Ordering value within the parent object. |
| 5 | `StorageIndex` | `tinyint` | NO | `0` | — | — | Quest objective progress storage index; signed values can carry special meanings. |
| 6 | `ObjectID` | `int` | NO | `0` | — | — | Typed objective operand; Type determines whether this is a creature, item, currency, spell, or another record. |
| 7 | `Amount` | `int` | NO | `0` | — | — | Required progress or quantity, interpreted by objective Type. |
| 8 | `ConditionalAmount` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `Flags` | `int unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 10 | `Flags2` | `int unsigned` | NO | `0` | — | — | Additional owning-subsystem flags. |
| 11 | `ProgressBarWeight` | `float` | NO | `0` | — | — | Contribution of this objective to quest progress-bar completion. |
| 12 | `ParentObjectiveID` | `int` | NO | `0` | — | — | Logical reference to [quest_objectives.ID](quest_objectives.md). Objective dependency. |
| 13 | `Visible` | `tinyint unsigned` | NO | `1` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 14 | `Description` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 15 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_objectives](quest_objectives.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.
- [quest_objectives](quest_objectives.md).`ParentObjectiveID` → [quest_objectives](quest_objectives.md).`ID`: Objective dependency.
- [quest_objectives_completion_effect](quest_objectives_completion_effect.md).`ObjectiveID` → [quest_objectives](quest_objectives.md).`ID`: Objective completion effect.
- [quest_objectives_locale](quest_objectives_locale.md).`ID` → [quest_objectives](quest_objectives.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:4684](../../../src/server/game/Globals/ObjectMgr.cpp#L4684)

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_objectives` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_objectives) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
