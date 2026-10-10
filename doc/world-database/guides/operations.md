# Operations and troubleshooting

[Database documentation](../README.md)

## Version and migrations

version records core/database/cache identity. updates records applied migration names, hashes, states, timestamps, and speeds. updates_include selects migration directories and states. These are updater bookkeeping, not ordinary gameplay customization tables.

The [official installation guide](https://trinitycore.info/en/install/Database-Installation) describes database roles and automatic updates. Use the updater supplied with the matching core. Do not manually mark a migration applied to suppress a schema error.

```sql
SELECT * FROM version;
SELECT * FROM updates ORDER BY timestamp DESC LIMIT 20;
SELECT * FROM updates_include;
```

Version metadata is a starting point; inspect applied migrations and actual schema when investigating drift.

## Reviewable content changes

1. Export a recoverable backup or work in a separate test database.
2. Inspect the existing row and every related template/spawn/source record.
3. Write a narrowly scoped migration using explicit column names and complete identity filters.
4. Review expected before/after values and referential effects.
5. Apply it to the test database and review startup sql.sql diagnostics.
6. Exercise the relevant gameplay path and record expected/observed behavior.
7. Retain the migration and rollback information in the repository's appropriate SQL workflow.

Use a transaction when the involved tables' engines support it. DDL has its own commit behavior, and transactions do not replace backups. Avoid broad DELETE/UPDATE predicates and implicit column-order INSERT statements.

No database mutation was performed while creating this documentation.

## Reloads and caches

Some world tables support targeted reload commands; others are consumed at startup or cached across systems. Confirm available reload behavior in this checkout's command scripts. A reload command should not be assumed to reconstruct every dependent cache, instance object, or active script.

When behavior is uncertain, test with a clean worldserver restart in a controlled environment. Client caches and locale/broadcast-text paths can also affect observed presentation.

## Diagnostics

| Symptom | First areas to inspect |
| --- | --- |
| Startup SQL column error | Core revision, applied migrations, captured versus expected schema |
| Row loads but does not appear | Map/difficulty, phase, event/pool, spawn group, instance state, disables |
| Interaction missing | NPC/object flags, menu/trainer/vendor association, conditions, registered scripts |
| SmartAI action does not run | AI selection, owner/source, event flags/phase/difficulty, target, operands |
| Quest unavailable | Source relations, race/skill/level/tuning, prerequisites, conditions, event/pool |
| Quest progress absent | Objective Type/ObjectID/storage, credit script, required item/currency |
| Loot missing | Correct source entry, ItemType, group/mode, quest eligibility, references |
| Movement broken | Path/addon precedence, movement type/capabilities, nodes, terrain |
| Text unexpected | Active broadcast-text source, locale, fallback, client cache |
| Labels misleading | Custom label-view CASE definitions versus current enums |

## Integrity checks

The guide queries deliberately check individual associations or simple invariants. Comprehensive integrity is type-dependent and spans client/hotfix data and compiled scripts. Do not automatically delete “orphans” reported by naive joins on signed, polymorphic, or sentinel fields.

Check command, disables, world_state, game_weather, game_tele, graveyard_zone, world_safe_locs, and access_requirement when a broader world rule seems responsible. Distinguish content definitions from persistent player/instance state in characters.
