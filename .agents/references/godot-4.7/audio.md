# Audio — Godot 4.7

Use `AudioStreamPlayer` for non-positional sound and the 2D/3D variants for positional sound. Route players to named buses for music, effects, voice, and UI control; adjust bus volume/effects centrally instead of traversing players. Reuse players or a small pool for overlapping short effects and avoid restarting a single player when overlap is required.

Loop music through the stream's import/resource settings where supported. Treat decibels as logarithmic and use Godot's linear/dB conversion helpers for user-facing sliders. Verify pause behavior and whether a player's process mode should continue while the tree is paused.

## Sources

- [Audio buses](https://docs.godotengine.org/en/4.7/tutorials/audio/audio_buses.html)
- [AudioStreamPlayer](https://docs.godotengine.org/en/4.7/classes/class_audiostreamplayer.html)
