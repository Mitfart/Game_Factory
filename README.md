# Game Factory

Game Factory is a local, Operator-guided workflow for creating and evaluating independent Godot Game Projects.

## Prerequisites

- A compatible Agent Skills harness with subagents and Godot MCP support.
- Git and Godot 4.7+ available to the harness.
- An explicit external destination for each Game Project.

## Start a Game Project

Invoke `/gf-start` and provide:

1. An absolute destination path.
2. An Internal Project Name.
3. An idea or research with source links.
4. An explicit `no assets` decision or supplied asset paths, with purpose and license/attribution.

Review and explicitly approve the generated Game Brief. The command verifies and commits a clean `main` baseline; it does not create `dev`.

## Run Prototypes

From a committed Game Project, invoke `/gf-prototype` or `/gf-prototype 1`.

- No count defaults to three alternatives.
- The count must be a positive integer.
- Provide the absolute Game Project path on every invocation.
- Approve the Prototype Space before Builders start.

Successful output contains each Prototype name and its exact editor testing instructions. Interrupted or blocked runs preserve their branches, worktrees, and evidence for reinvocation with the same project path.

The Factory remains stateless: project-owned files, Git refs, and worktrees are the recovery source of truth. Operator review decides whether to continue prototyping, select a Prototype for future development, or stop.
