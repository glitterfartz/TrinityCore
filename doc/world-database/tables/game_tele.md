# game_tele

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Named destinations used by game-master teleport commands.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Tele Command

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | auto_increment | Row identity within this table; use the complete primary key when selecting or editing. |
| 2 | `position_x` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 3 | `position_y` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 4 | `position_z` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 5 | `orientation` | `float` | NO | `0` | — | — | Facing angle in radians. |
| 6 | `map` | `smallint unsigned` | NO | `0` | — | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 7 | `name` | `varchar(100)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9039](../../../src/server/game/Globals/ObjectMgr.cpp#L9039)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:35](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L35)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:36](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L36)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `id` | `uint32 id         = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9053) |
| `position_x` | `gt.position_x     = fields[1].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9057) |
| `position_y` | `gt.position_y     = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9058) |
| `position_z` | `gt.position_z     = fields[3].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9059) |
| `orientation` | `gt.orientation    = fields[4].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9060) |
| `map` | `gt.mapId          = fields[5].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9061) |
| `name` | `gt.name           = fields[6].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9062) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `game_tele` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/game_tele) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
