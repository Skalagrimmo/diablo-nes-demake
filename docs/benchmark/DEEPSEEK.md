# Participant addendum — DeepSeek

Read [COMMON-PROMPT.md](COMMON-PROMPT.md) and the shared brief first. All common requirements and scoring weights apply.

## Implementation focus

Deliver a maintainable and testable game project rather than a large monolithic code dump. You may choose the implementation stack that best fits a complete, offline-capable desktop and mobile experience. Explain the choice briefly and do not depend on paid services or unavailable export tooling.

Pay particular attention to:
- clear separation of simulation/game rules from rendering and input;
- data-driven definitions for enemies, equipment, items and district features;
- deterministic or reproducible procedural generation where practical;
- save data versioning and safe loading of missing/older fields;
- responsive touch and keyboard input;
- a small set of tests for core rules such as damage, rewards, equipment effects, world interactions and save/load.

Do not over-engineer with abstractions that do not improve the delivered game. A playable vertical slice must be present early and remain runnable throughout development.

## Delivery

Include the full source project, build/run instructions, architecture and data-model notes, changelog, test report and actual gameplay evidence. Provide exact test commands and distinguish automated tests from manual play checks.
