# conversation_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Conversation definitions, initial lines, texture kits, and script bindings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `Id` | `int unsigned` | NO | NULL / absent; see conventions | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `FirstLineId` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `TextureKitId` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Flags` | `tinyint` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 5 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |
| 6 | `VerifiedBuild` | `int unsigned` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `Id` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ConversationDataStore.cpp:231](../../../src/server/game/Globals/ConversationDataStore.cpp#L231)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `Id` | `conversationTemplate.Id                 = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ConversationDataStore.cpp#L240) |
| `FirstLineId` | `conversationTemplate.FirstLineId        = fields[1].GetUInt32()` | [loader](../../../src/server/game/Globals/ConversationDataStore.cpp#L241) |
| `TextureKitId` | `conversationTemplate.TextureKitId       = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ConversationDataStore.cpp#L242) |
| `Flags` | `conversationTemplate.Flags              = (ConversationFlags)fields[3].GetUInt8()` | [loader](../../../src/server/game/Globals/ConversationDataStore.cpp#L243) |
| `ScriptName` | `conversationTemplate.ScriptId           = sObjectMgr->GetScriptId(fields[4].GetStringView())` | [loader](../../../src/server/game/Globals/ConversationDataStore.cpp#L244) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `conversation_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/conversation_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
