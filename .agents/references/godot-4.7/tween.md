# Tweens — Godot 4.7

Tweens are one-shot and start automatically. Build a new tween for each playback and kill an existing tween before another writes the same property. `Node.create_tween()` binds lifetime to that node; bind tree-created tweens unless outliving the node is deliberate.

Tweeners are sequential by default. Use `parallel()` or `set_parallel(true)` for a parallel step and `chain()` to resume sequencing. Give infinite loops real duration. Physics state should use physics process mode.

## Source

- [Tween](https://docs.godotengine.org/en/4.7/classes/class_tween.html)
