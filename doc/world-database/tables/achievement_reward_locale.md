# achievement_reward_locale

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Localized text for achievement_reward. Parent identity fields and locale jointly select each translation.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [achievement_reward.ID](achievement_reward.md). Translation parent identity; include all identity components plus locale. |
| 2 | `Locale` | `varchar(4)` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Subject` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Body` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `Locale` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [achievement_reward_locale](achievement_reward_locale.md).`ID` → [achievement_reward](achievement_reward.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Achievements/AchievementMgr.cpp:1343](../../../src/server/game/Achievements/AchievementMgr.cpp#L1343)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1355) |
| `Locale` | `std::string_view localeName = fields[1].GetStringView()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1356) |
| `Subject` | `ObjectMgr::AddLocaleString(fields[2].GetStringView(), locale, data.Subject)` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1369) |
| `Body` | `ObjectMgr::AddLocaleString(fields[3].GetStringView(), locale, data.Body)` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1370) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `achievement_reward_locale` LIMIT 5;
```

Translations must match the parent's full identity and an accepted locale; see [localization](../guides/localization.md).

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/achievement_reward_locale) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
