---
name: godot-physics
description: Implement or debug Godot static, rigid, animatable, and area physics, collision layers, and space queries; excludes CharacterBody movement.
---

# General physics

1. **Inspect:** Identify body/area ownership, shapes, layers/masks, physics-step mutations, signals, and query callers. Read the physics section of [runtime-performance.md](../../references/godot-4.7/runtime-performance.md). Use `godot-character-body` instead for CharacterBody movement.
2. **Change:** Implement only the selected body, area, layer/mask, or query change using the loaded reference.
3. **Verify:** Exercise collisions/overlaps, enter/exit lifecycle, moving platforms or rigid simulation that apply, and representative queries; inspect tunneling, duplicate signals, and runtime diagnostics.
