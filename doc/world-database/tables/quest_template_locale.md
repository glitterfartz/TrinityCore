# quest_template_locale

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Localized text for quest_template. Parent identity fields and locale jointly select each translation.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [quest_template.ID](quest_template.md). Translation parent identity; include all identity components plus locale. |
| 2 | `locale` | `varchar(4)` | NO | NULL / absent; see conventions | PRI | — | Locale key (for example deDE or frFR); translates a parent record rather than creating independent gameplay content. |
| 3 | `LogTitle` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `LogDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `QuestDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `AreaDescription` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `PortraitGiverText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `PortraitGiverName` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `PortraitTurnInText` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `PortraitTurnInName` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `QuestCompletionLog` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `locale` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_template_locale](quest_template_locale.md).`ID` → [quest_template](quest_template.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:5383](../../../src/server/game/Globals/ObjectMgr.cpp#L5383)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `locale` | `std::string_view localeName     = fields[1].GetStringView()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5395) |
| `LogTitle` | `AddLocaleString(fields[2].GetStringView(), locale, data.LogTitle)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5402) |
| `LogDescription` | `AddLocaleString(fields[3].GetStringView(), locale, data.LogDescription)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5403) |
| `QuestDescription` | `AddLocaleString(fields[4].GetStringView(), locale, data.QuestDescription)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5404) |
| `AreaDescription` | `AddLocaleString(fields[5].GetStringView(), locale, data.AreaDescription)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5405) |
| `PortraitGiverText` | `AddLocaleString(fields[6].GetStringView(), locale, data.PortraitGiverText)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5406) |
| `PortraitGiverName` | `AddLocaleString(fields[7].GetStringView(), locale, data.PortraitGiverName)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5407) |
| `PortraitTurnInText` | `AddLocaleString(fields[8].GetStringView(), locale, data.PortraitTurnInText)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5408) |
| `PortraitTurnInName` | `AddLocaleString(fields[9].GetStringView(), locale, data.PortraitTurnInName)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5409) |
| `QuestCompletionLog` | `AddLocaleString(fields[10].GetStringView(), locale, data.QuestCompletionLog)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L5410) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_template_locale` LIMIT 5;
```

Translations must match the parent's full identity and an accepted locale; see [localization](../guides/localization.md).

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_template_locale) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
