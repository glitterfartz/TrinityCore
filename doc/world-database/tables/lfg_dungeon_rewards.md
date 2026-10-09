# lfg_dungeon_rewards

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Quest rewards for dungeon-finder completion by level.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `dungeonId` | `int unsigned` | NO | `0` | PRI | — | Database comment: Dungeon entry from dbc |
| 2 | `maxLevel` | `tinyint unsigned` | NO | `0` | PRI | — | Database comment: Max level at which this reward is rewarded |
| 3 | `firstQuestId` | `int unsigned` | NO | `0` | — | — | Database comment: Quest id with rewards for first dungeon this day |
| 4 | `otherQuestId` | `int unsigned` | NO | `0` | — | — | Database comment: Quest id with rewards for Nth dungeon this day |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `dungeonId`, `maxLevel` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/DungeonFinding/LFGMgr.cpp:130](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L130)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `dungeonId` | `uint32 dungeonId = fields[0].GetUInt32()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L144) |
| `maxLevel` | `uint32 maxLevel = fields[1].GetUInt8()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L145) |
| `firstQuestId` | `uint32 firstQuestId = fields[2].GetUInt32()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L146) |
| `otherQuestId` | `uint32 otherQuestId = fields[3].GetUInt32()` | [loader](../../../src/server/game/DungeonFinding/LFGMgr.cpp#L147) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `lfg_dungeon_rewards` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/lfg_dungeon_rewards) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
