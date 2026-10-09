# world_state

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server world-state defaults and configuration.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `DefaultValue` | `int` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `MapIDs` | `varchar(128)` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `AreaIDs` | `varchar(255)` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 6 | `Comment` | `text` | YES | NULL / absent; see conventions | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/World/WorldStates/WorldStateMgr.cpp:56](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L56)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `int32 id = fields[0].GetInt32()` | [loader](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L66) |
| `DefaultValue` | `worldState.DefaultValue = fields[1].GetInt32()` | [loader](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L69) |
| `MapIDs` | `std::string_view mapIds = fields[2].GetStringView()` | [loader](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L71) |
| `AreaIDs` | `std::string_view areaIds = fields[3].GetStringView()` | [loader](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L99) |
| `ScriptName` | `worldState.ScriptId = sObjectMgr->GetScriptId(fields[4].GetStringView())` | [loader](../../../src/server/game/World/WorldStates/WorldStateMgr.cpp#L143) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `world_state` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/world_state) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
