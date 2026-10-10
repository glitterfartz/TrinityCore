# spell_threat

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spell threat additions, multipliers, and attack-power scaling.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entry` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `flatMod` | `int` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `pctMod` | `float` | NO | `1` | — | — | Database comment: threat multiplier for damage/healing |
| 4 | `apPctMod` | `float` | NO | `0` | — | — | Database comment: additional threat bonus from attack power |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entry` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Spells/SpellMgr.cpp:1920](../../../src/server/game/Spells/SpellMgr.cpp#L1920)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entry` | `uint32 entry = fields[0].GetUInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1932) |
| `flatMod` | `ste.flatMod  = fields[1].GetInt32()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1941) |
| `pctMod` | `ste.pctMod   = fields[2].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1942) |
| `apPctMod` | `ste.apPctMod = fields[3].GetFloat()` | [loader](../../../src/server/game/Spells/SpellMgr.cpp#L1943) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `spell_threat` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/spell_threat) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
