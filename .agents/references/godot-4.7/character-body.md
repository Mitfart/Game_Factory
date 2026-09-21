# Character bodies — Godot 4.7

Move `CharacterBody2D` from `_physics_process()` with `move_and_slide()` or `move_and_collide()`. `velocity` is units per second: `move_and_slide()` applies physics delta; `move_and_collide()` receives an absolute motion such as `velocity * delta`. Apply acceleration and `get_gravity()` with delta.

`move_and_slide()` rewrites velocity after collisions. Floor, wall, ceiling, and slide-collision state describes the latest call. Grounded classification uses `up_direction` and `floor_max_angle`; floating mode classifies collisions as walls.

## Source

- [CharacterBody2D](https://docs.godotengine.org/en/4.7/classes/class_characterbody2d.html)
