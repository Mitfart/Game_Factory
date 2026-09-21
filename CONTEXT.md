# Game Factory

Game Factory is a locally operated, agent-assisted process for turning a game idea into an independently stored Godot game project through human-approved stages.

## Language

**Game Factory**:
The system that guides ideation and coordinates creation of games. It owns the production process, not the resulting games.
_Avoid_: Generator, Fgen

**Game Project**:
An independently stored game made through the Game Factory. Each Game Project owns all of its game-specific source code, history, working data, and artifacts.
_Avoid_: Factory project, generated folder

**Game Brief**:
The Operator-approved abstract framing distilled from an idea or prior research before prototype work begins.
_Avoid_: Game Direction, implementation plan

**Game Direction**:
The Operator-approved design framing established before comparable Prototype alternatives are made.
_Avoid_: Prototype branch, game idea

**Prototype Space**:
The Operator-approved boundaries for a prototype run: shared invariants, permitted variation axes, evaluation criteria, and excluded directions. The Builder selects distinct Prototype alternatives within this space.
_Avoid_: Prototype list, visual theme

**Operator**:
The human directing the Game Factory, approving every development cycle, evaluating prototypes, and supplying assets.
_Avoid_: User, reviewer

**Builder**:
The agent responsible for planning and modifying a Game Project. In the first version, it is the only automated production role.
_Avoid_: Coder, generator

**Prototype**:
A playable Godot version of a game idea, run in the editor to gather basic information and decide whether full development is worthwhile. Its code is not presumed suitable for production.
_Avoid_: Web mockup, HTML prototype, production foundation

**Prototype Run**:
One Operator-framed effort that produces one or more comparable Prototypes while preserving earlier runs for later reference.
_Avoid_: Numbered round, development cycle

**Production Game**:
A professionally implemented Game Project developed after its prototype is approved. Proven gameplay may carry forward, but prototype code is kept only when it meets production standards.
_Avoid_: Polished prototype, real project

**Development Cycle**:
One proposed set of changes and its result, ending with explicit Operator approval before another cycle begins.
_Avoid_: Autonomous loop, iteration

**Asset Library**:
The Operator-maintained local collection of prepared, reusable assets. Source assets remain unchanged; a Game Project receives independent copies selected for its needs.
_Avoid_: Project asset folder, generated assets

**Internal Project Name**:
The stable working identity used to create and locate a Game Project before its eventual public game title is chosen.
_Avoid_: Final title, game title

**Asset Request**:
A request from the Builder for an image, sound, model, or other creative asset that the Operator must provide before dependent work proceeds.
_Avoid_: Placeholder generation
