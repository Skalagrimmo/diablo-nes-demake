# Participant addendum — OpenCode + Nemotron (PC toolchain)

Read [COMMON-PROMPT.md](COMMON-PROMPT.md) and the shared brief first. All common requirements and scoring weights apply.

## Workflow expectations

You are operating as a coding agent on a PC with a local development environment. Inspect the supplied project before changing it: map its entry points, game loop, input, rendering, audio, save logic and current gameplay systems. Make a short implementation plan, then start building rather than producing a long proposal.

The environment may include GameMaker, Tiled, Git and command-line tools. You are free to use them, but do not force a tool into the project merely because it is installed.

- GameMaker is acceptable if the project can be built and run reproducibly with the available installation and its licensing/export conditions are documented.
- Tiled may be used for authored city districts. Include editable map sources and the runtime representation/parser, or provide a reproducible export step.
- A modular JavaScript/Canvas solution is also acceptable if it offers the strongest complete result and reliable mobile support.
- Do not assume that a paid or unavailable Android export module is present. Verify the actual export pipeline before making it a dependency.

## Working method

- Create a separate working directory or branch for this submission.
- Inspect and test the baseline before modifying it.
- Prefer small, testable milestones: controls and scene; one district; one encounter; reward/progression; mechanism; boss; save; mobile validation.
- Use Git commits with clear messages so changes can be audited.
- Run syntax, build and smoke tests after meaningful changes.
- Keep generated files and temporary exports out of the source unless required.
- Do not overwrite the original baseline archive.

## Extra deliverables

Include a short technical decision record explaining:
- why you selected the engine/runtime;
- how maps and game data are represented;
- how input, simulation, rendering, audio and persistence are separated;
- how a future Android build would work, including any licensing or tooling constraints.

Provide exact commands to launch and build the project. Include the actual project files, not only screenshots or an executable.
