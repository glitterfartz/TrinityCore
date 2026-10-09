# conditions

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Reusable typed predicates that gate spells, gossip, loot, quests, spawns, and other content.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Condition System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `SourceTypeOrReferenceId` | `int` | NO | `0` | PRI | — | Nonnegative source enum, or negative ID defining a reusable reference template. |
| 2 | `SourceGroup` | `int unsigned` | NO | `0` | PRI | — | Source-specific group selector; interpretation depends on source type. |
| 3 | `SourceEntry` | `int` | NO | `0` | PRI | — | Source-specific entry selector; interpretation depends on source type. |
| 4 | `SourceId` | `int` | NO | `0` | PRI | — | Additional source-specific identifier; interpretation depends on source type. |
| 5 | `ElseGroup` | `int unsigned` | NO | `0` | PRI | — | Conditions within an ElseGroup are ANDed; distinct groups provide OR alternatives. |
| 6 | `ConditionTypeOrReference` | `int` | NO | `0` | PRI | — | Nonnegative condition enum, or negative reusable condition-reference ID. |
| 7 | `ConditionTarget` | `tinyint unsigned` | NO | `0` | PRI | — | Target slot to evaluate; available slots depend on the source type. |
| 8 | `ConditionValue1` | `int unsigned` | NO | `0` | PRI | — | Typed predicate operand; exact layout is documented in [condition enums](../reference/conditions-enums.md) and ConditionMgr.cpp. |
| 9 | `ConditionValue2` | `int unsigned` | NO | `0` | PRI | — | Typed predicate operand; exact layout is documented in [condition enums](../reference/conditions-enums.md) and ConditionMgr.cpp. |
| 10 | `ConditionValue3` | `int unsigned` | NO | `0` | PRI | — | Typed predicate operand; exact layout is documented in [condition enums](../reference/conditions-enums.md) and ConditionMgr.cpp. |
| 11 | `ConditionStringValue1` | `varchar(64)` | NO | `''` | PRI | — | String operand used by condition types such as String ID. |
| 12 | `NegativeCondition` | `tinyint unsigned` | NO | `0` | — | — | Negates the predicate when nonzero. |
| 13 | `ErrorType` | `int unsigned` | NO | `0` | — | — | Condition failure error category; supported by only applicable source types. |
| 14 | `ErrorTextId` | `int unsigned` | NO | `0` | — | — | Client error-text identifier used when the source supports reporting failures. |
| 15 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 16 | `Comment` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `SourceTypeOrReferenceId`, `SourceGroup`, `SourceEntry`, `SourceId`, `ElseGroup`, `ConditionTypeOrReference`, `ConditionTarget`, `ConditionValue1`, `ConditionValue2`, `ConditionValue3`, `ConditionStringValue1` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Conditions/ConditionMgr.cpp:1339](../../../src/server/game/Conditions/ConditionMgr.cpp#L1339)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:82](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L82)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `SourceTypeOrReferenceId` | `int32 iSourceTypeOrReferenceId  = fields[0].GetInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1364) |
| `SourceGroup` | `cond.SourceGroup               = fields[1].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1365) |
| `SourceEntry` | `cond.SourceEntry               = fields[2].GetInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1366) |
| `SourceId` | `cond.SourceId                  = fields[3].GetInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1367) |
| `ElseGroup` | `cond.ElseGroup                 = fields[4].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1368) |
| `ConditionTypeOrReference` | `int32 iConditionTypeOrReference = fields[5].GetInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1369) |
| `ConditionTarget` | `cond.ConditionTarget           = fields[6].GetUInt8()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1370) |
| `ConditionValue1` | `cond.ConditionValue1           = fields[7].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1371) |
| `ConditionValue2` | `cond.ConditionValue2           = fields[8].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1372) |
| `ConditionValue3` | `cond.ConditionValue3           = fields[9].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1373) |
| `ConditionStringValue1` | `cond.ConditionStringValue1     = fields[10].GetString()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1374) |
| `NegativeCondition` | `cond.NegativeCondition         = fields[11].GetBool()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1375) |
| `ErrorType` | `cond.ErrorType                 = fields[12].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1376) |
| `ErrorTextId` | `cond.ErrorTextId               = fields[13].GetUInt32()` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1377) |
| `ScriptName` | `cond.ScriptId                  = sObjectMgr->GetScriptId(fields[14].GetStringView())` | [loader](../../../src/server/game/Conditions/ConditionMgr.cpp#L1378) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `conditions` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/conditions) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
