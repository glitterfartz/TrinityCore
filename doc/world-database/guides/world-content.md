# Movement, events, pools, and phasing

[Database documentation](../README.md)

## Movement paths

waypoint_path defines a path; waypoint_path_node stores ordered nodes by PathId and NodeId. Nodes carry positions, orientation, and Delay. Creature/template addons can select paths. MovementType and template/spawn movement capabilities determine how an NPC uses the path.

script_spline_chain_meta and script_spline_chain_waypoints support scripted spline sequences rather than ordinary creature waypoint paths. Formation membership adds leader-relative offsets and behavior. SmartAI waypoint actions have their own timing/target parameters.

Do not import old waypoint_data or waypoints SQL into this schema. Validate the current path identity, node ordering, movement mode, terrain reachability, and any addon precedence.

## Events

game_event defines scheduling/progression. Its extension tables control spawn participation, quests, models/equipment, vendor offerings, NPC flags, pools, arena seasons, prerequisites, and condition contributions.

Event spawn association fields can be signed: the loader can use the sign to distinguish active/inactive-event participation. A negative event identifier is not simply an orphan reference. Read GameEventMgr before applying ordinary unsigned joins or cleanup.

Progression events combine prerequisites, conditions, quest contributions, and saved state in the characters database. Changing a world schedule does not reset every persistent event state.

## Pools and spawn groups

pool_template sets selection behavior; pool_members uses a type discriminator for member identity. Its spawnId can identify a creature, gameobject, or child pool according to type. Explicit chances and equal-chance members must satisfy PoolMgr's selection rules. Prevent recursive pool cycles.

Quest pools are separate: quest_pool_template and quest_pool_members rotate available quests.

spawn_group_template defines behavior flags; spawn_group associates typed persistent spawn IDs with groups. instance_spawn_groups can gate them by boss state. linked_respawn models typed respawn dependencies. spawn_tracking tables link spawn presence/state to quest-objective tracking.

A normal database spawn row does not bypass these systems.

## Phases and terrain

phase_area associates phases with areas; phase_name is an authoring label helper. Spawn PhaseId/PhaseGroup and phaseUseFlags determine visibility treatment. terrain_swap_defaults and terrain_worldmap relate replacement terrain to map presentation.

Conditions can gate phases and terrain swaps. External phase groups and maps are client records. An area ID, phase ID, phase group, and map ID are different identifiers.

## Area triggers, scenarios, and conversations

areatrigger_template and creation-property extensions describe shapes/motion. Persistent areatrigger spawns differ from client trigger IDs used by areatrigger_teleport, tavern, scripts, and quest relations.

instance_template, scenarios, and scenario POI tables configure instances/scenarios and map overlays. conversation_template, conversation_line_template, conversation_actors, and scene_template define cinematic content, with external DB2 references and scripts where applicable.

## Investigation sequence

For absent content, check map/difficulty, phase and terrain, event sign/schedule, pool selection, spawn group and instance boss state, spawn tracking, respawn dependencies, and disable entries. For broken movement, check path/addon association, node ordering, movement mode/capabilities, terrain, and scripts.
