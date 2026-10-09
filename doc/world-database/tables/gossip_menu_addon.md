# gossip_menu_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Additional menu-level gossip configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `MenuID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `FriendshipFactionID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `LfgDungeonsID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `MenuID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9685](../../../src/server/game/Globals/ObjectMgr.cpp#L9685)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `MenuID` | `uint32 menuID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9697) |
| `FriendshipFactionID` | `addon.FriendshipFactionID = fields[1].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9699) |
| `LfgDungeonsID` | `addon.LfgDungeonsID = fields[2].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9700) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gossip_menu_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gossip_menu_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
