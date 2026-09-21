---
name: godot-gdshader
description: Write, edit, or review Godot 4 GDShader code, materials, and shader performance.
---

# GDShader

1. **Inspect:** Identify shader type, renderer, material consumers, transparency/depth needs, and the measured effect cost. Read [gdshader.md](../../references/godot-4.7/gdshader.md); use `godot-docs-lookup` for processor built-ins.
2. **Change:** Implement only the inspected shader/material effect using the loaded reference; preserve unrelated material and renderer behavior.
3. **Verify:** Compile in the target renderer, inspect errors and visual output in every affected pass, and compare frame time/pipeline behavior when performance motivated the change.
