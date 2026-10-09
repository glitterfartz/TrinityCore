# creature_template_sparring

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Sparring behavior and health limits for creature templates.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: MyISAM. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Template extension. |
| 2 | `NoNPCDamageBelowHealthPct` | `float` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Entry`, `NoNPCDamageBelowHealthPct` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_sparring](creature_template_sparring.md).`Entry` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:882](../../../src/server/game/Globals/ObjectMgr.cpp#L882)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L895) |
| `NoNPCDamageBelowHealthPct` | `float noNPCDamageBelowHealthPct = fields[1].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L896) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template_sparring` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template_sparring) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
