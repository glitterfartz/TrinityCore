# class_expansion_requirement

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Expansion eligibility for playable classes.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ClassID` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `RaceID` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `ActiveExpansionLevel` | `tinyint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `AccountExpansionLevel` | `tinyint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ClassID`, `RaceID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:10535](../../../src/server/game/Globals/ObjectMgr.cpp#L10535)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ClassID` | `uint8 classID = fields[0].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10547) |
| `RaceID` | `uint8 raceID = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10548) |
| `ActiveExpansionLevel` | `uint8 activeExpansionLevel = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10549) |
| `AccountExpansionLevel` | `uint8 accountExpansionLevel = fields[3].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10550) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `class_expansion_requirement` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/class_expansion_requirement) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
