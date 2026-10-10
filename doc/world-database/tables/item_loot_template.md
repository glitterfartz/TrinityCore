# item_loot_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Loot rows for item sources. Shared typed reward, probability, mode, grouping, and count fields are described in the loot guide.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Loot System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Entry` | `int unsigned` | NO | `0` | MUL | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `ItemType` | `tinyint` | NO | `0` | — | — | LootStoreItem::Type: 0 item, 1 reference, 2 currency, 3 tracking quest. See the loot guide for type-specific count rules. |
| 3 | `Item` | `int unsigned` | NO | `0` | — | — | Typed reward identifier; interpretation follows ItemType, including reference entries. |
| 4 | `Chance` | `float` | NO | `100` | — | — | Selection chance; units and zero behavior depend on the table (see loot/profession guide). |
| 5 | `QuestRequired` | `tinyint(1)` | NO | `0` | — | — | Loot reward is restricted to qualifying quest needs. |
| 6 | `LootMode` | `smallint unsigned` | NO | `1` | — | — | Loot-mode bitmask controlling eligibility. |
| 7 | `GroupId` | `tinyint unsigned` | NO | `0` | — | — | Loot roll group; group zero and nonzero groups use different selection rules. |
| 8 | `MinCount` | `tinyint unsigned` | NO | `1` | — | — | Type-dependent count. Item/currency use a positive minimum; tracking quest requires 1. See loot guide. |
| 9 | `MaxCount` | `tinyint unsigned` | NO | `1` | — | — | Type-dependent count. Item/currency require at least MinCount; tracking quest requires 0. References use repeat semantics. See loot guide. |
| 10 | `Comment` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `idx_primary` | No | `Entry`, `ItemType`, `Item` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/AuctionHouseBot/AuctionHouseBotSeller.cpp:78](../../../src/server/game/AuctionHouseBot/AuctionHouseBotSeller.cpp#L78)
- [src/server/game/Loot/LootMgr.cpp:144](../../../src/server/game/Loot/LootMgr.cpp#L144)
- [src/server/game/Loot/LootMgr.cpp:155](../../../src/server/game/Loot/LootMgr.cpp#L155)
- [src/server/game/Loot/LootMgr.cpp:285](../../../src/server/game/Loot/LootMgr.cpp#L285)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Entry` | `uint32 entry               = fields[0].GetUInt32()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L155) |
| `ItemType` | `LootStoreItem::Type type   = static_cast<LootStoreItem::Type>(fields[1].GetInt8())` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L156) |
| `Item` | `uint32 item                = fields[2].GetUInt32()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L157) |
| `Chance` | `float  chance              = fields[3].GetFloat()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L158) |
| `QuestRequired` | `bool   needsquest          = fields[4].GetBool()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L159) |
| `LootMode` | `uint16 lootmode            = fields[5].GetUInt16()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L160) |
| `GroupId` | `uint8  groupid             = fields[6].GetUInt8()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L161) |
| `MinCount` | `uint8  mincount            = fields[7].GetUInt8()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L162) |
| `MaxCount` | `uint8  maxcount            = fields[8].GetUInt8()` | [loader](../../../src/server/game/Loot/LootMgr.cpp#L163) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `item_loot_template` LIMIT 5;
```

See [loot](../guides/loot.md) for typed rewards, roll groups, and reference relationships.

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/item_loot_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
