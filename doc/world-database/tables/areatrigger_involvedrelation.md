# areatrigger_involvedrelation

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Connects client area triggers to quest exploration/completion credit.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Trigger System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | `0` | PRI | — | Row identity within this table; use the complete primary key when selecting or editing. |
| 2 | `quest` | `int unsigned` | NO | `0` | — | — | Database comment: Quest Identifier |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:6442](../../../src/server/game/Globals/ObjectMgr.cpp#L6442)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `id` | `uint32 trigger_ID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6458) |
| `quest` | `uint32 quest_ID   = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6459) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `areatrigger_involvedrelation` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/areatrigger_involvedrelation) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
