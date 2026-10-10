# trainer_spell

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Spells offered by trainers, costs, and prerequisite skills/spells/levels.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `TrainerId` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [trainer.Id](trainer.md). Spells available from trainer. |
| 2 | `SpellId` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `MoneyCost` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `ReqSkillLine` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ReqSkillRank` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `ReqAbility1` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `ReqAbility2` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `ReqAbility3` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `ReqLevel` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `TrainerId`, `SpellId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [trainer_spell](trainer_spell.md).`TrainerId` → [trainer](trainer.md).`Id`: Spells available from trainer.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:9257](../../../src/server/game/Globals/ObjectMgr.cpp#L9257)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `TrainerId` | `uint32 trainerId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9264) |
| `SpellId` | `spell.SpellId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9265) |
| `MoneyCost` | `spell.MoneyCost = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9266) |
| `ReqSkillLine` | `spell.ReqSkillLine = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9267) |
| `ReqSkillRank` | `spell.ReqSkillRank = fields[4].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9268) |
| `ReqAbility1` | `spell.ReqAbility[0] = fields[5].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9269) |
| `ReqAbility2` | `spell.ReqAbility[1] = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9270) |
| `ReqAbility3` | `spell.ReqAbility[2] = fields[7].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9271) |
| `ReqLevel` | `spell.ReqLevel = fields[8].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L9272) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `trainer_spell` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/trainer_spell) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
