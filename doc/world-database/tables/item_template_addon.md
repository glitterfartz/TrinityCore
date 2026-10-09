# item_template_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server-only item behavior supplementing client/hotfix item definitions.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `FlagsCu` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `FoodType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `MinMoneyLoot` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `MaxMoneyLoot` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `SpellPPMChance` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `RandomBonusListTemplateId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `QuestLogItemId` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:3388](../../../src/server/game/Globals/ObjectMgr.cpp#L3388)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `uint32 itemId = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3394) |
| `FlagsCu` | `itemTemplate->FlagsCu = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3409) |
| `FoodType` | `itemTemplate->FoodType = fields[2].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3410) |
| `MinMoneyLoot` | `uint32 minMoneyLoot = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3402) |
| `MaxMoneyLoot` | `uint32 maxMoneyLoot = fields[4].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3403) |
| `SpellPPMChance` | `itemTemplate->SpellPPMRate = fields[5].GetFloat()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3413) |
| `RandomBonusListTemplateId` | `itemTemplate->RandomBonusListTemplateId = fields[6].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3414) |
| `QuestLogItemId` | `itemTemplate->QuestLogItemId = fields[7].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L3415) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `item_template_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/item_template_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
