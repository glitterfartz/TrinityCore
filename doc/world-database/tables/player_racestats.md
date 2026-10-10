# player_racestats

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Base racial statistics.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Stores race stats.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `race` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `str` | `smallint` | NO | NULL / absent; see conventions | — | — | Database comment: strength |
| 3 | `agi` | `smallint` | NO | NULL / absent; see conventions | — | — | Database comment: agility |
| 4 | `sta` | `smallint` | NO | NULL / absent; see conventions | — | — | Database comment: stamina |
| 5 | `inte` | `smallint` | NO | NULL / absent; see conventions | — | — | Database comment: intellect |
| 6 | `spi` | `smallint` | NO | NULL / absent; see conventions | — | — | Database comment: spirit |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `race` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:4268](../../../src/server/game/Globals/ObjectMgr.cpp#L4268)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `race` | `uint32 current_race = fields[0].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L4280) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `player_racestats` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/player_racestats) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
