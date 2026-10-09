# character_template_class

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Race, faction, and class combinations for character presets.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `TemplateId` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `FactionGroup` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Database comment: 3 - Alliance, 5 - Horde |
| 3 | `Class` | `tinyint unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `TemplateId`, `FactionGroup`, `Class` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/CharacterTemplateDataStore.cpp:36](../../../src/server/game/Globals/CharacterTemplateDataStore.cpp#L36)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `TemplateId` | `uint32 templateId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/CharacterTemplateDataStore.cpp#L42) |
| `FactionGroup` | `uint8 factionGroup = fields[1].GetUInt8()` | [loader](../../../src/server/game/Globals/CharacterTemplateDataStore.cpp#L43) |
| `Class` | `uint8 classID = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/CharacterTemplateDataStore.cpp#L44) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `character_template_class` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/character_template_class) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
