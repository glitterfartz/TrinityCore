# spell_totem_model

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Totem display model by spell and race.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpellID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `RaceID` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `DisplayID` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpellID`, `RaceID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:5612](../../../src/server/game/Spells/SpellMgr.cpp#L5612)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpellID` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5625) |
| `RaceID` | `uint8 race = fields[1].GetUInt8()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5626) |
| `DisplayID` | `uint32 displayId = fields[2].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5627) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_totem_model` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_totem_model) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
