---
name: godot-character-body
description: Implement or debug CharacterBody2D or CharacterBody3D movement and collision response.
---

# Character bodies

1. **Inspect:** Trace input, velocity updates, motion calls, collision reads, floor settings, and physics-step ownership. Read [character-body.md](../../references/godot-4.7/character-body.md); verify 3D member differences through `godot-docs-lookup`.
2. **Change:** Implement only the inspected movement or collision-response change using the loaded references.
3. **Verify:** Exercise start/stop, slopes, jump/fall, walls, ceilings, and moving platforms that apply; inspect parser/runtime diagnostics and collision state after movement.
