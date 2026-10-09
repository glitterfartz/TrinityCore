# creature_questender

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Creature templates that accept a quest turn-in.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Creature template identity, not spawn GUID. |
| 2 | `quest` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Quest offer/turn-in relationship. |
| 3 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id`, `quest` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_questender](creature_questender.md).`id` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_questender](creature_questender.md).`quest` → [quest_template](quest_template.md).`ID`: Quest offer/turn-in relationship.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_questender` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_questender) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
