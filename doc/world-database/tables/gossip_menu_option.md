# gossip_menu_option

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Selectable gossip options and their navigation, interaction, and confirmation settings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `MenuID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [gossip_menu.MenuID](gossip_menu.md). Menu containing the option. |
| 2 | `GossipOptionID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `OptionID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `OptionNpc` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `OptionText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `OptionBroadcastTextID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `Language` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `Flags` | `int` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 9 | `ActionMenuID` | `int unsigned` | NO | `0` | — | — | Logical reference to [gossip_menu.MenuID](gossip_menu.md). Submenu navigation; zero may mean no navigation. |
| 10 | `ActionPoiID` | `int unsigned` | NO | `0` | — | — | Logical reference to [points_of_interest.ID](points_of_interest.md). Map point shown by selection. |
| 11 | `GossipNpcOptionID` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `BoxCoded` | `tinyint unsigned` | NO | `0` | — | — | Whether the gossip confirmation asks for typed input. |
| 13 | `BoxMoney` | `bigint unsigned` | NO | `0` | — | — | Gossip confirmation cost in copper. |
| 14 | `BoxText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Gossip confirmation prompt. |
| 15 | `BoxBroadcastTextID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `SpellID` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 17 | `OverrideIconID` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `MenuID`, `OptionID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gossip_menu_option](gossip_menu_option.md).`MenuID` → [gossip_menu](gossip_menu.md).`MenuID`: Menu containing the option.
- [gossip_menu_option](gossip_menu_option.md).`ActionMenuID` → [gossip_menu](gossip_menu.md).`MenuID`: Submenu navigation; zero may mean no navigation.
- [gossip_menu_option](gossip_menu_option.md).`ActionPoiID` → [points_of_interest](points_of_interest.md).`ID`: Map point shown by selection.
- [gossip_menu_option_locale](gossip_menu_option_locale.md).`MenuID` → [gossip_menu_option](gossip_menu_option.md).`MenuID`: Translation parent identity; include all identity components plus locale.
- [gossip_menu_option_locale](gossip_menu_option_locale.md).`OptionID` → [gossip_menu_option](gossip_menu_option.md).`OptionID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9561](../../../src/server/game/Globals/ObjectMgr.cpp#L9561)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `MenuID` | `gMenuItem.MenuID                = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9582) |
| `GossipOptionID` | `gMenuItem.GossipOptionID        = fields[1].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9583) |
| `OptionID` | `gMenuItem.OrderIndex            = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9584) |
| `OptionNpc` | `gMenuItem.OptionNpc             = GossipOptionNpc(fields[3].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9585) |
| `OptionText` | `gMenuItem.OptionText            = fields[4].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9586) |
| `OptionBroadcastTextID` | `gMenuItem.OptionBroadcastTextID = fields[5].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9587) |
| `Language` | `gMenuItem.Language              = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9588) |
| `Flags` | `gMenuItem.Flags                 = GossipOptionFlags(fields[7].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9589) |
| `ActionMenuID` | `gMenuItem.ActionMenuID          = fields[8].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9590) |
| `ActionPoiID` | `gMenuItem.ActionPoiID           = fields[9].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9591) |
| `GossipNpcOptionID` | `gMenuItem.GossipNpcOptionID     = fields[10].GetInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9592) |
| `BoxCoded` | `gMenuItem.BoxCoded              = fields[11].GetBool()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9593) |
| `BoxMoney` | `gMenuItem.BoxMoney              = fields[12].GetUInt64()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9594) |
| `BoxText` | `gMenuItem.BoxText               = fields[13].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9595) |
| `BoxBroadcastTextID` | `gMenuItem.BoxBroadcastTextID    = fields[14].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9596) |
| `SpellID` | `gMenuItem.SpellID               = fields[15].GetInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9597) |
| `OverrideIconID` | `gMenuItem.OverrideIconID        = fields[16].GetInt32OrNull()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9598) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gossip_menu_option` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gossip_menu_option) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
