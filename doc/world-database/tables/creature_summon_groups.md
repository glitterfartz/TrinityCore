# creature_summon_groups

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Groups of creatures summoned together by a typed summoner.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `summonerId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `summonerType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `groupId` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `entry` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 6 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 7 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 8 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 9 | `summonType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `summonTime` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `Comment` | `varchar(255)` | NO | `''` | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

No indexes were reported in information_schema for this object.

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2010](../../../src/server/game/Globals/ObjectMgr.cpp#L2010)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `summonerId` | `uint32 summonerId               = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2023) |
| `summonerType` | `SummonerType summonerType       = SummonerType(fields[1].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2024) |
| `groupId` | `uint8 group                     = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2025) |
| `entry` | `data.entry                      = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2056) |
| `position_x` | `float posX                      = fields[4].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2064) |
| `position_y` | `float posY                      = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2065) |
| `position_z` | `float posZ                      = fields[6].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2066) |
| `orientation` | `float orientation               = fields[7].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2067) |
| `summonType` | `data.type                       = TempSummonType(fields[8].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2071) |
| `summonTime` | `data.time                       = Milliseconds(fields[9].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2079) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_summon_groups` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_summon_groups) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
