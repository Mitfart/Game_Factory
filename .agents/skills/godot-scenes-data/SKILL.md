---
name: godot-scenes-data
description: Build or debug Godot node trees, scene instancing/transitions, autoloads, Resources, and project data flow.
---

# Scenes and data

1. **Inspect:** Trace node ownership/lifetime, scene entry points, instancing callers, autoload responsibilities, resource sharing, and save paths. Read [scenes-data.md](../../references/godot-4.7/scenes-data.md).
2. **Change:** Implement only the inspected scene, autoload, Resource, or data-flow change using the loaded reference.
3. **Verify:** Instantiate/reload affected scenes, exercise transitions and save/load paths, confirm intended resource sharing or duplication, and inspect parser/runtime diagnostics.
