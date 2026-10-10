# SmartAI

[Database documentation](../README.md)

[smart_scripts](../tables/smart_scripts.md) stores an event, an action, and a target for each program row. The owner is selected by entryorguid and source_type. id identifies a row within the owner; link chains execution into another row. The SQL primary key also includes link, so loader expectations should be checked separately from database uniqueness.

## Current enum and operand reference

[SmartAI enums](../reference/smartai-enums.md) reproduces this checkout's event, action, target, source, phase, and flag definitions with operand comments. Reserved/unused values and end/count sentinels are not valid content choices.

Each event/action/target discriminator selects a different operand layout. Keep unused parameters neutral according to the loader. Modern master has event_param5, event_param_string, action_param7, action_param_string, target_param4, target_param_string, and Difficulties; older examples may omit them.

The runtime implementation in SmartScript.cpp establishes exact behavior. Header comments are useful parameter maps, but they cannot describe every condition or target restriction.

## Ownership and phases

A creature template generally selects SmartAI through AIName; gameobject AI and area-trigger/scene sources have their own configuration and source types. Negative entryorguid can select a specific spawn where supported. A timed action list uses its list identity and its dedicated source type.

event_phase_mask filters SmartAI's internal event phases. It does not change world visibility phases. World PhaseId/PhaseGroup settings are a separate subsystem.

Difficulties filters script rows by difficulty IDs. event_flags controls execution rules such as repetition/reset behavior. event_chance controls probability once an event is eligible.

## Linking and timing

A linked row should use SMART_EVENT_LINK and belong to the appropriate owner/source. Avoid missing targets, duplicate runtime IDs, self-links, and cycles. Timed action lists sequence delayed actions rather than serving as ordinary creature event rows.

Update/cooldown timing operands generally use milliseconds. Some actions consume seconds, distances, percentages, or typed IDs. Use the operand comments and implementation for that particular action.

## Read-only example

```sql
SET @script_entry = 0; -- existing creature template
SELECT *
FROM smart_scripts
WHERE entryorguid = @script_entry AND source_type = 0
ORDER BY id, link;
```

Source type 0 is the current creature source; verify other values in the local enum.

For a repeatable combat cast, review SMART_EVENT_UPDATE_IC, SMART_ACTION_CAST, and SMART_TARGET_VICTIM. The event's initial/repeat ranges, action spell/flags, and victim availability all matter. Use current operand definitions rather than blindly copying a numeric INSERT example.

## Debugging

First confirm the intended AI is selected and the program loads without sql.sql errors. Then check owner identity/source type, difficulty, event flags and phase, trigger availability, event chance, conditions, target availability, and operand validity. A target such as action invoker depends on the triggering context; an update timer may not supply a player invoker.

The custom vw_smart_scripts_with_labels view has older names and misses current fields. It is a convenience view, not the authoritative enum reference.
