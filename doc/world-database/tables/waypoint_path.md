# waypoint_path

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Reusable waypoint paths and movement configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `PathId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Reusable path identity. |
| 2 | `MoveType` | `tinyint unsigned` | NO | `0` | — | — | WaypointMoveType enum: path movement style; see spawn/movement enums. |
| 3 | `Flags` | `tinyint unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 4 | `Velocity` | `float` | YES | NULL / absent; see conventions | — | — | Optional positive movement velocity; NULL uses the default, and nonpositive values are rejected/reset. |
| 5 | `Comment` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `PathId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [waypoint_path_node](waypoint_path_node.md).`PathId` → [waypoint_path](waypoint_path.md).`PathId`: Ordered nodes within a path.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Movement/Waypoints/WaypointManager.cpp:48](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L48)
- [src/server/game/Movement/Waypoints/WaypointManager.cpp:99](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L99)
- [src/server/game/Movement/Waypoints/WaypointManager.cpp:175](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L175)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:47](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L47)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:48](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L48)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `PathId` | `uint32 pathId = fields.PathId().GetUInt32();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L101) |
| `MoveType` | `path.MoveType = WaypointMoveType(fields.MoveType().GetUInt8());` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L105) |
| `Flags` | `path.Flags = WaypointPathFlags(fields.Flags().GetUInt8());` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L113) |
| `Velocity` | `path.Velocity = fields.Velocity().GetFloatOrNull();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L114) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `waypoint_path` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/waypoint_path) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
