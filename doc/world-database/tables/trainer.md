# trainer

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Trainer identity, category, requirements, and greeting.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Type` | `tinyint unsigned` | NO | `2` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Greeting` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [trainer_spell](trainer_spell.md).`TrainerId` → [trainer](trainer.md).`Id`: Spells available from trainer.
- [trainer_locale](trainer_locale.md).`Id` → [trainer](trainer.md).`Id`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9308](../../../src/server/game/Globals/ObjectMgr.cpp#L9308)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `uint32 trainerId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9313) |
| `Type` | `Trainer::Type trainerType = Trainer::Type(fields[1].GetUInt8())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9314) |
| `Greeting` | `std::string_view greeting = fields[2].GetStringView()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9315) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `trainer` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/trainer) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
