# Scenes and data — Godot 4.7

## Nodes and scenes

A scene is a `PackedScene` resource that instantiates a node tree. Give ownership of dynamically added nodes to the intended scene owner only when they must be saved. Use `queue_free()` for normal deletion and add a node to the tree before relying on tree-dependent callbacks.

Load a fixed scene with `preload()`, instantiate it with `PackedScene.instantiate()`, configure it through its public API, then add it under the node that owns its lifecycle. Use `change_scene_to_file()` for whole-scene transitions; preserve cross-scene state in a deliberately small autoload or Resource, not accidental node paths.

Autoloads are always loaded and globally reachable. Use them only for genuinely cross-scene services or state; they are not ordinary singleton enforcement and should not absorb scene-local behavior.

## Resources

`Resource` is reference-counted data. Export typed properties in custom Resource scripts and store editor-authored data in `.tres` files. Loaded resources are cached and shared: duplicate before mutating data that must become instance-local. Keep runtime node references and scene-tree behavior out of reusable data resources.

Resource paths use `res://` inside the project and `user://` for writable user data. Packaged `res://` content is not a general save location.

## Sources

- [Nodes and scenes](https://docs.godotengine.org/en/4.7/getting_started/step_by_step/nodes_and_scenes.html)
- [Instancing](https://docs.godotengine.org/en/4.7/getting_started/step_by_step/instancing.html)
- [PackedScene](https://docs.godotengine.org/en/4.7/classes/class_packedscene.html)
- [Autoloads](https://docs.godotengine.org/en/4.7/tutorials/scripting/singletons_autoload.html)
- [Resources](https://docs.godotengine.org/en/4.7/tutorials/scripting/resources.html)
