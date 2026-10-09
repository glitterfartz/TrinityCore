# spell_pet_auras

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Pet auras selected by owner spell and pet entry.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `spell` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: dummy spell id |
| 2 | `effectId` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `pet` | `int unsigned` | NO | `0` | PRI | — | Database comment: pet id; 0 = all |
| 4 | `aura` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Database comment: pet aura id |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `spell`, `effectId`, `pet` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:1972](../../../src/server/game/Spells/SpellMgr.cpp#L1972)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `spell` | `uint32 spell = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1984) |
| `effectId` | `SpellEffIndex eff = SpellEffIndex(fields[1].GetUInt8())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1985) |
| `pet` | `uint32 pet = fields[2].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1986) |
| `aura` | `uint32 aura = fields[3].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1987) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_pet_auras` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_pet_auras) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
