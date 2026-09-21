# Navigation — Godot 4.7

Navigation agents compute paths and avoidance but never move their parent. Wait for the navigation map to synchronize before the first query. While active, call `get_next_path_position()` once per physics tick and stop after `is_navigation_finished()`. Clearance comes from baked map agent radius; the agent radius controls avoidance.

## Source

- [Navigation overview](https://docs.godotengine.org/en/4.7/tutorials/navigation/navigation_introduction_2d.html)
