# 3D scenes and rendering — Godot 4.7

## Baseline scenes

Build around `Node3D` transforms, a current `Camera3D`, deliberate lights, and a `WorldEnvironment`. Keep imported scenes as source assets and compose them in project-owned scenes. Check near/far planes, shadow distances, environment background, and renderer compatibility in the actual target camera.

## Repetition

Use `MultiMeshInstance3D` when one mesh/material repeats in very large counts and instances only need transform, color, or custom data. Set transform format and color/custom-data flags before `instance_count`; resizing clears buffers. MultiMesh has no per-instance script, collision, visibility, or culling. Split spatially distant instances into regional MultiMeshes.

## LOD

Imported scene meshes can generate automatic mesh LOD. Tune global threshold and per-instance bias only after measuring. Use visibility ranges when levels are artist-authored or a distant merged node replaces a group. Visibility ranges operate on `GeometryInstance3D` AABB-center distance; use margins for hysteresis/fades and verify renderer limitations.

## Occlusion

Occlusion culling pays off when a scene has a few large opaque blockers and many fully covered occludee AABBs. Bake static occluders, inspect the occlusion buffer, and compare frame time/draw calls. Moving occluders rebuild acceleration data; toggle visibility for doors instead of animating baked occluders.

## Sources

- [Introduction to 3D](https://docs.godotengine.org/en/4.7/tutorials/3d/introduction_to_3d.html)
- [Environment and post-processing](https://docs.godotengine.org/en/4.7/tutorials/3d/environment_and_post_processing.html)
- [MultiMeshInstance3D](https://docs.godotengine.org/en/4.7/classes/class_multimeshinstance3d.html)
- [Mesh LOD](https://docs.godotengine.org/en/4.7/tutorials/3d/mesh_lod.html)
- [Visibility ranges](https://docs.godotengine.org/en/4.7/tutorials/3d/visibility_ranges.html)
- [Occlusion culling](https://docs.godotengine.org/en/4.7/tutorials/3d/occlusion_culling.html)
