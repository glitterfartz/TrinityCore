# creature_formations

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Leader/member associations and follow geometry for creature formations.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `leaderGUID` | `bigint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `memberGUID` | `bigint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `dist` | `float` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `angle` | `float` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `groupAI` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `point_1` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `point_2` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `memberGUID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Entities/Creature/CreatureGroups.cpp:103](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L103)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:46](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L46)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `leaderGUID` | `ObjectGuid::LowType leaderSpawnId = fields[0].GetUInt64()` | [loader](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L117) |
| `memberGUID` | `ObjectGuid::LowType memberSpawnId = fields[1].GetUInt64()` | [loader](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L118) |
| `dist` | `member.FollowDist             = fields[2].GetFloat()` | [loader](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L145) |
| `angle` | `member.FollowAngle            = fields[3].GetFloat() * float(M_PI) / 180.0f` | [loader](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L146) |
| `groupAI` | `member.GroupAI                    = fields[4].GetUInt32()` | [loader](../../../src/server/game/Entities/Creature/CreatureGroups.cpp#L149) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_formations` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_formations) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
