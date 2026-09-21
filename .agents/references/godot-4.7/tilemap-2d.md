# TileMapLayer — Godot 4.7

Use `TileMapLayer`; `TileMap` is deprecated. Each layer owns a `TileSet`. `set_cell()` takes coordinates first and no layer index. Batch edits settle at frame end; `update_internals()` forces the expensive immediate update. Restrict runtime tile-data overrides to cells that need them.

## Source

- [TileMapLayer](https://docs.godotengine.org/en/4.7/classes/class_tilemaplayer.html)
