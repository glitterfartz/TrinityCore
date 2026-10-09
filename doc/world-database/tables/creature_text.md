# creature_text

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Groups of NPC speech lines, probabilities, emotes, sounds, and broadcast-text references.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `CreatureID` | `int unsigned` | NO | `0` | PRI | — | Logical reference to [creature_template.entry](creature_template.md). Creature template identity, not spawn GUID. |
| 2 | `GroupID` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `ID` | `tinyint unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `Text` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Type` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `Language` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 7 | `Probability` | `float` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 8 | `Emote` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 9 | `Duration` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 10 | `Sound` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 11 | `SoundPlayType` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 12 | `BroadcastTextId` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 13 | `TextRange` | `tinyint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 14 | `comment` | `varchar(255)` | YES | `''` | — | — | Authoring/provenance note; do not use it as a gameplay identifier. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `CreatureID`, `GroupID`, `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [creature_text](creature_text.md).`CreatureID` → [creature_template](creature_template.md).`entry`: Creature template identity, not spawn GUID.
- [creature_text_locale](creature_text_locale.md).`GroupID` → [creature_text](creature_text.md).`GroupID`: Translation parent identity; include all identity components plus locale.
- [creature_text_locale](creature_text_locale.md).`ID` → [creature_text](creature_text.md).`ID`: Translation parent identity; include all identity components plus locale.
- [creature_text_locale](creature_text_locale.md).`CreatureID` → [creature_text](creature_text.md).`CreatureID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Texts/CreatureTextMgr.cpp:50](../../../src/server/game/Texts/CreatureTextMgr.cpp#L50)
- [src/server/database/Database/Implementation/WorldDatabase.cpp:29](../../../src/server/database/Database/Implementation/WorldDatabase.cpp#L29)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `CreatureID` | `temp.creatureId      = fields[0].GetUInt32()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L67) |
| `GroupID` | `temp.groupId         = fields[1].GetUInt8()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L68) |
| `ID` | `temp.id              = fields[2].GetUInt8()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L69) |
| `Text` | `temp.text            = fields[3].GetString()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L70) |
| `Type` | `temp.type            = ChatMsg(fields[4].GetUInt8())` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L71) |
| `Language` | `temp.lang            = Language(fields[5].GetUInt8())` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L72) |
| `Probability` | `temp.probability     = fields[6].GetFloat()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L73) |
| `Emote` | `temp.emote           = Emote(fields[7].GetUInt32())` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L74) |
| `Duration` | `temp.duration        = fields[8].GetUInt32()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L75) |
| `Sound` | `temp.sound           = fields[9].GetUInt32()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L76) |
| `SoundPlayType` | `temp.SoundPlayType   = SoundKitPlayType(fields[10].GetUInt8())` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L77) |
| `BroadcastTextId` | `temp.BroadcastTextId = fields[11].GetUInt32()` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L78) |
| `TextRange` | `temp.TextRange       = CreatureTextRange(fields[12].GetUInt8())` | [loader](../../../src/server/game/Texts/CreatureTextMgr.cpp#L79) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `creature_text` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/creature_text) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
