---
name: gf-prototype
description: Run or resume isolated, Godot-verified Prototype alternatives in an approved Prototype Space.
argument-hint: "[count]"
disable-model-invocation: true
---

# Game Factory Prototype Run

`count` is one optional positive base-10 integer. No argument means `3`. Reject zero, negatives, decimals, extra positional arguments, and non-integers before mutation.

## 1. Locate and inspect

Ask for and confirm the explicit absolute Game Project path on every invocation. Inspect before mutation:

- current branch/status, `main` and `dev` refs, commits, and registered worktrees;
- `project.godot`, committed `GAME_BRIEF.md`, `ASSETS.md`, and `.game-factory/start.md`;
- `PROTOTYPE_SPACE.md`, `.game-factory/runs/*.md`, Prototype branches/worktrees, and `PROTOTYPE.md` files.

A valid start record says `Command: gf-start`, approved and Godot-verified, and agrees with committed `main`. Reject a missing, foreign, or invalid baseline before Prototype work.

If the tree is dirty, first determine without mutation whether those changes belong to an identifiable incomplete `/gf-prototype` run. Reject unrelated or ambiguous dirt before creating `dev` or starting owner work. If an incomplete record, matching partial branch/worktree, recoverable dirty state, stale evidence, or required MCP outage exists, read [recovery.md](references/recovery.md) before proceeding. Otherwise require clean `main`/`dev` state.

## 2. Establish the approved baseline

For the first run, create `dev` from committed `main` without changing `main`. For any later invocation, read [later-runs.md](references/later-runs.md) and retain its disposition and feedback before dependent work.

Run one focused grilling to establish the Game Direction and a Prototype Space containing shared invariants, permitted variation axes, manual evaluation criteria, excluded directions, and one required playable path with expected controls.

Draft `PROTOTYPE_SPACE.md`, show it, and stop for explicit Operator approval. Silence is not approval. Commit the approved space and submitted feedback on `dev` before any Prototype Builder starts.

## 3. Plan and checkpoint

Choose a unique descriptive `run-slug`, never a numbered round. Select exactly `count` alternatives whose hypotheses differ meaningfully on approved variation axes; cosmetic, content-only, and tuning-only differences do not qualify.

For each alternative choose a display name and descriptive `prototype-slug`, then reserve branch `prototype/<run-slug>/<prototype-slug>` and matching worktree `.worktrees/<run-slug>/<prototype-slug>`. Ensure `.worktrees/` is ignored.

Before launching Builders, write and commit `.game-factory/runs/<run-slug>.md` on `dev` with:

- command, run slug, requested count, approved-space commit, `dev` baseline commit, disposition, and submitted feedback;
- automated start time, two-hour budget, elapsed time, model invocations, and available provider token/currency telemetry;
- every requested Prototype's display name, hypothesis/axis, branch, absolute worktree, owning Builder, and state (`planned`, `active`, `blocked`, `failed`, or `evaluable`);
- last successful check, checks/results, limitations, placeholders, unfinished work, retry/escalation/correction history, and failure/recovery detail;
- Godot/MCP verification state.

Create every branch/worktree from that exact `dev` commit. Checkpoint meaningful transitions atomically and commit evidence updates on `dev`.

## 4. Build alternatives

Assign exactly one end-to-end Prototype Builder to each worktree. Only that Builder edits it at a time. A Prototype Builder asks the lead Builder for support; only the lead Builder launches support tasks, keeping orchestration one level deep.

Model routing:

- `openai-codex/gpt-5.6-terra`, medium reasoning: lead Builder, Prototype Builders, judgment, integration, correction, and recovery;
- `openai-codex/gpt-5.6-luna`, low reasoning: clearly bounded mechanical support only.

After one materially failed Luna attempt, escalate ambiguous or cross-cutting work to Terra. A delegated task gets at most one retry after its edits are preserved and inspected; then the lead Builder replans. Retries preserve history and elapsed time.

Each Prototype Builder must:

1. Read the approved Game Brief, Prototype Space, relevant copied assets, and narrow Godot task skills/references.
2. Build one complete playable path testing the assigned hypothesis while preserving shared invariants.
3. Use primitives and obvious placeholders by default. Request an asset only when no honest placeholder can test an essential direction; record asset, format, constraints, use, and blocked evaluation, then pause only that Prototype.
4. Keep GDScript focused and readable; avoid production architecture, generated assets, exhaustive tests, and known Web-incompatible choices.
5. Create `PROTOTYPE.md` containing only display name and exact editor testing instructions: scene/path, controls, steps, and observable result.
6. Exercise those instructions in Godot, fix parser/runtime errors, and fix or explain relevant warnings in run evidence.
7. Commit the playable result and `PROTOTYPE.md`, leave the worktree clean, and return checks, limits, placeholders, unfinished work, telemetry, and commit ID to the lead Builder.

## 5. Budget and acceptance

The run has a two-hour elapsed automated wall-clock budget shared by alternatives and synthesis. Concurrent Builders consume elapsed time, not summed agent-hours. Pause only for Operator input/review or an Asset Request. At expiry launch nothing new, safely cancel active tasks, checkpoint all work, and follow [recovery.md](references/recovery.md) unless the Operator explicitly approves a stated extension.

The lead Builder reviews every branch, worktree, and evidence entry. A Prototype is evaluable only when it has a distinct approved hypothesis, intact invariants, exercised playable path, clean Godot import/run, fixed or explained warnings, sufficient controls/instructions, committed playable work and compliant `PROTOTYPE.md`, a clean worktree, and evidence agreeing with Git.

A rejected result receives one correction pass in the same worktree and remaining budget. After that it stays unevaluable. The run completes only when every requested Prototype is evaluable and the final reconciled run record is committed on `dev`. Keep all branches and worktrees. Leave scoring, game feel, visual judgment, comparison, selection, approval, merging, and cleanup to the Operator.

## 6. Output

On success, output only each Prototype display name followed by its exact `PROTOTYPE.md` testing instructions—no preface, ranking, recommendation, branch detail, evidence summary, or next-step menu.

For any incomplete outcome, use the stop-report contract in [recovery.md](references/recovery.md) and withhold comparative review.
