# creature_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Per-spawn path, appearance, emote, and aura configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Logical reference to [creature.guid](creature.md). Per-spawn addon; template addon provides defaults. |
| 2 | `PathId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `mount` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `MountCreatureID` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `StandState` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `AnimTier` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `VisFlags` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `SheathState` | `tinyint unsigned` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `PvPFlags` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `emote` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `aiAnimKit` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `movementAnimKit` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `meleeAnimKit` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `visibilityDistanceType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `auras` | `mediumtext` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_addon](creature_addon.md).`guid` → [creature](creature.md).`guid`: Per-spawn addon; template addon provides defaults.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1177](../../../src/server/game/Globals/ObjectMgr.cpp#L1177)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:60](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L60)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:61](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L61)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:62](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L62)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:63](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L63)
- [src/server/scripts/Commands/cs_wp.cpp:182](../../../src/server/scripts/Commands/cs_wp.cpp#L182)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `guid` | `ObjectGuid::LowType guid = fields[0].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1190) |
| `PathId` | `creatureAddon.PathId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1201) |
| `mount` | `creatureAddon.mount                     = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1208) |
| `StandState` | `creatureAddon.standState                = fields[3].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1209) |
| `AnimTier` | `creatureAddon.animTier                  = fields[4].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1210) |
| `VisFlags` | `creatureAddon.visFlags                  = fields[5].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1211) |
| `SheathState` | `creatureAddon.sheathState               = fields[6].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1212) |
| `PvPFlags` | `creatureAddon.pvpFlags                  = fields[7].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1213) |
| `emote` | `creatureAddon.emote                     = fields[8].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1214) |
| `aiAnimKit` | `creatureAddon.aiAnimKit                 = fields[9].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1215) |
| `movementAnimKit` | `creatureAddon.movementAnimKit           = fields[10].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1216) |
| `meleeAnimKit` | `creatureAddon.meleeAnimKit              = fields[11].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1217) |
| `visibilityDistanceType` | `creatureAddon.visibilityDistanceType    = VisibilityDistanceType(fields[12].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1218) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
