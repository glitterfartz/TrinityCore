# quest_reward_house_room

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Housing room rewards for quests.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `QuestID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Parent quest. |
| 2 | `OrderIndex` | `int` | NO | NULL / absent; see conventions | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `HouseRoomID` | `int` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `QuestID`, `OrderIndex` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_reward_house_room](quest_reward_house_room.md).`QuestID` → [quest_template](quest_template.md).`ID`: Parent quest.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_reward_house_room` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_reward_house_room) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
