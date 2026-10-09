# quest_template_addon

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Server-side prerequisites, chain relationships, skills, scripts, and other quest settings.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **BASE TABLE**. Engine: InnoDB. Collation: utf8mb4_unicode_ci.

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `ID` | `int unsigned` | NO | `0` | PRI | — | Record identifier; consult the complete primary key and relationships before treating it as a template ID. |
| 2 | `MaxLevel` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 3 | `AllowableClasses` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 4 | `SourceSpellID` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 5 | `PrevQuestID` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 6 | `NextQuestID` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 7 | `ExclusiveGroup` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 8 | `BreadcrumbForQuestId` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 9 | `RewardMailTemplateID` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 10 | `RewardMailDelay` | `int unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 11 | `RequiredSkillID` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 12 | `RequiredSkillPoints` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 13 | `RequiredMinRepFaction` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 14 | `RequiredMaxRepFaction` | `smallint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 15 | `RequiredMinRepValue` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 16 | `RequiredMaxRepValue` | `int` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 17 | `ProvidedItemCount` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 18 | `SpecialFlags` | `tinyint unsigned` | NO | `0` | — | — | **Meaning not independently established.** The schema confirms storage only; use the linked source sites to resolve behavior before editing. |
| 19 | `ScriptName` | `varchar(64)` | NO | `''` | — | — | Name of a compiled C++ script registered by this core. Text alone cannot create a script. |

## Keys and indexes

| Index | Unique | Ordered columns | Method |
| --- | --- | --- | --- |
| `PRIMARY` | Yes | `ID` | BTREE |

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `quest_template_addon` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/quest_template_addon) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
