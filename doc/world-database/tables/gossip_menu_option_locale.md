# gossip_menu_option_locale

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Localized text for gossip_menu_option. Parent identity fields and locale jointly select each translation.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `MenuID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [gossip_menu_option.MenuID](gossip_menu_option.md). Translation parent identity; include all identity components plus locale. |
| 2 | `OptionID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [gossip_menu_option.OptionID](gossip_menu_option.md). Translation parent identity; include all identity components plus locale. |
| 3 | `Locale` | `varchar(4)` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `OptionText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `BoxText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Gossip confirmation prompt. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `MenuID`, `OptionID`, `Locale` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [gossip_menu_option_locale](gossip_menu_option_locale.md).`MenuID` → [gossip_menu_option](gossip_menu_option.md).`MenuID`: Translation parent identity; include all identity components plus locale.
- [gossip_menu_option_locale](gossip_menu_option_locale.md).`OptionID` → [gossip_menu_option](gossip_menu_option.md).`OptionID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:293](../../../src/server/game/Globals/ObjectMgr.cpp#L293)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `MenuID` | `uint32 menuId               = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L302) |
| `OptionID` | `uint32 optionId             = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L303) |
| `Locale` | `std::string_view localeName = fields[2].GetStringView()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L304) |
| `OptionText` | `AddLocaleString(fields[3].GetStringView(), locale, data.OptionText)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L311) |
| `BoxText` | `AddLocaleString(fields[4].GetStringView(), locale, data.BoxText)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L312) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `gossip_menu_option_locale` LIMIT 5;
```

Translations must match the parent's full identity and an accepted locale; see [localization](../guides/localization.md).

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/gossip_menu_option_locale) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
