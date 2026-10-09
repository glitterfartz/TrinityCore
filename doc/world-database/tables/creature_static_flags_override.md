# creature_static_flags_override

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Difficulty-specific static creature flag overrides.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpawnId` | `bigint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `DifficultyId` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `StaticFlags1` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `StaticFlags2` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `StaticFlags3` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `StaticFlags4` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `StaticFlags5` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `StaticFlags6` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `StaticFlags7` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `StaticFlags8` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpawnId`, `DifficultyId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:10862](../../../src/server/game/Globals/ObjectMgr.cpp#L10862)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpawnId` | `ObjectGuid::LowType spawnId = fields[0].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10875) |
| `DifficultyId` | `Difficulty difficultyId = static_cast<Difficulty>(fields[1].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10876) |
| `StaticFlags1` | `staticFlagsOverride.StaticFlags1 = static_cast<CreatureStaticFlags>(fields[2].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10897) |
| `StaticFlags2` | `staticFlagsOverride.StaticFlags2 = static_cast<CreatureStaticFlags2>(fields[3].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10899) |
| `StaticFlags3` | `staticFlagsOverride.StaticFlags3 = static_cast<CreatureStaticFlags3>(fields[4].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10901) |
| `StaticFlags4` | `staticFlagsOverride.StaticFlags4 = static_cast<CreatureStaticFlags4>(fields[5].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10903) |
| `StaticFlags5` | `staticFlagsOverride.StaticFlags5 = static_cast<CreatureStaticFlags5>(fields[6].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10905) |
| `StaticFlags6` | `staticFlagsOverride.StaticFlags6 = static_cast<CreatureStaticFlags6>(fields[7].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10907) |
| `StaticFlags7` | `staticFlagsOverride.StaticFlags7 = static_cast<CreatureStaticFlags7>(fields[8].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10909) |
| `StaticFlags8` | `staticFlagsOverride.StaticFlags8 = static_cast<CreatureStaticFlags8>(fields[9].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10911) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_static_flags_override` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_static_flags_override) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
