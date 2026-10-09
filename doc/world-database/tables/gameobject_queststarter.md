# gameobject_queststarter

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Gameobject templates that offer quests.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [gameobject_template.entry](gameobject_template.md). Gameobject template identity. |
| 2 | `quest` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Quest offer/turn-in relationship. |
| 3 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id`, `quest` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gameobject_queststarter](gameobject_queststarter.md).`id` → [gameobject_template](gameobject_template.md).`entry`: Gameobject template identity.
- [gameobject_queststarter](gameobject_queststarter.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gameobject_queststarter` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gameobject_queststarter) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
