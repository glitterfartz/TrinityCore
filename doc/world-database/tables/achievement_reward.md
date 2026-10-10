# achievement_reward

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Defines titles and mail rewards granted for achievements.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: MyISAM. Collation: utf8mb4_unicode_ci.

Database comment: Loot System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `TitleA` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `TitleH` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `ItemID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Sender` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Subject` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `Body` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `MailTemplateID` | `int unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [achievement_reward_locale](achievement_reward_locale.md).`ID` → [achievement_reward](achievement_reward.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Achievements/AchievementMgr.cpp:1228](../../../src/server/game/Achievements/AchievementMgr.cpp#L1228)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1239) |
| `TitleA` | `reward.TitleId[0]       = fields[1].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1248) |
| `TitleH` | `reward.TitleId[1]       = fields[2].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1249) |
| `ItemID` | `reward.ItemId           = fields[3].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1250) |
| `Sender` | `reward.SenderCreatureId = fields[4].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1251) |
| `Subject` | `reward.Subject          = fields[5].GetString()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1252) |
| `Body` | `reward.Body             = fields[6].GetString()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1253) |
| `MailTemplateID` | `reward.MailTemplateId   = fields[7].GetUInt32()` | [loader](../../../src/server/game/Achievements/AchievementMgr.cpp#L1254) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `achievement_reward` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/achievement_reward) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
