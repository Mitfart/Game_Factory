# GDScript, signals, and groups — Godot 4.7

## Scripts

Statically type variables, parameters, returns, and containers. Use `StringName` literals (`&"name"`) for repeated identifiers, `preload()` for fixed paths, cached or `@onready` node references, packed arrays for bulk buffers, integer vectors for grids, and static methods when instance state is unnecessary. Avoid per-frame allocation.

Match virtual callback signatures exactly. `_process()` and `_physics_process()` receive seconds as `float`; physics movement belongs in `_physics_process()`. Use `_unhandled_key_input()` for gameplay keys when GUI should get first refusal.

`await` makes the enclosing function a coroutine when waiting on a signal or coroutine. After resumption, revalidate object lifetime, tree membership, and the state or generation that started the work.

## Signals

Declare typed signals and connect callables rather than string method names. Signals decouple senders from receivers; connect where the relationship is owned and disconnect only when lifecycle does not handle it. Use one-shot or deferred connection flags only for the behavior they name. Avoid signal callbacks that synchronously trigger the same signal path.

## Groups

Groups are tags for discovery and broadcast, not ordered collections. Add stable groups in the scene or `_ready()`, query with `get_tree().get_nodes_in_group()`, and use `call_group()` for fire-and-forget broadcasts. Validate nodes or use a shared method contract before calling group members. Do not poll groups every frame when a signal can maintain the relevant set.

## Sources

- [GDScript basics](https://docs.godotengine.org/en/4.7/tutorials/scripting/gdscript/gdscript_basics.html)
- [Static typing](https://docs.godotengine.org/en/4.7/tutorials/scripting/gdscript/static_typing.html)
- [Using signals](https://docs.godotengine.org/en/4.7/getting_started/step_by_step/signals.html)
- [Groups](https://docs.godotengine.org/en/4.7/tutorials/scripting/groups.html)
- [SceneTree](https://docs.godotengine.org/en/4.7/classes/class_scenetree.html)
