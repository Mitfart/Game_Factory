# UI and localization — Godot 4.7

## Layout and focus

Containers own the rectangles of their direct `Control` children. Configure container properties and size flags instead of manually positioning those children. `SIZE_EXPAND` claims surplus space and `SIZE_FILL` stretches within it. Use anchors and offsets only under non-container parents.

Keyboard/controller targets use `FOCUS_ALL`; decoration uses `FOCUS_NONE`. Give an opened screen's first meaningful control focus with a deferred `grab_focus()` and restore focus when a modal closes. Keep visible focus styling and a mouse-free path through every operation.

`MOUSE_FILTER_STOP` receives and blocks, `PASS` receives and bubbles to Control ancestors, and `IGNORE` neither receives nor blocks. Consume Control-owned events with `accept_event()` only when handled.

## Themes

Themes propagate through uninterrupted `Control` or `Window` ancestry. Prefer theme type variations for reusable semantics and overrides for one-offs. Refresh cached theme values on `NOTIFICATION_THEME_CHANGED`.

## Localization

Translate whole messages, then format them. Node scripts can use `atr()`/`atr_n()` to respect auto-translate mode; `tr_n()` chooses a plural form but does not substitute the count. Context is part of a translation key.

Test pseudolocalization, expansion, RTL layout, focus order, and directional icons. Keep `layout_direction` inherited unless the UI has a specific reason to override it.

## Sources

- [GUI containers](https://docs.godotengine.org/en/4.7/tutorials/ui/gui_containers.html)
- [Keyboard/controller navigation](https://docs.godotengine.org/en/4.7/tutorials/ui/gui_navigation.html)
- [Using themes](https://docs.godotengine.org/en/4.7/tutorials/ui/gui_skinning.html)
- [Internationalizing games](https://docs.godotengine.org/en/4.7/tutorials/i18n/internationalizing_games.html)
