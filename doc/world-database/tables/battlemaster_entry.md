# battlemaster_entry

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Maps NPC templates to the battleground types they offer.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | `0` | PRI | — | Database comment: Entry of a creature |
| 2 | `bg_template` | `int unsigned` | NO | `0` | — | — | Database comment: Battleground template id |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Battlegrounds/BattlegroundMgr.cpp:618](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L618)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L634) |
| `bg_template` | `uint32 bgTypeId  = fields[1].GetUInt32()` | [loader](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L646) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `battlemaster_entry` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/battlemaster_entry) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
