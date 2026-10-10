# creature_onkill_reputation

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Faction reputation awarded when a creature is killed.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Creature OnKill Reputation gain

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `creature_id` | `int unsigned` | NO | `0` | PRI | — | Database comment: Creature Identifier |
| 2 | `RewOnKillRepFaction1` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `RewOnKillRepFaction2` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `MaxStanding1` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `IsTeamAward1` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `RewOnKillRepValue1` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `MaxStanding2` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `IsTeamAward2` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `RewOnKillRepValue2` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `TeamDependent` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `creature_id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8130](../../../src/server/game/Globals/ObjectMgr.cpp#L8130)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `creature_id` | `uint32 creature_id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8145) |
| `RewOnKillRepFaction1` | `repOnKill.RepFaction1          = fields[1].GetInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8148) |
| `RewOnKillRepFaction2` | `repOnKill.RepFaction2          = fields[2].GetInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8149) |
| `MaxStanding1` | `repOnKill.ReputationMaxCap1  = fields[4].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8151) |
| `IsTeamAward1` | `repOnKill.IsTeamAward1        = fields[3].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8150) |
| `RewOnKillRepValue1` | `repOnKill.RepValue1            = fields[5].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8152) |
| `MaxStanding2` | `repOnKill.ReputationMaxCap2  = fields[7].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8154) |
| `IsTeamAward2` | `repOnKill.IsTeamAward2        = fields[6].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8153) |
| `RewOnKillRepValue2` | `repOnKill.RepValue2            = fields[8].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8155) |
| `TeamDependent` | `repOnKill.TeamDependent       = fields[9].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8156) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_onkill_reputation` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_onkill_reputation) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
