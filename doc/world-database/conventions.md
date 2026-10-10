# Conventions and version scope

[Database documentation](README.md)

## What this database contains

World is content configuration: creature and object definitions, spawns, quests, scripted behavior, loot, navigation, and server rules. Account identity belongs to auth; persistent player progress belongs to characters. Modern master also consumes client DB2 and hotfix data. A missing world item_template table does not mean items do not exist.

This reference applies to master revision 914a6f655c97 and TDB 1210.26091 captured on 2026-10-09. Do not copy SQL or enum values from 3.3.5 documentation without comparing this schema and core. Notable current features include creature_template_difficulty, separate waypoint_path/waypoint_path_node tables, typed loot ItemType, spawnDifficulties lists, additional SmartAI string operands and action_param7, and modern quest housing rewards.

## Evidence order

1. Captured information_schema establishes the installed storage structure.
2. The inspected local C++ loader and runtime implementation establish how the server consumes it.
3. Verified client data establishes external DB2 identifiers and packet-related values.
4. The master wiki supplies background and additional interpretation; pages may lag the core.
5. A name-based editorial association is a navigation aid, not a foreign-key constraint.

Schema coverage is complete for the captured objects. Semantic coverage is explicitly qualified: fields without a reliable interpretation are marked unresolved. Do not infer acceptable values solely from SQL range or existing data.

## Identities and references

A template entry identifies a reusable definition. A spawn GUID identifies one persistent placement. Runtime GUIDs include additional context and are not interchangeable with either. Many tables use composite keys; include every identity component when editing. A nonunique index accelerates lookup but does not impose uniqueness.

No enforced world foreign keys were reported. Loaders may reject, skip, substitute, or log invalid references. A successful SQL INSERT is therefore insufficient evidence that gameplay data works.

## SQL metadata

Types include widths and unsigned attributes exactly as information_schema reports them. YES in Nullable means SQL NULL is permitted. It does not mean NULL behaves like zero.

COLUMN_DEFAULT is metadata, not original DDL text. A null metadata value may mean a SQL NULL default or no explicit default. Use SHOW CREATE TABLE when this distinction matters; the pages intentionally avoid guessing. An empty string default is shown as ''. PRI/MUL/UNI is the column-level metadata abbreviation; the complete index section is authoritative for composite keys and uniqueness.

View column metadata describes projected output, not independent stored rows. A MySQL updatable flag does not guarantee every derived column can be changed through the view.

## Units, masks, and sentinels

World coordinates are map-local coordinates; orientation is normally radians. A UI-map coordinate need not use the same space. Quaternion rotation components on gameobjects must form the intended rotation, not arbitrary angles.

Time units vary. Spawn respawn time is seconds; SmartAI update/cooldown timers generally use milliseconds; waypoint delays and gameobject-specific fields must be checked in their respective runtime consumers. Source comments are reproduced in the references where available.

A bitmask combines named flag bits. An ordinary enum selects a value. Comma-separated difficulty IDs are neither of those. Never treat 0, -1, an empty string, and NULL as interchangeable: each table's loader defines their meaning.

VerifiedBuild records provenance; it does not choose the server's active client build. Preserve signed provenance conventions when retaining source data.

## Examples

Inspection SQL is read-only and bounded. Placeholder values such as @creature_entry and @quest_id must be set to relevant existing identifiers. Diagnostic joins are examples, not exhaustive integrity checks. DML examples describe a reviewable workflow and were not executed against the connected database.
