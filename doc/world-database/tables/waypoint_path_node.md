# waypoint_path_node

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Ordered positions, orientation, and pause delays for waypoint paths.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `PathId` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [waypoint_path.PathId](waypoint_path.md). Ordered nodes within a path. |
| 2 | `NodeId` | `int unsigned` | NO | `0` | PRI | — | Ordered node identity within PathId. |
| 3 | `PositionX` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 4 | `PositionY` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 5 | `PositionZ` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 6 | `Orientation` | `float` | YES | NULL / absent; see conventions | — | — | Facing angle in radians; NULL may leave orientation unspecified according to the loader. |
| 7 | `Delay` | `int unsigned` | NO | `0` | — | — | Pause delay in milliseconds; zero means no delay. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `PathId`, `NodeId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [waypoint_path_node](waypoint_path_node.md).`PathId` → [waypoint_path](waypoint_path.md).`PathId`: Ordered nodes within a path.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Movement/Waypoints/WaypointManager.cpp:75](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L75)
- [src/server/game/Movement/Waypoints/WaypointManager.cpp:125](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L125)
- [src/server/game/Movement/Waypoints/WaypointManager.cpp:195](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L195)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:49](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L49)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:50](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L50)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:51](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L51)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:52](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L52)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:53](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L53)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:54](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L54)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:55](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L55)

Additional source references exist; search the repository for the exact table name.

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `PathId` | `uint32 pathId = fields.PathId().GetUInt32();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L127) |
| `NodeId` | `path->Nodes.emplace_back(fields.NodeId().GetUInt32(), x, y, z, o, delay);` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L148) |
| `PositionX` | `float x = fields.PositionX().GetFloat();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L136) |
| `PositionY` | `float y = fields.PositionY().GetFloat();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L137) |
| `PositionZ` | `float z = fields.PositionZ().GetFloat();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L138) |
| `Orientation` | `Optional<float> o = fields.Orientation().GetFloatOrNull();` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L139) |
| `Delay` | `if (uint32 delayMs = fields.Delay().GetUInt32())` | [loader](../../../src/server/game/Movement/Waypoints/WaypointManager.cpp#L142) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `waypoint_path_node` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/waypoint_path_node) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
