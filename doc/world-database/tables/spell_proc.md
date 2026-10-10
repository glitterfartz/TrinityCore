# spell_proc

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Overrides spell proc filters, chances, cooldowns, and charges.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SpellId` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `SchoolMask` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `SpellFamilyName` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `SpellFamilyMask0` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `SpellFamilyMask1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `SpellFamilyMask2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `SpellFamilyMask3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `ProcFlags` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `ProcFlags2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `SpellTypeMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `SpellPhaseMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `HitMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `AttributesMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `DisableEffectsMask` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 15 | `ProcsPerMinute` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 16 | `Chance` | `float` | NO | `0` | — | — | Selection chance; units and zero behavior depend on the table (see loot/profession guide). |
| 17 | `Cooldown` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 18 | `Charges` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SpellId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:1504](../../../src/server/game/Spells/SpellMgr.cpp#L1504)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SpellId` | `int32 spellId = fields[0].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1515) |
| `SchoolMask` | `baseProcEntry.SchoolMask         = fields[1].GetUInt8()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1545) |
| `SpellFamilyName` | `baseProcEntry.SpellFamilyName    = fields[2].GetUInt16()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1546) |
| `SpellFamilyMask0` | `baseProcEntry.SpellFamilyMask[0] = fields[3].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1547) |
| `SpellFamilyMask1` | `baseProcEntry.SpellFamilyMask[1] = fields[4].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1548) |
| `SpellFamilyMask2` | `baseProcEntry.SpellFamilyMask[2] = fields[5].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1549) |
| `SpellFamilyMask3` | `baseProcEntry.SpellFamilyMask[3] = fields[6].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1550) |
| `ProcFlags` | `baseProcEntry.ProcFlags[0]       = fields[7].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1551) |
| `ProcFlags2` | `baseProcEntry.ProcFlags[1]       = fields[8].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1552) |
| `SpellTypeMask` | `baseProcEntry.SpellTypeMask      = ProcFlagsSpellType(fields[9].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1553) |
| `SpellPhaseMask` | `baseProcEntry.SpellPhaseMask     = ProcFlagsSpellPhase(fields[10].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1554) |
| `HitMask` | `baseProcEntry.HitMask            = ProcFlagsHit(fields[11].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1555) |
| `AttributesMask` | `baseProcEntry.AttributesMask     = ProcAttributes(fields[12].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1556) |
| `DisableEffectsMask` | `baseProcEntry.DisableEffectsMask = fields[13].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1557) |
| `ProcsPerMinute` | `baseProcEntry.ProcsPerMinute     = fields[14].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1558) |
| `Chance` | `baseProcEntry.Chance             = fields[15].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1559) |
| `Cooldown` | `baseProcEntry.Cooldown           = Milliseconds(fields[16].GetUInt32())` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1560) |
| `Charges` | `baseProcEntry.Charges            = fields[17].GetUInt8()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1561) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_proc` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_proc) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
