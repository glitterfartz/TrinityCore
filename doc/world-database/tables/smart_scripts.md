# smart_scripts

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Typed event/action/target programs for SmartAI and related script sources.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `entryorguid` | `bigint` | NO | `0` | PRI | — | Template/source entry or negative spawn GUID where supported by source_type. |
| 2 | `source_type` | `tinyint unsigned` | NO | `0` | PRI | — | SmartAI script owner category; see current SmartScriptType enum. |
| 3 | `id` | `smallint unsigned` | NO | `0` | PRI | — | Row identity within this table; use the complete primary key when selecting or editing. |
| 4 | `link` | `smallint unsigned` | NO | `0` | PRI | — | SmartAI linked row ID; linked execution uses SMART_EVENT_LINK. |
| 5 | `Difficulties` | `varchar(100)` | NO | `''` | — | — | Difficulty filter expressed as difficulty IDs; inspect SmartScriptMgr parsing for empty-list behavior. |
| 6 | `event_type` | `tinyint unsigned` | NO | `0` | — | — | SmartAI event enum; determines interpretation of event parameters. |
| 7 | `event_phase_mask` | `smallint unsigned` | NO | `0` | — | — | SmartAI internal phase bitmask; separate from world visibility phases. |
| 8 | `event_chance` | `tinyint unsigned` | NO | `100` | — | — | Probability of executing an eligible SmartAI event, in percent. |
| 9 | `event_flags` | `smallint unsigned` | NO | `0` | — | — | SmartAI event behavior flags; see SmartAI enum reference. |
| 10 | `event_param1` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 11 | `event_param2` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 12 | `event_param3` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 13 | `event_param4` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 14 | `event_param5` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 15 | `event_param_string` | `varchar(255)` | NO | `''` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 16 | `action_type` | `tinyint unsigned` | NO | `0` | — | — | SmartAI action enum; determines interpretation of action parameters. |
| 17 | `action_param1` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 18 | `action_param2` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 19 | `action_param3` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 20 | `action_param4` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 21 | `action_param5` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 22 | `action_param6` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 23 | `action_param7` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 24 | `action_param_string` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 25 | `target_type` | `tinyint unsigned` | NO | `0` | — | — | SmartAI target enum; determines interpretation of target parameters and coordinates. |
| 26 | `target_param1` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 27 | `target_param2` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 28 | `target_param3` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 29 | `target_param4` | `int unsigned` | NO | `0` | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 30 | `target_param_string` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Type-dependent operand; use the corresponding event/action/target row in [SmartAI enums](../reference/smartai-enums.md). |
| 31 | `target_x` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 32 | `target_y` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 33 | `target_z` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 34 | `target_o` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 35 | `comment` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `entryorguid`, `source_type`, `id`, `link` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/AI/SmartScripts/SmartScriptMgr.cpp:70](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L70)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:30](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L30)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `entryorguid` | `temp.entryOrGuid = fields[0].GetInt64()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L87) |
| `source_type` | `SmartScriptType source_type = (SmartScriptType)fields[1].GetUInt8()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L94) |
| `id` | `temp.event_id = fields[2].GetUInt16()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L254) |
| `link` | `temp.link = fields[3].GetUInt16()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L255) |
| `event_type` | `temp.event.type = (SMART_EVENT)fields[5].GetUInt8()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L284) |
| `event_phase_mask` | `temp.event.event_phase_mask = fields[6].GetUInt16()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L285) |
| `event_chance` | `temp.event.event_chance = fields[7].GetUInt8()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L286) |
| `event_flags` | `temp.event.event_flags = fields[8].GetUInt16()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L287) |
| `event_param1` | `temp.event.raw.param1 = fields[9].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L289) |
| `event_param2` | `temp.event.raw.param2 = fields[10].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L290) |
| `event_param3` | `temp.event.raw.param3 = fields[11].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L291) |
| `event_param4` | `temp.event.raw.param4 = fields[12].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L292) |
| `event_param5` | `temp.event.raw.param5 = fields[13].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L293) |
| `event_param_string` | `temp.event.param_string = fields[14].GetString()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L295) |
| `action_type` | `temp.action.type = (SMART_ACTION)fields[15].GetUInt8()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L297) |
| `action_param1` | `temp.action.raw.param1 = fields[16].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L298) |
| `action_param2` | `temp.action.raw.param2 = fields[17].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L299) |
| `action_param3` | `temp.action.raw.param3 = fields[18].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L300) |
| `action_param4` | `temp.action.raw.param4 = fields[19].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L301) |
| `action_param5` | `temp.action.raw.param5 = fields[20].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L302) |
| `action_param6` | `temp.action.raw.param6 = fields[21].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L303) |
| `action_param7` | `temp.action.raw.param7 = fields[22].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L304) |
| `action_param_string` | `temp.action.param_string = fields[23].GetString()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L305) |
| `target_type` | `temp.target.type = (SMARTAI_TARGETS)fields[24].GetUInt8()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L307) |
| `target_param1` | `temp.target.raw.param1 = fields[25].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L308) |
| `target_param2` | `temp.target.raw.param2 = fields[26].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L309) |
| `target_param3` | `temp.target.raw.param3 = fields[27].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L310) |
| `target_param4` | `temp.target.raw.param4 = fields[28].GetUInt32()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L311) |
| `target_param_string` | `temp.target.param_string = fields[29].GetString()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L312) |
| `target_x` | `temp.target.x = fields[30].GetFloat()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L313) |
| `target_y` | `temp.target.y = fields[31].GetFloat()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L314) |
| `target_z` | `temp.target.z = fields[32].GetFloat()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L315) |
| `target_o` | `temp.target.o = fields[33].GetFloat()` | [loader](../../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp#L316) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `smart_scripts` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/smart_scripts) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
