# reputation_spillover_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Reputation spillover destinations, rates, and rank limits.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Reputation spillover reputation gain

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `faction` | `smallint unsigned` | NO | `0` | PRI | — | Database comment: faction entry |
| 2 | `faction1` | `smallint unsigned` | NO | `0` | — | — | Database comment: faction to give spillover for |
| 3 | `rate_1` | `float` | NO | `0` | — | — | Database comment: the given rep points * rate |
| 4 | `rank_1` | `tinyint unsigned` | NO | `0` | — | — | Database comment: max rank,above this will not give any spillover |
| 5 | `faction2` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `rate_2` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `rank_2` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `faction3` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `rate_3` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `rank_3` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `faction4` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `rate_4` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `rank_4` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `faction5` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `rate_5` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `rank_5` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `faction` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8199](../../../src/server/game/Globals/ObjectMgr.cpp#L8199)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `faction` | `uint32 factionId                = fields[0].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8211) |
| `faction1` | `repTemplate.faction[0]          = fields[1].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8215) |
| `rate_1` | `repTemplate.faction_rate[0]     = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8216) |
| `rank_1` | `repTemplate.faction_rank[0]     = fields[3].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8217) |
| `faction2` | `repTemplate.faction[1]          = fields[4].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8218) |
| `rate_2` | `repTemplate.faction_rate[1]     = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8219) |
| `rank_2` | `repTemplate.faction_rank[1]     = fields[6].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8220) |
| `faction3` | `repTemplate.faction[2]          = fields[7].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8221) |
| `rate_3` | `repTemplate.faction_rate[2]     = fields[8].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8222) |
| `rank_3` | `repTemplate.faction_rank[2]     = fields[9].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8223) |
| `faction4` | `repTemplate.faction[3]          = fields[10].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8224) |
| `rate_4` | `repTemplate.faction_rate[3]     = fields[11].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8225) |
| `rank_4` | `repTemplate.faction_rank[3]     = fields[12].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8226) |
| `faction5` | `repTemplate.faction[4]          = fields[13].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8227) |
| `rate_5` | `repTemplate.faction_rate[4]     = fields[14].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8228) |
| `rank_5` | `repTemplate.faction_rank[4]     = fields[15].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8229) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `reputation_spillover_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/reputation_spillover_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
