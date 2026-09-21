# Shaders — Godot 4.7

Prefer built-in materials and environment features when they express the effect. Godot shading language starts with `shader_type`; use explicit types and only outputs the effect needs. Writing spatial `ALPHA` enters the transparent pipeline. Avoid `discard` unless clipping is required.

Shader processor functions and built-ins differ across `spatial`, `canvas_item`, `particles`, `sky`, and `fog`. Verify renderer support before adding preprocessor branches or screen/depth texture reads.

## Source

- [Shading language](https://docs.godotengine.org/en/4.7/tutorials/shaders/shader_reference/shading_language.html)
