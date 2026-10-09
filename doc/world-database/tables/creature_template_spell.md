# creature_template_spell

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spells assigned to creature template slots.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Template extension. |
| 2 | `Index` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Spell` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureID`, `Index` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template_spell](creature_template_spell.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Template extension.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:567](../../../src/server/game/Globals/ObjectMgr.cpp#L567)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `CreatureID` | `uint32 creatureID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L581) |
| `Index` | `uint8 index       = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L582) |
| `Spell` | `creatureTemplate.spells[index] = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L598) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_template_spell` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_template_spell) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
