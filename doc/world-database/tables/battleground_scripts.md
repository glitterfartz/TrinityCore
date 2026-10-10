# battleground_scripts

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Compiled script bindings for battleground types.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `MapId` | `int` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `BattlemasterListId` | `int` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `MapId`, `BattlemasterListId` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Battlegrounds/BattlegroundMgr.cpp:259](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L259)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `MapId` | `uint32 mapID = fields[0].GetUInt32()` | [loader](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L272) |
| `BattlemasterListId` | `BattlegroundTypeId bgTypeId = static_cast<BattlegroundTypeId>(fields[1].GetUInt32())` | [loader](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L281) |
| `ScriptName` | `scriptTemplate.ScriptId = sObjectMgr->GetScriptId(fields[2].GetStringView())` | [loader](../../../src/server/game/Battlegrounds/BattlegroundMgr.cpp#L291) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `battleground_scripts` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/battleground_scripts) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
