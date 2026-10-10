# instance_spawn_groups

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Controls spawn groups using instance boss-state conditions.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `instanceMapId` | `smallint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `bossStateId` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `bossStates` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `spawnGroupId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `flags` | `tinyint unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `instanceMapId`, `bossStateId`, `spawnGroupId`, `bossStates` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:2857](../../../src/server/game/Globals/ObjectMgr.cpp#L2857)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `instanceMapId` | `TC_LOG_ERROR("sql.sql", "Invalid spawn group {} specified for instance {}. Skipped.", spawnGroupId, fields[0].GetUInt16())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2873) |
| `bossStateId` | `info.BossStateId = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2887) |
| `bossStates` | `uint8 const states = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2890) |
| `spawnGroupId` | `uint32 const spawnGroupId = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2869) |
| `flags` | `uint8 const flags = fields[4].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L2899) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `instance_spawn_groups` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/instance_spawn_groups) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
