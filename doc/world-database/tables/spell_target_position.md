# spell_target_position

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Fixed positional targets for spell effects.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Spell System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `EffectIndex` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `OrderIndex` | `int` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `MapID` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `PositionX` | `float` | NO | `0` | — | — | Map-space X coordinate. |
| 6 | `PositionY` | `float` | NO | `0` | — | — | Map-space Y coordinate. |
| 7 | `PositionZ` | `float` | NO | `0` | — | — | Map-space Z coordinate (height). |
| 8 | `Orientation` | `float` | YES | NULL / absent; see conventions | — | — | Facing angle in radians; NULL may leave orientation unspecified according to the loader. |
| 9 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `EffectIndex`, `OrderIndex` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:1166](../../../src/server/game/Spells/SpellMgr.cpp#L1166)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 spellId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1177) |
| `EffectIndex` | `SpellEffIndex effIndex = SpellEffIndex(fields[1].GetUInt8())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1178) |
| `PositionZ` | `SpellTargetPosition st(fields[3].GetUInt16(), fields[4].GetFloat(), fields[5].GetFloat(), fields[6].GetFloat())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1180) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_target_position` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_target_position) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
