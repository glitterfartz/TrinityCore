# item_random_bonus_list_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Weighted item bonus-list selections.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Item Random Enchantment System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `BonusListID` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `Chance` | `float` | NO | NULL / absent; see conventions | — | — | Selection chance; units and zero behavior depend on the table (see loot/profession guide). |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id`, `BonusListID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Entities/Item/ItemEnchantmentMgr.cpp:48](../../../src/server/game/Entities/Item/ItemEnchantmentMgr.cpp#L48)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `uint32 id = fields[0].GetUInt32()` | [loader](../../../src/server/game/Entities/Item/ItemEnchantmentMgr.cpp#L58) |
| `BonusListID` | `uint32 bonusListId = fields[1].GetUInt32()` | [loader](../../../src/server/game/Entities/Item/ItemEnchantmentMgr.cpp#L59) |
| `Chance` | `float chance = fields[2].GetFloat()` | [loader](../../../src/server/game/Entities/Item/ItemEnchantmentMgr.cpp#L60) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `item_random_bonus_list_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/item_random_bonus_list_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
