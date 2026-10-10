# page_text

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Chained readable pages used by items and other content.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

Database comment: Item System

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 2 | `Text` | `mediumtext` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `NextPageID` | `int unsigned` | NO | `0` | — | — | Logical reference to [page_text.ID](page_text.md). Next readable page; prevent cycles. |
| 4 | `PlayerConditionID` | `int` | NO | `0` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 5 | `Flags` | `tinyint unsigned` | NO | `0` | — | — | Flags interpreted by the owning subsystem; use the linked enum source, not another table's flag constants. |
| 6 | `VerifiedBuild` | `int` | NO | `0` | — | — | Client-build provenance supplied by the data author; not an activation switch. Keep existing signed values until their provenance is understood. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

- [page_text](page_text.md).`NextPageID` → [page_text](page_text.md).`ID`: Next readable page; prevent cycles.
- [page_text_locale](page_text_locale.md).`ID` → [page_text](page_text.md).`ID`: Translation parent identity; include all identity components plus locale.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:6112](../../../src/server/game/Globals/ObjectMgr.cpp#L6112)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `ID` | `uint32 id           = fields[0].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6124) |
| `Text` | `pageText.Text       = fields[1].GetString()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6127) |
| `NextPageID` | `pageText.NextPageID = fields[2].GetUInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6128) |
| `PlayerConditionID` | `pageText.PlayerConditionID = fields[3].GetInt32()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6129) |
| `Flags` | `pageText.Flags = fields[4].GetUInt8()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6130) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `page_text` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/page_text) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
