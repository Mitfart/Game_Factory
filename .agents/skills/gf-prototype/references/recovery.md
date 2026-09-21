# `/gf-prototype` recovery

Read this file when state indicates an interrupted/failed run, dirty work, stale evidence, budget expiry, or required Godot MCP outage.

## Reconcile

An incomplete run takes precedence over a new run. Compare its record with actual refs, commits, registered worktrees, and files; Git/worktree state is authoritative. Repair stale evidence without deleting work and report the correction. Resume the same run slug and reuse matching branches, worktrees, and artifacts. Create a missing artifact only when evidence and Git both prove it never existed. If several incomplete runs make intent ambiguous, stop and ask which one to resume or preserve.

Preserve every tracked/untracked file. Never reset, clean, force-delete, overwrite, recreate a nonempty path, silently duplicate state, or remove a lock without proving no live process owns it. A completed Prototype is reused unless its verification is demonstrably invalid.

## Isolate failures

Keep unaffected Prototype Builders running when safe. A failed task gets the established one retry; preserve edits and history. The lead Builder may take over the same worktree only after its previous Builder has stopped.

When Godot MCP is required but unavailable, finish safe non-MCP work, make one fresh connection attempt, then mark only dependent verification blocked. Record the failed operation and exact harness-level fix. Never claim editor/runtime verification without performing it.

At the elapsed budget limit, start nothing new, safely cancel active tasks, and checkpoint every complete and partial result.

## Stop report

After a failed correction, unresolved block, or timeout, keep all branches/worktrees and withhold comparative review. Report only:

- command stage and failure/interruption;
- retry/recovery attempted;
- safe artifact paths;
- evaluable, partial, and missing Prototypes;
- exact next `/gf-prototype` invocation or external MCP/asset fix.

A successful resume emits only the normal Prototype names and testing instructions; recovery detail remains in evidence.
