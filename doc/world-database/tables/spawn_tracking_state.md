# spawn_tracking_state

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

State configuration for spawn tracking.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpawnType` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `SpawnId` | `bigint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `State` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Visible` | `tinyint unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `StateSpellVisualId` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `StateAnimId` | `smallint unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `StateAnimKitId` | `smallint unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `StateWorldEffects` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpawnType`, `SpawnId`, `State` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:11811](../../../src/server/game/Globals/ObjectMgr.cpp#L11811)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpawnType` | `SpawnObjectType spawnType = SpawnObjectType(fields[0].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11824) |
| `SpawnId` | `ObjectGuid::LowType spawnId = fields[1].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11825) |
| `State` | `SpawnTrackingState state = SpawnTrackingState(fields[2].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11826) |
| `Visible` | `spawnTrackingStateData.Visible = fields[3].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11858) |
| `StateSpellVisualId` | `spawnTrackingStateData.StateSpellVisualId = fields[4].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11859) |
| `StateAnimId` | `spawnTrackingStateData.StateAnimId = fields[5].GetUInt16OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11860) |
| `StateAnimKitId` | `spawnTrackingStateData.StateAnimKitId = fields[6].GetUInt16OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L11861) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spawn_tracking_state` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spawn_tracking_state) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
