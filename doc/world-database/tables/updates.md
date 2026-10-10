# updates

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

History and checksums of SQL migrations applied by the database updater.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: List of all applied updates in this database.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `name` | `varchar(200)` | NO | NULL / absent; see conventions | PRI | — | Database comment: filename with extension of the update. |
| 2 | `hash` | `char(40)` | YES | `''` | — | — | Database comment: sha1 hash of the sql file. |
| 3 | `state` | `enum('RELEASED','ARCHIVED')` | NO | `RELEASED` | — | — | Database comment: defines if an update is released or archived. |
| 4 | `timestamp` | `timestamp` | NO | `CURRENT_TIMESTAMP` | — | DEFAULT_GENERATED | Database comment: timestamp when the query was applied. |
| 5 | `speed` | `int unsigned` | NO | `0` | — | — | Database comment: time the query takes to apply in ms. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `name` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `updates` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/updates) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
