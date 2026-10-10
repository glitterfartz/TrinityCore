# guild_rewards

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Items available as guild rewards and their requirements.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ItemID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `MinGuildRep` | `tinyint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `RaceMask` | `bigint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Cost` | `bigint unsigned` | YES | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ItemID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Guilds/GuildMgr.cpp:500](../../../src/server/game/Guilds/GuildMgr.cpp#L500)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ItemID` | `reward.ItemID        = fields[0].GetUInt32()` | [loader](../../../src/server/game/Guilds/GuildMgr.cpp#L514) |
| `MinGuildRep` | `reward.MinGuildRep   = fields[1].GetUInt8()` | [loader](../../../src/server/game/Guilds/GuildMgr.cpp#L515) |
| `RaceMask` | `reward.RaceMask      = { advstd::bit_cast<std::array<int32, 2>>(fields[2].GetUInt64()) }` | [loader](../../../src/server/game/Guilds/GuildMgr.cpp#L516) |
| `Cost` | `reward.Cost          = fields[3].GetUInt64()` | [loader](../../../src/server/game/Guilds/GuildMgr.cpp#L517) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `guild_rewards` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/guild_rewards) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
