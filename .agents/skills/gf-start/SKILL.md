---
name: gf-start
description: Start or resume an independent Godot Game Project from an idea and explicit asset decision.
disable-model-invocation: true
---

# Game Factory start

Create one recoverable Game Project. The Game Factory repository stores nothing from the run.

## 1. Collect and classify

Require an explicit **absolute** destination before touching it. Inspect it first:

- nonexistent or empty: this may be a new operation;
- nonempty: read [recovery.md](references/recovery.md) and either resume an identifiable interrupted start or refuse it without mutation.

For a new operation, also require an Operator-provided Internal Project Name, idea or prior research with references, and either explicit `no assets` or explicit local Asset Library paths/uploads. For supplied assets require purpose and supplied license/attribution for each input; `unknown` is valid, but never infer it. Ask for missing inputs and confirm the destination and asset decision.

For a resume, use retained inputs and ask only for missing Operator decisions.

## 2. Initialize and checkpoint

For a new operation:

1. Create the destination and initialize an independent Git repository with branch `main`.
2. Immediately create `.game-factory/start.md` with `Command: gf-start`, absolute destination, Internal Project Name, status/checkpoint, submitted idea/research and references, asset decision/metadata, brief feedback/approval state, and verification/commit state.
3. Create the smallest GDScript Godot project with `project.godot`, one main scene, and one script that visibly launches. Use the installed Godot version and keep the bootstrap neutral to 2D/3D.
4. Add `.worktrees/` to `.gitignore`; do not create `dev`.

Update the start record atomically after each durable checkpoint and before dependent work.

## 3. Intake assets

For `no assets`, write the explicit decision in `ASSETS.md`.

For supplied paths, read and follow [assets.md](references/assets.md). Do not continue to briefing until every copy and inventory row is verified.

## 4. Draft and approve the Game Brief

Use the retained idea/research, references, feedback, and copied-project asset inspection to draft `GAME_BRIEF.md` containing only:

- player fantasy;
- premise;
- core experience;
- broad genre;
- inspirations and source links;
- non-negotiables;
- scope boundaries.

Show the draft and stop for explicit Operator approval or feedback. Record feedback in `.game-factory/start.md` before revising. Silence is not approval. Record the approved status and exact approved revision before verification. Leave public title selection, risk analysis, and repeated platform boilerplate out.

## 5. Verify and commit

Using configured Godot/editor tooling:

1. Import/open the project and launch the bootstrap.
2. Fix and rerun until it has no parser error or immediate runtime error; static inspection is not runtime verification.
3. Check required contents of `GAME_BRIEF.md`, `ASSETS.md`, and `.game-factory/start.md`; recheck supplied asset bytes and paths.
4. Confirm branch is `main`, `dev` does not exist, and no credentials or machine configuration were written.
5. Mark verification complete, stage the bootstrap and all records/assets, and create one baseline commit.
6. Confirm `main` contains it and `git status --porcelain` is empty.

If interrupted, leave the latest checkpoint and report the exact `/gf-start` reinvocation. On success, report the Game Project path and baseline commit; do not begin prototyping.
