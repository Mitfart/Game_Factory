# Prototype-stage implementation acceptance

Validated with disposable repositories outside the Game Factory repository using official Godot `4.7.2.stable` (`ed1daf0bf`). Test artifacts were retained under `%TEMP%/game-factory-acceptance/` during implementation.

## Static

- 20 Agent Skills passed frontmatter/name uniqueness checks.
- 25 internal reference links resolved; all 14 shared Godot references were present.
- 37 concrete official Godot 4.7 documentation URLs returned success.
- The five superseded 3D entrypoints were absent; no Three.js, multiplayer, selector, or broad-router guidance was found.

## `/gf-start`

- No-assets start: Godot import and bounded runtime passed; committed clean `main`; no `dev`.
- Asset-backed start: nested filenames/structure and SHA-256 hashes matched; `ASSETS.md` retained provenance.
- Two same-basename inputs produced a pre-copy collision stop with no overwritten asset.
- A foreign nonempty destination was unchanged.
- Interruptions after initialization and asset intake resumed the same records without duplicate assets, ending in one clean baseline commit.

## `/gf-prototype`

- Count `1`: created `dev`, approved/committed the Prototype Space, retained one descriptive branch/worktree, passed Godot import/runtime checks, and ended clean/evaluable.
- Default count: created exactly three isolated, clean alternatives with distinct momentum, grid-step, and directional-burst hypotheses.
- Later run: retained explicit `continue prototyping` feedback and a revised approved Prototype Space; prior branch, worktree, evidence, and `PROTOTYPE.md` blobs remained unchanged.
- Recovery injection: preserved failed-owner edits while unaffected work continued; repaired stale evidence to Git; checkpointed a simulated two-hour stop; isolated one MCP-blocked verification after one reconnect attempt; resumed the same run identity and artifacts after the simulated fix; all three then passed Godot import/bounded runtime and emitted minimal review output.

Model names/reasoning routes were checked statically because the acceptance harness supplied its configured model rather than Terra/Luna.
