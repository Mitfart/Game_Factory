---
name: godot-work
description: Inspect or modify scenes, nodes, resources, scripts, editor state, and diagnostics in an already connected Godot project.
---

# Work in a connected editor

1. **Inspect:** Confirm the explicit project and connected Godot MCP target, then read the active scene, relevant resources/scripts, and current diagnostics before mutation.
2. **Change:** Apply the smallest inspected change through the narrow domain skill, using MCP for editor-owned state and file editing when simpler.
3. **Verify:** Validate GDScript, run the affected scene or playable path, and inspect parser/runtime errors and relevant warnings. Never claim editor verification from file inspection alone.

Use `godot-init` only when the project or MCP connection does not exist.
