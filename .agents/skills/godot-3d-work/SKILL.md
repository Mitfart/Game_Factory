---
name: godot-3d-work
description: Build or debug Godot 3D scenes, cameras, lighting, environments, MultiMesh, LOD/HLOD, occlusion, and rendering stutter.
---

# Godot 3D work

1. **Inspect:** Read the scene hierarchy, camera, environment, lights, imported resources, renderer, frame monitors, and measured bottleneck. Read [3d-rendering.md](../../references/godot-4.7/3d-rendering.md). Also read [runtime-performance.md](../../references/godot-4.7/runtime-performance.md) only for profiling or pipeline-compilation work.
2. **Change:** Implement only the inspected scene or measured rendering-performance change using the loaded references.
3. **Verify:** Run from the target camera and renderer, inspect visual correctness and diagnostics, and A/B frame time, draw calls, primitives, culling, or pipeline monitors relevant to the change.
