# quest_greeting

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Creature/gameobject quest greeting text and emotes.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Type` | `tinyint unsigned` | NO | `0` | PRI | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `GreetEmoteType` | `smallint unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 4 | `GreetEmoteDelay` | `int unsigned` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Greeting` | `mediumtext` | YES | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 6 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID`, `Type` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [quest_greeting_locale](quest_greeting_locale.md).`ID` → [quest_greeting](quest_greeting.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:6530](../../../src/server/game/Globals/ObjectMgr.cpp#L6530)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id                   = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6542) |
| `GreetEmoteType` | `uint16 greetEmoteType       = fields[2].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6564) |
| `GreetEmoteDelay` | `uint32 greetEmoteDelay      = fields[3].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6565) |
| `Greeting` | `std::string greeting        = fields[4].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6566) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_greeting` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_greeting) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
