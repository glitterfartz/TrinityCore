# points_of_interest_locale

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Localized text for points_of_interest. Parent identity fields and locale jointly select each translation.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [points_of_interest.ID](points_of_interest.md). Translation parent identity; include all identity components plus locale. |
| 2 | `locale` | `varchar(4)` | NO | NULL / absent; see conventions | PRI | — | Locale key (for example deDE or frFR); translates a parent record rather than creating independent gameplay content. |
| 3 | `Name` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `locale` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [points_of_interest_locale](points_of_interest_locale.md).`ID` → [points_of_interest](points_of_interest.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:325](../../../src/server/game/Globals/ObjectMgr.cpp#L325)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id                   = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L333) |
| `locale` | `std::string_view localeName = fields[1].GetStringView()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L334) |
| `Name` | `AddLocaleString(fields[2].GetStringView(), locale, data.Name)` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L341) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `points_of_interest_locale` LIMIT 5;
```

Translations must match the parent's full identity and an accepted locale; see [localization](../guides/localization.md).

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/points_of_interest_locale) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
