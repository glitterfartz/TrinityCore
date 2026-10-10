# creature_text_locale

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Localized text for creature_text. Parent identity fields and locale jointly select each translation.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [creature_text.CreatureID](creature_text.md). Translation parent identity; include all identity components plus locale. |
| 2 | `GroupID` | `tinyint unsigned` | NO | `0` | PRI | — | Logical reference to [creature_text.GroupID](creature_text.md). Translation parent identity; include all identity components plus locale. |
| 3 | `ID` | `tinyint unsigned` | NO | `0` | PRI | — | Logical reference to [creature_text.ID](creature_text.md). Translation parent identity; include all identity components plus locale. |
| 4 | `Locale` | `varchar(4)` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Text` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureID`, `GroupID`, `ID`, `Locale` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_text_locale](creature_text_locale.md).`GroupID` → [creature_text](creature_text.md).`GroupID`: Translation parent identity; include all identity components plus locale.
- [creature_text_locale](creature_text_locale.md).`ID` → [creature_text](creature_text.md).`ID`: Translation parent identity; include all identity components plus locale.
- [creature_text_locale](creature_text_locale.md).`CreatureID` → [creature_text](creature_text.md).`CreatureID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Texts/CreatureTextMgr.cpp:148](../../../src/server/game/Texts/CreatureTextMgr.cpp#L148)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id                   = fields[2].GetUInt8()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L159) |
| `Locale` | `std::string_view localeName = fields[3].GetStringView()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L160) |
| `Text` | `ObjectMgr::AddLocaleString(fields[4].GetStringView(), locale, data.Text)` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L167) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_text_locale` LIMIT 5;
```

Translations must match the parent's full identity and an accepted locale; see [localization](../guides/localization.md).

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_text_locale) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
