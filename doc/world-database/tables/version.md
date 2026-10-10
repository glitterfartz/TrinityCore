# version

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Installed database release, core revision, and cache version.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Version Notes

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `core_version` | `varchar(250)` | NO | `''` | PRI | — | Database comment: Core revision dumped at startup. |
| 2 | `core_revision` | `varchar(120)` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `db_version` | `varchar(120)` | YES | NULL / absent; see conventions | — | — | Database comment: Version of world DB. |
| 4 | `cache_id` | `int` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `core_version` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/World/World.cpp:3349](../../../src/server/game/World/World.cpp#L3349)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `db_version` | `m_DBVersion = fields[0].GetString()` | [loader](../../../src/server/game/World/World.cpp#L3353) |
| `cache_id` | `m_int_configs[CONFIG_CLIENTCACHE_VERSION] = fields[1].GetUInt32()` | [loader](../../../src/server/game/World/World.cpp#L3355) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `version` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/version) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
