# vw_disables_with_labels

[All tables](../README.md#table-index) · [Conventions](../conventions.md) · [Relationships](../relationships.md)

Custom diagnostic view replacing disable source numbers with labels.

## Schema

Captured 2026-10-09 from TDB 1210.26091, core 914a6f655c97. Object type: **VIEW**. Engine: not applicable. Collation: not applicable.

Database comment: VIEW

| # | Column | SQL type | Nullable | Default metadata | Key | Extra | Meaning / evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `sourceType` | `varchar(33)` | NO | `''` | — | — | Projected/derived view output; see the view definition and caveats below. |
| 2 | `entry` | `int unsigned` | NO | NULL / absent; see conventions | — | — | Projected/derived view output; see the view definition and caveats below. |
| 3 | `flags` | `smallint` | NO | NULL / absent; see conventions | — | — | Projected/derived view output; see the view definition and caveats below. |
| 4 | `params_0` | `varchar(255)` | NO | `''` | — | — | Projected/derived view output; see the view definition and caveats below. |
| 5 | `params_1` | `varchar(255)` | NO | `''` | — | — | Projected/derived view output; see the view definition and caveats below. |
| 6 | `comment` | `varchar(255)` | NO | `''` | — | — | Projected/derived view output; see the view definition and caveats below. |

## Keys and indexes

No indexes were reported in information_schema for this object.

## Relationships

No database-enforced foreign keys were reported. The associations below are logical relationships maintained by data authors and validated by core loaders.

No unambiguous world-to-world association has been established here. Client DB2/hotfix references and typed polymorphic relationships may still exist.

## Runtime evidence

No literal SQL usage site was found by the source scan. Dynamic SQL, generic loaders, SQL-only helper objects, or unused/legacy data can explain this. Presence in the schema does not prove active runtime consumption.

## View definition and caveats

Security mode: DEFINER. MySQL reports updatable: YES. Treat this as a diagnostic projection and edit the numeric base table deliberately. The definition is local database customization, not proof of an upstream standard view.

```sql
select (case when (`world`.`disables`.`sourceType` = 0) then 'DISABLE_TYPE_SPELL' when (`world`.`disables`.`sourceType` = 1) then 'DISABLE_TYPE_QUEST' when (`world`.`disables`.`sourceType` = 2) then 'DISABLE_TYPE_MAP' when (`world`.`disables`.`sourceType` = 3) then 'DISABLE_TYPE_BATTLEGROUND' when (`world`.`disables`.`sourceType` = 4) then 'DISABLE_TYPE_ACHIEVEMENT_CRITERIA' when (`world`.`disables`.`sourceType` = 5) then 'DISABLE_TYPE_OUTDOORPVP' when (`world`.`disables`.`sourceType` = 6) then 'DISABLE_TYPE_VMAP' when (`world`.`disables`.`sourceType` = 7) then 'DISABLE_TYPE_MMAP' when (`world`.`disables`.`sourceType` = 8) then 'DISABLE_TYPE_LFG_MAP' else `world`.`disables`.`sourceType` end) AS `sourceType`,`world`.`disables`.`entry` AS `entry`,`world`.`disables`.`flags` AS `flags`,`world`.`disables`.`params_0` AS `params_0`,`world`.`disables`.`params_1` AS `params_1`,`world`.`disables`.`comment` AS `comment` from `world`.`disables`
```

## Inspection example

This query is read-only. Substitute explicit identity filters before using data in an update.

```sql
SELECT * FROM `vw_disables_with_labels` LIMIT 5;
```

## Further reference

[Master wiki candidate page](https://trinitycore.info/database/master/world/vw_disables_with_labels) — linked for further investigation; availability and correctness were not individually verified. Live schema and this checkout take precedence over another branch's page.
