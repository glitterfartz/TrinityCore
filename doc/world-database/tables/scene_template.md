# scene_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Scene package configuration and compiled scene script bindings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SceneId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Flags` | `int unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 3 | `ScriptPackageID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Encrypted` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SceneId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:10971](../../../src/server/game/Globals/ObjectMgr.cpp#L10971)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SceneId` | `uint32 sceneId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10983) |
| `Flags` | `sceneTemplate.PlaybackFlags     = static_cast<SceneFlag>(fields[1].GetUInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10986) |
| `ScriptPackageID` | `sceneTemplate.ScenePackageId    = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10987) |
| `Encrypted` | `sceneTemplate.Encrypted         = fields[3].GetUInt8() != 0` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10988) |
| `ScriptName` | `sceneTemplate.ScriptId          = GetScriptId(fields[4].GetStringView())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L10989) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `scene_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/scene_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
