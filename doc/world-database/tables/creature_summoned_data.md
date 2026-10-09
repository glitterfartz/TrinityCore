# creature_summoned_data

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Template data specific to summoned creatures.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `CreatureIDVisibleToSummoner` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `GroundMountDisplayID` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `FlyingMountDisplayID` | `int unsigned` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `DespawnOnQuestsRemoved` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:665](../../../src/server/game/Globals/ObjectMgr.cpp#L665)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `CreatureID` | `uint32 creatureId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L677) |
| `CreatureIDVisibleToSummoner` | `summonedData.CreatureIDVisibleToSummoner = fields[1].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L685) |
| `GroundMountDisplayID` | `summonedData.GroundMountDisplayID = fields[2].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L686) |
| `FlyingMountDisplayID` | `summonedData.FlyingMountDisplayID = fields[3].GetUInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L687) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_summoned_data` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_summoned_data) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
