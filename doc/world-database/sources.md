# Sources and evidence limits

[Database documentation](README.md)

## Primary evidence

The live MySQL MCP connection selected database world. Read-only metadata queries inspected TABLES, COLUMNS, STATISTICS, KEY_COLUMN_USAGE, and VIEWS in information_schema restricted to DATABASE(), plus the version row. The snapshot contains no credentials and no gameplay row dump.

The inspected checkout is 914a6f655c973d57c392ae78c92c14c5376f8e38. Its revision matches version.core_revision. Local loaders and definitions are linked from each table page.

Important entry points:

- [ObjectMgr.cpp](../../src/server/game/Globals/ObjectMgr.cpp): creature, gameobject, quest, NPC, and many world-content loaders.
- [WorldDatabase.cpp](../../src/server/database/Database/Implementation/WorldDatabase.cpp): prepared SQL statements.
- [ConditionMgr.cpp](../../src/server/game/Conditions/ConditionMgr.cpp) and [ConditionMgr.h](../../src/server/game/Conditions/ConditionMgr.h): condition validation, evaluation, source definitions, and operand comments.
- [SmartScriptMgr.h](../../src/server/game/AI/SmartScripts/SmartScriptMgr.h), [SmartScriptMgr.cpp](../../src/server/game/AI/SmartScripts/SmartScriptMgr.cpp), and [SmartScript.cpp](../../src/server/game/AI/SmartScripts/SmartScript.cpp): SmartAI enums, load-time validation, and execution.
- [LootMgr.cpp](../../src/server/game/Loot/LootMgr.cpp) and [LootMgr.h](../../src/server/game/Loot/LootMgr.h): typed rewards, rolls, groups, modes, and generic loot loading.
- [QuestDef.h](../../src/server/game/Quests/QuestDef.h): quest and objective enums.
- [GameObjectData.h](../../src/server/game/Entities/GameObject/GameObjectData.h): type-dependent Data slot layouts.

The generated table pages contain selected direct column-to-field assignments and SQL usage links extracted from the local source. Generic or concatenated queries may not produce a per-table mapping. An assignment is evidence of a runtime destination, not proof of all downstream behavior. Enum extraction preserves local source comments; comments can still be incomplete.

Local source excerpts remain subject to the repository's licensing; see [COPYING](../../COPYING) and [AUTHORS](../../AUTHORS).

## Wiki research

These pages were accessed as supplementary references on 2026-10-09:

- [TrinityCore wiki home](https://trinitycore.info/): branch and documentation navigation.
- [Master world index](https://trinitycore.info/database/master/world/home): master table navigation.
- [Master conditions](https://trinitycore.info/database/master/world/conditions): condition reference navigation.
- [Master smart_scripts](https://trinitycore.info/database/master/world/smart_scripts): SmartAI reference navigation.
- [Master creature_loot_template](https://trinitycore.info/database/master/world/creature_loot_template): sparse legacy page; insufficient for the current typed loot schema.
- [Database installation](https://trinitycore.info/en/install/Database-Installation): database roles and updater overview.
- [3.3.5 world index](https://trinitycore.info/database/335/world/home): comparison only; its branch differs from this installation.

No wiki article is copied wholesale. The detailed enums and gameobject layouts come from the local repository. Per-table wiki links are candidate follow-up pages, not claims that every page was reviewed or exists.

## Confirmed local differences

The database includes three diagnostic label views. These are documented as local objects; they are not assumed to be upstream standard schema.

vw_conditions_with_labels contains a CASE expression that labels ConditionTypeOrReference using comparisons to SourceTypeOrReferenceId. That is a definition error, not just an uncertain interpretation. It also omits ConditionStringValue1. vw_smart_scripts_with_labels contains older enum labels and omits some current operands/filter columns. Consult the numeric base tables and source enums.

The documentation process does not repair these views or change gameplay data.

## Remaining limits

The [coverage report](coverage.md) lists fields whose meanings remain independently unresolved. External DB2 IDs, flag applicability, generic loaders, and custom scripts may require further investigation. SQL schema completeness should not be presented as complete behavioral knowledge.

This snapshot will drift as core migrations are applied. Refresh metadata and review the source revision before authoring new content from these pages.
