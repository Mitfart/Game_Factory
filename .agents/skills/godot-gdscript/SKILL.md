---
name: godot-gdscript
description: Write, edit, or review typed GDScript structure, callbacks, coroutines, and script-level conventions.
---

# GDScript

1. **Inspect:** Read the whole affected script, its base class, callers, signals, and project Godot version. Read [language.md](../../references/godot-4.7/language.md) for syntax, callback, typing, or coroutine facts.
2. **Change:** Implement the smallest script change using the loaded reference and preserve unrelated behavior.
3. **Verify:** Run script validation, exercise the affected scene/path, and inspect parser/runtime diagnostics. Recheck object and state validity after every relevant `await`.
