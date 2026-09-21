# Physics and runtime performance — Godot 4.7

## Physics

Use static bodies for unmoving collision, rigid bodies for simulation-owned motion, animatable bodies for scripted moving platforms, areas for overlap/field detection, and character bodies only for user-controlled kinematic motion. Keep physics changes in the physics step.

Collision layers describe where an object exists; masks describe what it scans or collides with. Prefer areas/signals for ongoing overlap and direct-space-state queries for explicit point, ray, shape, or motion checks. Exclude the querying body where self-hits are possible. Do not mutate the physics world while a query result is being iterated.

## Profiling

Measure before changing architecture. Use the profiler, frame-time monitors, rendering statistics, and debugger monitors to identify script, physics, rendering, or allocation cost. Verify optimization in the representative camera and target renderer.

## Pipeline compilation

Forward+ and Mobile precompile pipelines from rendering evidence already seen; content first instantiated or toggled during gameplay can still stutter. Exercise dynamic effects during a loading/warm-up path and watch pipeline-compilation monitors. Compatibility uses a different path and requires visible warm-up. The export Shader Baker reduces source compilation at launch but does not bake driver pipelines.

## Sources

- [Physics introduction](https://docs.godotengine.org/en/4.7/tutorials/physics/physics_introduction.html)
- [Ray casting](https://docs.godotengine.org/en/4.7/tutorials/physics/ray-casting.html)
- [Using the profiler](https://docs.godotengine.org/en/4.7/tutorials/scripting/debug/the_profiler.html)
- [Reducing stutter from shader compilation](https://docs.godotengine.org/en/4.7/tutorials/performance/pipeline_compilations.html)
