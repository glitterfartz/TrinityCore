# npc_spellclick_spells

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spells cast when players interact with spell-click NPCs.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `npc_entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: reference to creature_template |
| 2 | `spell_id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: spell which should be casted  |
| 3 | `cast_flags` | `tinyint unsigned` | NO | NULL / absent; see conventions | — | — | Database comment: first bit defines caster: 1=player, 0=creature; second bit defines target, same mapping as caster bit |
| 4 | `user_type` | `smallint unsigned` | NO | `0` | — | — | Database comment: relation with summoner: 0-no 1-friendly 2-raid 3-party player can click |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `npc_entry`, `spell_id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:8417](../../../src/server/game/Globals/ObjectMgr.cpp#L8417)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `npc_entry` | `uint32 npc_entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8431) |
| `spell_id` | `uint32 spellid = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8439) |
| `cast_flags` | `uint8 castFlags = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8451) |
| `user_type` | `uint8 userType = fields[3].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L8447) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `npc_spellclick_spells` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/npc_spellclick_spells) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
