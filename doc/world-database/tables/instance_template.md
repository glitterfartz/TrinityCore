# instance_template

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Instance map parent relationships and compiled instance scripts.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `map` | `smallint unsigned` | NO | NULL / absent; see conventions | PRI | — | Client Map record identifier; a map ID is distinct from an instance save ID. |
| 2 | `parent` | `smallint unsigned` | NO | NULL / absent; see conventions | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |
| 3 | `script` | `varchar(128)` | NO | `''` | — | — | Runtime field mapping is shown below; special values and validation are governed by that loader. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `map` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

Source sites are captured from this checkout. SQL references establish usage, not every semantic rule. Review validation around each loader when changing values.

- [src/server/game/Globals/ObjectMgr.cpp:6187](../../../src/server/game/Globals/ObjectMgr.cpp#L6187)

### Selected column mappings

These are extracted assignments from nearby loader code. They show the runtime destination and conversion, not a complete behavioral specification.

| Column | C++ assignment / conversion | Source |
| --- | --- | --- |
| `map` | `uint16 mapID = fields[0].GetUInt16()` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6200) |
| `parent` | `instanceTemplate.Parent     = uint32(fields[1].GetUInt16())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6210) |
| `script` | `instanceTemplate.ScriptId   = GetScriptId(fields[2].GetStringView())` | [loader](../../../src/server/game/Globals/ObjectMgr.cpp#L6211) |

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `instance_template` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/instance_template) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
