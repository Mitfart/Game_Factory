# `/gf-start` recovery

Read this file only when the explicit destination is nonempty.

Inspect without mutation. Resume only when the destination is a Git repository containing `.game-factory/start.md` whose `Command: gf-start`, absolute destination, and incomplete status agree with the invocation. `project.godot` may be absent only when the recorded checkpoint precedes bootstrap creation.

A foreign, completed, contradictory, or ambiguous destination is a hard stop. Explain what was found and request another empty destination.

For an identifiable interruption:

1. Report the discovered status and last durable checkpoint.
2. Preserve every tracked and untracked file. Never reset, clean, overwrite, force-delete, recreate the path, or remove a lock without proving no process owns it.
3. Validate completed checkpoints against files and Git. Reuse valid records and copies rather than duplicating them.
4. Continue from the first incomplete checkpoint. A demonstrably invalid checkpoint becomes incomplete; preserve its files and report the discrepancy before correction.
