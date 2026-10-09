# creature_immunities

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Reusable sets of school, mechanic, effect, and other creature immunities.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `SchoolMask` | `tinyint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `DispelTypeMask` | `smallint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `MechanicsMask` | `bigint` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Effects` | `mediumtext` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `Auras` | `mediumtext` | NO | NULL / absent; see conventions | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `ImmuneAoE` | `tinyint(1)` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `ImmuneChain` | `tinyint(1)` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `Comment` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_template](creature_template.md).`CreatureImmunitiesId` → [creature_immunities](creature_immunities.md).`ID`: Reusable immunity definition.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:5356](../../../src/server/game/Spells/SpellMgr.cpp#L5356)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `int32 id = fields[0].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5361) |
| `SchoolMask` | `uint8 school = fields[1].GetInt8()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5362) |
| `DispelTypeMask` | `uint16 dispelType = fields[2].GetInt16()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5363) |
| `MechanicsMask` | `uint64 mechanics = fields[3].GetInt64()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L5364) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_immunities` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_immunities) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
