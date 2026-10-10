# gameobject_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Shared object definitions; Data0–Data34 are interpreted according to object type.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Gameobject System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `type` | `tinyint unsigned` | NO | `0` | — | — | Gameobject type discriminator; determines the complete Data0–Data34 layout. |
| 3 | `displayId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `name` | `varchar(200)` | NO | NULL / absent; see conventions | MUL | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `IconName` | `varchar(100)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `castBarCaption` | `varchar(100)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `unk1` | `varchar(100)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `size` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `Data0` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 10 | `Data1` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 11 | `Data2` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 12 | `Data3` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 13 | `Data4` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 14 | `Data5` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 15 | `Data6` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 16 | `Data7` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 17 | `Data8` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 18 | `Data9` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 19 | `Data10` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 20 | `Data11` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 21 | `Data12` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 22 | `Data13` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 23 | `Data14` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 24 | `Data15` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 25 | `Data16` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 26 | `Data17` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 27 | `Data18` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 28 | `Data19` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 29 | `Data20` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 30 | `Data21` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 31 | `Data22` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 32 | `Data23` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 33 | `Data24` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 34 | `Data25` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 35 | `Data26` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 36 | `Data27` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 37 | `Data28` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 38 | `Data29` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 39 | `Data30` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 40 | `Data31` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 41 | `Data32` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 42 | `Data33` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 43 | `Data34` | `int` | NO | `0` | — | — | Type-dependent union slot. See [gameobject data layouts](../reference/gameobject-data.md); never interpret this slot without type. |
| 44 | `ContentTuningId` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 45 | `RequiredLevel` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 46 | `AIName` | `varchar(64)` | NO | `''` | — | — | Registered AI implementation name. SmartAI requires the corresponding SmartAI source rows. |
| 47 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 48 | `StringId` | `varchar(64)` | YES | NULL / absent; see conventions | — | — | Author-defined string identifier used by object lookup and string-ID conditions. |
| 49 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `idx_name` | No | `name` | BTREE |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gameobject](gameobject.md).`id` → [gameobject_template](gameobject_template.md).`entry`: Template identity shared by gameobject spawns.
- [gameobject_queststarter](gameobject_queststarter.md).`id` → [gameobject_template](gameobject_template.md).`entry`: Gameobject template identity.
- [gameobject_template_locale](gameobject_template_locale.md).`entry` → [gameobject_template](gameobject_template.md).`entry`: Translation parent identity; include all identity components plus locale.
- [gameobject_questender](gameobject_questender.md).`id` → [gameobject_template](gameobject_template.md).`entry`: Gameobject template identity.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:7565](../../../src/server/game/Globals/ObjectMgr.cpp#L7565)
- [src/server/game/Maps/TransportMgr.cpp:198](../../../src/server/game/Maps/TransportMgr.cpp#L198)
- [src/server/scripts/Commands/cs_gobject.cpp:198](../../../src/server/scripts/Commands/cs_gobject.cpp#L198)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7585) |
| `type` | `got.type           = uint32(fields[1].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7589) |
| `displayId` | `got.displayId      = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7590) |
| `name` | `got.name           = fields[3].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7591) |
| `IconName` | `got.IconName       = fields[4].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7592) |
| `castBarCaption` | `got.castBarCaption = fields[5].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7593) |
| `unk1` | `got.unk1           = fields[6].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7594) |
| `size` | `got.size           = fields[7].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7595) |
| `ContentTuningId` | `got.ContentTuningId = fields[43].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7600) |
| `RequiredLevel` | `got.RequiredLevel = fields[44].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7601) |
| `AIName` | `got.AIName = fields[45].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7602) |
| `ScriptName` | `got.ScriptId = GetScriptId(fields[46].GetStringView())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7603) |
| `StringId` | `got.StringId = fields[47].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7604) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gameobject_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gameobject_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
