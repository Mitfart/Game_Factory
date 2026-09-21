# Implementation Tickets

Published under [parent issue #13](https://github.com/Mitfart/Game_Factory/issues/13).

## 1. [#14 — Refactor Godot guidance into shared 4.7 references](https://github.com/Mitfart/Game_Factory/issues/14)

**Blocked by:** None — ready for agent

**Delivers:** Concise Godot task skills backed by shared Godot 4.7 references, including one consolidated 3D work skill.

**Acceptance:**
- Retained skills have one responsibility and valid reference links.
- The five overlapping 3D/performance entrypoints become one discoverable 3D skill.
- Official documentation sources are recorded.
- No broad router, C#, multiplayer, or Three.js guidance is added.

## 2. [#15 — Add the missing single-player Godot task skills](https://github.com/Mitfart/Game_Factory/issues/15)

**Blocked by:** [#14](https://github.com/Mitfart/Game_Factory/issues/14)

**Delivers:** Focused Builder skills for scenes/data, signals/groups, audio, general physics, and export.

**Acceptance:**
- Each domain has a focused inspect–change–verify skill.
- Skills support single-player GDScript projects in 2D and 3D.
- Version-specific facts use shared references.
- No selector skill, C#, multiplayer, or Three.js is added.

## 3. [#16 — Start a no-assets Game Project](https://github.com/Mitfart/Game_Factory/issues/16)

**Blocked by:** None — ready for agent

**Delivers:** The no-assets `/gf-start` path from Operator idea to approved, runnable, committed Game Project.

**Acceptance:**
- Requires explicit destination, Internal Project Name, idea/research, and asset decision.
- Creates a runnable Godot repository on clean `main` with no `dev` branch.
- Retains inputs and requires explicit Game Brief approval.
- Verifies the bootstrap in Godot.

## 4. [#17 — Start an asset-backed Game Project safely](https://github.com/Mitfart/Game_Factory/issues/17)

**Blocked by:** [#16](https://github.com/Mitfart/Game_Factory/issues/16)

**Delivers:** Safe, provenance-preserving intake of Operator-supplied assets in `/gf-start`.

**Acceptance:**
- Copies assets byte-for-byte while preserving names and relative structure.
- Rejects collisions without overwrite, rename, conversion, or mutation.
- Restricts inspection to copied Game Project assets.
- Records source, destination, purpose, license, and attribution.

## 5. [#18 — Resume or refuse interrupted Game Project starts](https://github.com/Mitfart/Game_Factory/issues/18)

**Blocked by:** [#17](https://github.com/Mitfart/Game_Factory/issues/17)

**Delivers:** Repository-driven `/gf-start` recovery without destructive changes.

**Acceptance:**
- Refuses foreign or ambiguous nonempty destinations before mutation.
- Resumes only identifiable interrupted starts.
- Reuses durable checkpoints without duplication.
- Preserves uncommitted files and never resets, cleans, overwrites, or recreates work.

## 6. [#19 — Produce one evaluable Prototype](https://github.com/Mitfart/Game_Factory/issues/19)

**Blocked by:** [#14](https://github.com/Mitfart/Game_Factory/issues/14), [#15](https://github.com/Mitfart/Game_Factory/issues/15), [#16](https://github.com/Mitfart/Game_Factory/issues/16)

**Delivers:** A complete `/gf-prototype 1` run with an isolated, Godot-verified Prototype.

**Acceptance:**
- Validates the committed Game Project baseline.
- Creates `dev`, obtains and commits an approved Prototype Space, and creates one descriptive branch/worktree.
- Produces a committed playable path with clean verification and exact testing instructions.
- Records durable run evidence and emits only the Prototype name and instructions.

## 7. [#20 — Produce a complete multi-Prototype Run](https://github.com/Mitfart/Game_Factory/issues/20)

**Blocked by:** [#19](https://github.com/Mitfart/Game_Factory/issues/19)

**Delivers:** Default-three and explicit-count Prototype Runs with isolated owners and shared acceptance controls.

**Acceptance:**
- Defaults to three and accepts only positive counts.
- Each alternative tests a meaningfully different approved hypothesis.
- Enforces one owner per worktree, model routing, retry/correction rules, Asset Requests, and the two-hour budget.
- Withholds review unless every requested Prototype is evaluable.

## 8. [#21 — Run another Prototype Run from Operator feedback](https://github.com/Mitfart/Game_Factory/issues/21)

**Blocked by:** [#20](https://github.com/Mitfart/Game_Factory/issues/20)

**Delivers:** Deliberate later runs that use Operator feedback and preserve prior alternatives.

**Acceptance:**
- Retains feedback before dependent work starts.
- Requires explicit approval of the revised Prototype Space.
- Starts new alternatives from current `dev`.
- Preserves earlier branches, worktrees, documents, and evidence.

## 9. [#22 — Recover incomplete Prototype Runs](https://github.com/Mitfart/Game_Factory/issues/22)

**Blocked by:** [#20](https://github.com/Mitfart/Game_Factory/issues/20)

**Delivers:** Safe recovery for interrupted, failed, stale, timed-out, or MCP-blocked Prototype Runs.

**Acceptance:**
- Reuses the same run identity and matching artifacts on resume.
- Treats Git refs and worktree contents as authoritative over stale evidence.
- Isolates owner failures and preserves partial work.
- Produces actionable incomplete reports without reset, cleanup, duplication, or silent overwrite.

## Dependency Graph

```text
#14 ──> #15 ──┐
              ├──> #19 ──> #20 ──┬──> #21
#16 ──> #17 ──> #18          │     └──> #22
                             └──> (complete multi-Prototype flow)
```

The parent issue and published GitHub blocking relationships remain authoritative.