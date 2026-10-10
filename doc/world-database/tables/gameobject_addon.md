# gameobject_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Per-spawn gameobject addon configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `guid` | `bigint unsigned` | NO | `0` | PRI | — | Logical reference to [gameobject.guid](gameobject.md). Per-spawn addon. |
| 2 | `parent_rotation0` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `parent_rotation1` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `parent_rotation2` | `float` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `parent_rotation3` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `invisibilityType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `invisibilityValue` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `WorldEffectID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `AIAnimKitID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `guid` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gameobject_addon](gameobject_addon.md).`guid` → [gameobject](gameobject.md).`guid`: Per-spawn addon.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:1322](../../../src/server/game/Globals/ObjectMgr.cpp#L1322)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:80](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L80)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `guid` | `ObjectGuid::LowType guid = fields[0].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1335) |
| `parent_rotation3` | `gameObjectAddon.ParentRotation = QuaternionData(fields[1].GetFloat(), fields[2].GetFloat(), fields[3].GetFloat(), fields[4].GetFloat())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1345) |
| `invisibilityType` | `gameObjectAddon.invisibilityType = InvisibilityType(fields[5].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1346) |
| `invisibilityValue` | `gameObjectAddon.InvisibilityValue = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1347) |
| `WorldEffectID` | `gameObjectAddon.WorldEffectID = fields[7].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1348) |
| `AIAnimKitID` | `gameObjectAddon.AIAnimKitID   = fields[8].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L1349) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gameobject_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gameobject_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
