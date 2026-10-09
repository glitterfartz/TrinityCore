# reputation_reward_rate

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Faction-specific reputation rate multipliers by reward source.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `faction` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `quest_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `quest_daily_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `quest_weekly_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `quest_monthly_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `quest_repeatable_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `creature_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `spell_rate` | `float` | NO | `1` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `faction` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8039](../../../src/server/game/Globals/ObjectMgr.cpp#L8039)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `faction` | `uint32 factionId            = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8050) |
| `quest_rate` | `repRate.questRate           = fields[1].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8054) |
| `quest_daily_rate` | `repRate.questDailyRate      = fields[2].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8055) |
| `quest_weekly_rate` | `repRate.questWeeklyRate     = fields[3].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8056) |
| `quest_monthly_rate` | `repRate.questMonthlyRate    = fields[4].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8057) |
| `quest_repeatable_rate` | `repRate.questRepeatableRate = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8058) |
| `creature_rate` | `repRate.creatureRate        = fields[6].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8059) |
| `spell_rate` | `repRate.spellRate           = fields[7].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8060) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `reputation_reward_rate` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/reputation_reward_rate) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
