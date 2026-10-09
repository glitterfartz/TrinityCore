# Zone scripting guides

These guides explain how players move through a zone and how the world database, server scripts, and client data work together. They describe the installed implementation rather than assuming that a retail walkthrough proves server functionality.

| Zone | Guide | Audit scope |
| --- | --- | --- |
| Exile's Reach | [Overview and implementation status](exiles-reach.md) | Source inventory, with a detailed database audit of the opening |
| Exile's Reach | [From the ship to the beach](exiles-reach-ship-to-beach.md) | Character creation, scenes, Jaina/Thrall, training quests, crash callbacks |
| Exile's Reach | [Validation and troubleshooting](exiles-reach-validation.md) | Known gaps, read-only queries, and in-game acceptance tests |

Snapshot: 2026-10-09, core revision `914a6f655c97`, world database `TDB 1210.26091`. See the [world database reference](../world-database/README.md) for individual tables and the [quest hub](../world-database/guides/quests.md) for authoring quests.
