---
name: godot-navigation
description: Implement or debug Godot 2D/3D navigation agents, path following, avoidance, map synchronization, and baking.
---

# Navigation

1. **Inspect:** Trace map/region setup, bake state, agent layers, target updates, movement ownership, and synchronization. Read [navigation.md](../../references/godot-4.7/navigation.md) and verify dimension-specific members through `godot-docs-lookup`.
2. **Change:** Implement only the inspected map, path, avoidance, or bake change using the loaded references.
3. **Verify:** Exercise reachable/unreachable targets, narrow clearance, retargeting, completion, and avoidance if enabled; inspect jitter, recursive callbacks, and runtime diagnostics.
