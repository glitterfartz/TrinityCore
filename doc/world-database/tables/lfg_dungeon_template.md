# lfg_dungeon_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Dungeon-finder entry locations and custom dungeon settings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `dungeonId` | `int unsigned` | NO | `0` | PRI | — | Database comment: Unique id from LFGDungeons.dbc |
| 2 | `name` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 4 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 5 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 6 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 7 | `requiredItemLevel` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `dungeonId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/DungeonFinding/LFGMgr.cpp:218](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L218)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `dungeonId` | `uint32 dungeonId = fields[0].GetUInt32()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L230) |
| `position_x` | `data.x                  = fields[1].GetFloat()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L239) |
| `position_y` | `data.y                  = fields[2].GetFloat()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L240) |
| `position_z` | `data.z                  = fields[3].GetFloat()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L241) |
| `orientation` | `data.o                  = fields[4].GetFloat()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L242) |
| `requiredItemLevel` | `data.requiredItemLevel  = fields[5].GetUInt16()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L243) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `lfg_dungeon_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/lfg_dungeon_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
