# graveyard_zone

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Associates zones and teams with resurrection locations.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Trigger System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `GhostZone` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Comment` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `GhostZone` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:6770](../../../src/server/game/Globals/ObjectMgr.cpp#L6770)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:33](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L33)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:34](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L34)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 safeLocId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6786) |
| `GhostZone` | `uint32 zoneId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6787) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `graveyard_zone` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/graveyard_zone) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
