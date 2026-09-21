---
name: godot-tween
description: Implement or debug Godot Tween property, method, callback, parallel, loop, timing, and lifetime behavior.
---

# Tweens

1. **Inspect:** Find every writer of the target property, tween creation site, binding/lifetime, process mode, pause behavior, and await caller. Read [tween.md](../../references/godot-4.7/tween.md).
2. **Change:** Implement only the inspected tween sequence and lifetime change using the loaded reference.
3. **Verify:** Exercise replay, interruption, node deletion, pause/time scale, and completion signals that apply; inspect for per-frame tween creation and runtime errors.
