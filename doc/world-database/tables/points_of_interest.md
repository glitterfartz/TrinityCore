# points_of_interest

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Map markers shown by gossip and navigation interactions.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `PositionX` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 3 | `PositionY` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 4 | `PositionZ` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 5 | `Icon` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Flags` | `int unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 7 | `Importance` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `Name` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `WMOGroupID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gossip_menu_option](gossip_menu_option.md).`ActionPoiID` → [points_of_interest](points_of_interest.md).`ID`: Map point shown by selection.
- [points_of_interest_locale](points_of_interest_locale.md).`ID` → [points_of_interest](points_of_interest.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8296](../../../src/server/game/Globals/ObjectMgr.cpp#L8296)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8308) |
| `PositionZ` | `pointOfInterest.Pos.Relocate(fields[1].GetFloat(), fields[2].GetFloat(), fields[3].GetFloat())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8312) |
| `Icon` | `pointOfInterest.Icon            = fields[4].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8313) |
| `Flags` | `pointOfInterest.Flags           = fields[5].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8314) |
| `Importance` | `pointOfInterest.Importance      = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8315) |
| `Name` | `pointOfInterest.Name            = fields[7].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8316) |
| `WMOGroupID` | `pointOfInterest.WMOGroupID      = fields[8].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8317) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `points_of_interest` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/points_of_interest) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
