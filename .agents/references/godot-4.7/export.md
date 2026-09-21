# Export — Godot 4.7

Export presets live in `export_presets.cfg`; credentials and signing secrets stay outside the repository. Install the matching export templates, define the target preset in the editor, then use the editor or `godot --headless --path <project> --export-release <preset> <output>`.

An export command succeeding is not a launch test. Run the exported artifact on its target, exercise the required path, and inspect errors. For Web, verify browser/runtime feature compatibility, cross-origin hosting requirements, input methods, viewport responsiveness, and threaded-export headers when threads are enabled.

## Sources

- [Exporting projects](https://docs.godotengine.org/en/4.7/tutorials/export/exporting_projects.html)
- [Command line tutorial](https://docs.godotengine.org/en/4.7/tutorials/editor/command_line_tutorial.html)
- [Exporting for Web](https://docs.godotengine.org/en/4.7/tutorials/export/exporting_for_web.html)
