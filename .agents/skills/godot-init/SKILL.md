---
name: godot-init
description: Initialize a Godot 4.7+ GDScript project and connect its editor through the configured Godot MCP runtime.
---

# Initialize a Godot project

1. **Inspect:** Confirm the explicit project path is empty, the intended renderer and 2D/3D root are known, and the harness already exposes Git, Godot, Node, and Godot MCP. Read [official-docs.md](../../references/godot-4.7/official-docs.md) when command-line behavior is version-sensitive.
2. **Change:** Create only the required GDScript project, main scene, and connection-facing project state; leave machine configuration with the harness.
3. **Verify:** Open/import the project with the installed Godot, run the main scene, inspect parser/runtime diagnostics, and confirm the configured MCP can read the project before claiming connected-editor work is available.
