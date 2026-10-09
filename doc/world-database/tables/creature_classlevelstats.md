# creature_classlevelstats

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Base creature combat statistics by class and level.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `level` | `tinyint` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `class` | `tinyint` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `basemana` | `int unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `attackpower` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `rangedattackpower` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `comment` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `level`, `class` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:10017](../../../src/server/game/Globals/ObjectMgr.cpp#L10017)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `level` | `uint8 Level = fields[0].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10030) |
| `class` | `uint8 Class = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10031) |
| `basemana` | `stats.BaseMana = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10038) |
| `attackpower` | `stats.AttackPower = fields[3].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10040) |
| `rangedattackpower` | `stats.RangedAttackPower = fields[4].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10041) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_classlevelstats` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_classlevelstats) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
