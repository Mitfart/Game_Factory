# Game-development skills audit

**Ticket:** [#3 — Audit candidate and local game-development skills](https://github.com/Mitfart/Game_Factory/issues/3)
**Decision:** retain the local Godot set; adopt selected Apache-2.0 Godot coverage only after a reference-first rewrite; do not import the Three.js pack or either upstream router.
**Method:** primary repository files at the revisions below, plus the live local checkout. This is a recommendation only: no skill files were changed.

## Evidence and scope

| Source | Revision inspected | What was inspected | License / consequence |
|---|---|---|---|
| [awesome-gamedev-agent-skills](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179) | `b105e1cf617adf0b68ed98790a716bbb60993179` | README catalog, [router](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/router/SKILL.md), all 15 `skills/godot/*` skill folders and their references | [Apache-2.0](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/LICENSE). A copied/modified file needs its license, copyright/attribution notices, change notice, and the upstream [NOTICE](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/NOTICE) retained. |
| [threejs-game-skills](https://github.com/majidmanzarpour/threejs-game-skills/tree/e5f301d548bb18c530afbece78cd25082f4cda9c) | `e5f301d548bb18c530afbece78cd25082f4cda9c` | README, all nine `skills/threejs-*` folders, helper/scripts inventory, and package manifest | [MIT](https://github.com/majidmanzarpour/threejs-game-skills/blob/e5f301d548bb18c530afbece78cd25082f4cda9c/LICENSE). Copying a substantial portion requires the copyright and permission notice. |
| Local Game Factory checkout | `D:/Projects/Godot/Game_Factory/.agents/skills/` (17 untracked skill folders, inspected 2026-09-19) | every local `SKILL.md`; local repository has no `LICENSE` | Treat local material as proprietary/unlicensed until the parent project adds an explicit license. Do not redistribute it or mix copied third-party text without provenance. |

The local repository's `.agents/skills/` is presently untracked, so it has no Git provenance or inherited project license. That is a release blocker for sharing these skills, not a reason to delete their useful content.

## What is useful

### Keep the local majority

Keep all 17 local skills. They are focused, Godot-4.7-aware reference material and cover several gaps the candidate Godot set does not: `godot-docs-lookup`, `godot-init`, `godot-work`, `godot-localization`, `godot-mesh-lod-3d`, `godot-multimesh-3d`, `godot-navigation`, `godot-occlusion-culling-3d`, `godot-pipeline-compilation`, and `godot-visibility-ranges-3d`.

The remaining seven (`godot-character-body`, `godot-gdscript`, `godot-gdshader`, `godot-input`, `godot-tilemap-2d`, `godot-tween`, `godot-ui`) also contain useful targeted Godot facts. Preserve them, but remove duplicated routing/boilerplate when reorganizing them below.

### Candidate Godot coverage worth adopting

The upstream Godot catalog is deliberately task-scoped and places depth in a sibling `references/` file; see the [Godot catalog](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot). Its missing local capabilities are worthwhile:

| Candidate | Recommendation | Reason / overlap |
|---|---|---|
| [`godot-nodes-scenes`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-nodes-scenes) | **Import then rewrite** | Missing local scene-tree, instancing, autoload, and `PackedScene` guidance. |
| [`godot-signals-groups`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-signals-groups) | **Import then rewrite** | Local GDScript mentions signals/groups but does not own their composition patterns. |
| [`godot-resources`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-resources) | **Import then rewrite** | Missing data-driven `Resource`/`.tres` design guidance. |
| [`godot-audio`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-audio) | **Import then rewrite** | Missing buses, effects, and music/SFX runtime guidance. |
| [`godot-multiplayer`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-multiplayer) | **Import then rewrite, on demand** | Useful isolated netcode coverage; keep it out of normal single-player context. |
| [`godot-export`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-export) | **Import then rewrite** | Missing editor/CLI export procedure; it complements rather than replaces local pipeline-stutter guidance. |
| [`godot-3d-essentials`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-3d-essentials) | **Import then rewrite** | Missing baseline cameras, environment, lights, and GridMap. Pair with the local detailed 3D performance references. |
| [`godot-physics`](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/b105e1cf617adf0b68ed98790a716bbb60993179/skills/godot/godot-physics) | **Import selectively** | Adds rigid/static/area bodies, layers, and queries. Keep local `godot-character-body` as the authority for kinematic bodies. |

Do **not** copy the following whole skills: `godot-gdscript`, `godot-shaders`, `godot-tilemap`, `godot-ui-control`, `godot-animation`, or `godot-2d-movement`. Their scopes overlap local `godot-gdscript`, `godot-gdshader`, `godot-tilemap-2d`, `godot-ui`, `godot-tween`, and `godot-character-body`; one authority per API topic avoids contradictory advice. Mine them only for version-verified facts while rewriting from official Godot documentation.

`godot-csharp` is deferred, not rejected. The local `godot-init` explicitly creates a .NET project and installs Godot-MCP, so C# can become relevant. Add it only when Game Factory chooses C# gameplay as a supported authoring path; otherwise its 170-line workflow is dead context.

### Three.js result: do not import

The pack is competent but is the wrong engine and operational shape for this project. Its [README](https://github.com/majidmanzarpour/threejs-game-skills/blob/e5f301d548bb18c530afbece78cd25082f4cda9c/README.md) describes a Vite/TypeScript/Three.js scaffold, browser QA, and optional Tripo, Gemini, and ElevenLabs asset services. The repository manifest adds Playwright and `pngjs` development dependencies; the nine skill folders also bundle 426 KB of scripts, assets, and references.

| Three.js skill(s) | Decision | Conflict / dependency |
|---|---|---|
| `threejs-game-director` and all eight specialists | **Do not import** | A browser-game router overlaps the role of a project workflow but selects the wrong engine and assumes sibling `threejs-*` names. |
| `threejs-gameplay-systems`, `threejs-aaa-graphics-builder`, `threejs-game-ui-designer`, `threejs-debug-profiler`, `threejs-qa-release` | **Do not copy; optionally re-express a principle** | Their scope-to-verification discipline is useful, but their implementation assumes Three.js/browser tooling and bundled helpers. Recreate only a Godot-specific verification checklist if a real release workflow needs it. |
| `threejs-3d-generator`, `threejs-image-generator`, `threejs-audio-generator` | **Do not import** | They depend on Tripo/Gemini/ElevenLabs credentials and provider workflows. They create cost, secret-handling, and asset-license questions unrelated to a Godot skill baseline. |

## Overlap, conflicts, and dependencies

1. **Router conflict.** Do not install awesome-gamedev's top-level router. Its documented behavior detects one of ten engines, defaults an unknown engine to Godot, and routes to its complete 73-skill catalog. That broad, always-applicable entrypoint would compete with Game Factory's Godot-specific materials. Do not install the Three.js director for the same reason.
2. **Version alignment.** Both local skills and the selected awesome Godot skills target Godot 4.7, so there is no baseline conflict today. Preserve the existing `godot-docs-lookup` practice of checking version-sensitive APIs; upstream guidance explicitly says to preserve an existing project's pinned engine version.
3. **Authority boundaries.** API/syntax belongs in the Godot reference; a task skill should own only selection and execution. Keep `godot-character-body` authoritative for `CharacterBody*`, `godot-tilemap-2d` for `TileMapLayer`, `godot-ui` for `Control`, `godot-tween` for tweens, and `godot-gdshader` for shaders. New general physics must link to—not repeat—the character-body material.
4. **Project integration boundary.** Keep `godot-init` and `godot-work` separate. The former performs one-time .NET/Godot-MCP setup and human OAuth; the latter requires an already connected MCP endpoint. Neither dependency is present in the two candidate repositories.
5. **License boundary.** First establish local ownership/license. Then either (a) independently rewrite from official Godot docs, avoiding upstream text, or (b) retain Apache-2.0 and NOTICE attribution for each copied awesome-derived file. Never transplant Three.js content without its MIT notice, and never copy its credential scripts into Godot tooling.

## Recommended target structure

Use plain shared reference, not another catch-all model-invoked skill. This follows the writing guidance: shared material that multiple skills need lives outside the skill system, while task skills point to it only when their branch applies.

```text
.agents/
  references/
    godot-4.7/
      language.md                 # GDScript and signals/groups
      scenes-data.md              # nodes, scenes, autoloads, Resources
      2d-gameplay.md              # CharacterBody, TileMapLayer, input, navigation
      ui-localization.md          # Control, focus, translations
      animation-shaders.md        # Tween, AnimationPlayer/Tree, GDShader
      3d-rendering.md             # scene/environment, LOD/HLOD, MultiMesh, occlusion
      runtime-performance.md      # physics, pipeline compilation, profiling
      audio-multiplayer-export.md # three opt-in concerns
      official-docs.md            # existing raw-RST lookup method and version rule
  skills/
    godot-init/
    godot-work/
    godot-gdscript/
    godot-character-body/
    godot-tilemap-2d/
    godot-input/
    godot-ui/
    godot-localization/
    godot-navigation/
    godot-gdshader/
    godot-tween/
    godot-3d-work/                # new, replaces only the fragmented 3D entrypoint
    godot-audio/
    godot-multiplayer/
    godot-export/
```

Each retained/new task `SKILL.md` should be short: a precise description with trigger branches, a three-step inspect/change/verify loop, and one link of the form “Read `../../references/godot-4.7/<topic>.md` when …”. This is progressive disclosure: everyday tasks read only the task body, while common facts have one source of truth and detailed 3D/network/export material loads only when requested.

### Restructure actions, in order

1. **Add provenance first:** add a project license/ownership decision, commit the currently untracked local skills, and record any Apache-derived files plus the Apache LICENSE/NOTICE in a third-party-notices location.
2. **Create the nine shared references:** migrate the facts from all 17 local skills without changing their meaning; add selected Awesome coverage by independent rewrite or compliant Apache attribution.
3. **Keep names stable initially:** do not rename the 17 existing skills during the reference extraction—descriptions are invocation pointers. There is no correctness gain from a churn-only rename.
4. **Consolidate only the six 3D performance entrypoints** (`godot-mesh-lod-3d`, `godot-multimesh-3d`, `godot-occlusion-culling-3d`, `godot-pipeline-compilation`, `godot-visibility-ranges-3d`, plus imported 3D essentials) into new `godot-3d-work`. Delete those six thin wrappers only after their trigger branches and verification steps are represented there. This is the only recommended delete.
5. **Add the eight selected coverage gaps** as focused task skills/reference sections. Leave C# deferred until it is actually supported.
6. **Add a lightweight Godot-only selector only if selection fails in practice.** It should inspect `project.godot`, choose the minimal task skill(s), and link to references; it must not copy the broad upstream router or route to non-Godot engines.

## Acceptance checks for the implementation ticket

- Every retained/imported skill has a unique authority and an accurate model-facing description.
- No task body repeats Godot API reference material owned by `references/godot-4.7/`.
- Each shared-reference pointer says exactly when to read it.
- `godot-init` and `godot-work` still preserve their setup-versus-connected-project boundary.
- Any copied Apache text has LICENSE, NOTICE, source URL/revision, and a modification notice; independently rewritten material has its official Godot-doc sources recorded.
- No Three.js runtime, browser dependency, provider credential workflow, or upstream broad router is installed.

## Primary-source links

- Awesome catalog and stated Godot 4.7 baseline: [README](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/README.md)
- Awesome task routing, minimal selection, and reference-on-demand protocol: [router/SKILL.md](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/router/SKILL.md)
- Awesome license and attribution: [LICENSE](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/LICENSE), [NOTICE](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/blob/b105e1cf617adf0b68ed98790a716bbb60993179/NOTICE)
- Three.js package scope/dependencies: [README](https://github.com/majidmanzarpour/threejs-game-skills/blob/e5f301d548bb18c530afbece78cd25082f4cda9c/README.md), [package.json](https://github.com/majidmanzarpour/threejs-game-skills/blob/e5f301d548bb18c530afbece78cd25082f4cda9c/package.json), [LICENSE](https://github.com/majidmanzarpour/threejs-game-skills/blob/e5f301d548bb18c530afbece78cd25082f4cda9c/LICENSE)
- Local evidence: `D:/Projects/Godot/Game_Factory/.agents/skills/*/SKILL.md` (untracked audit snapshot).
