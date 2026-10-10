# access_requirement

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Restricts instance entry by map and difficulty, level, items, quests, and achievements.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: MyISAM. Collation: utf8mb4_unicode_ci.

Database comment: Access Requirements

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `mapId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Client Map identifier whose instance access is restricted. |
| 2 | `difficulty` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `level_min` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `level_max` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `item` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `item2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `quest_done_A` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `quest_done_H` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `completed_achievement` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `quest_failed_text` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `comment` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `mapId`, `difficulty` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:7172](../../../src/server/game/Globals/ObjectMgr.cpp#L7172)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `difficulty` | `Difficulty difficulty = Difficulty(fields[1].GetInt32())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7193) |
| `level_min` | `ar->levelMin            = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7203) |
| `level_max` | `ar->levelMax            = fields[3].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7204) |
| `item` | `ar->item                = fields[4].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7205) |
| `item2` | `ar->item2               = fields[5].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7206) |
| `quest_done_A` | `ar->quest_A             = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7207) |
| `quest_done_H` | `ar->quest_H             = fields[7].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7208) |
| `completed_achievement` | `ar->achievement         = fields[8].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7209) |
| `quest_failed_text` | `ar->questFailedText     = fields[9].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L7210) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `access_requirement` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/access_requirement) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
