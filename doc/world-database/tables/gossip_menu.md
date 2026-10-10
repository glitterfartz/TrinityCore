# gossip_menu

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

NPC dialogue menus and their NPC-text records.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `MenuID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `TextID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [npc_text.ID](npc_text.md). NPC text for the menu. |
| 3 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `MenuID`, `TextID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_gossip](creature_template_gossip.md).`MenuID` → [gossip_menu](gossip_menu.md).`MenuID`: Available menu.
- [gossip_menu](gossip_menu.md).`TextID` → [npc_text](npc_text.md).`ID`: NPC text for the menu.
- [gossip_menu_option](gossip_menu_option.md).`MenuID` → [gossip_menu](gossip_menu.md).`MenuID`: Menu containing the option.
- [gossip_menu_option](gossip_menu_option.md).`ActionMenuID` → [gossip_menu](gossip_menu.md).`MenuID`: Submenu navigation; zero may mean no navigation.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9524](../../../src/server/game/Globals/ObjectMgr.cpp#L9524)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `MenuID` | `gMenu.MenuID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9538) |
| `TextID` | `gMenu.TextID = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9539) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gossip_menu` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gossip_menu) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
