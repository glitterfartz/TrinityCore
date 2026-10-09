# skill_tiers

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Skill tier thresholds.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Value1` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `Value2` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `Value3` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `Value4` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `Value5` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `Value6` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `Value7` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `Value8` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `Value9` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 11 | `Value10` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 12 | `Value11` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 13 | `Value12` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 14 | `Value13` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 15 | `Value14` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 16 | `Value15` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 17 | `Value16` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8942](../../../src/server/game/Globals/ObjectMgr.cpp#L8942)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8954) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `skill_tiers` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/skill_tiers) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
