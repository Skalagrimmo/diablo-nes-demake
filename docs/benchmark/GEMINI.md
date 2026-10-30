# Participant addendum — Gemini

**Role:** independent implementation contestant. This is separate from Google AI Studio's Kotlin/Android submission. Do not reuse or inspect that submission.

Read [COMMON-PROMPT.md](COMMON-PROMPT.md) and the shared brief first. All common requirements and scoring weights apply.

## 1. Establish the exact starting point

Use only:
- baseline commit: `dd1a795cebb12366fd3d6062e4d33c177415ba9b`;
- baseline archive: https://github.com/Skalagrimmo/diablo-nes-demake/archive/refs/heads/benchmark/baseline-2026-10-30.zip;
- common brief: https://github.com/Skalagrimmo/diablo-nes-demake/blob/66b5c97098400a447ac8fe65d43477ee50a5c8d5/docs/AI-BENCHMARK-BRIEF.md.

Before implementation, confirm what source files you have actually read. If you cannot download or extract the ZIP, say so immediately and request the exact baseline source file(s) as an upload. Do not treat the repository README, architecture notes or brief as a substitute for source inspection. Do not silently build a fresh game from the brief and claim that you evolved the baseline.

In your initial response, provide a compact source-inspection report:
- exact files opened;
- whether the actual baseline `index.html` was read in full;
- any files or assets missing;
- a short description of the baseline's current architecture and systems, grounded in source.

Do not spend many turns retrying a failing archive URL. Use a directly supplied source file if available.

## 2. Implementation expectations

Build a genuinely playable evolution of **The Last Reactor**, following the common brief. You may select the stack that is best supported by your available environment. Do not assume you must use the same stack as another participant.

A browser-first implementation is acceptable when that produces the most reliable, portable deliverable. A multi-file project is welcome if all files can be delivered and launched reproducibly. You may use a game engine if you can provide its complete project and prove the build path.

Avoid a code-only answer that contains placeholders such as `// game code here`, omitted sections, pseudocode or instructions for the user to finish implementation. If your interface cannot create a repository or downloadable project, provide every required source file in clearly named, complete artifacts.

## 3. Work in verifiable milestones

Use a compact workflow:

1. Inspect the supplied baseline and identify what will be retained, refactored or replaced.
2. Build a minimal end-to-end playable slice early.
3. Add the industrial-fantasy setting, enemy behaviours, progression, one world-state mechanism and a major encounter.
4. Add and validate touch controls, save/continue and responsive scaling.
5. Run the available checks and prepare the delivery package.

Do not spend the entire task generating a long plan. Equally, do not skip source inspection or claim that features exist before implementing them.

## 4. Technical quality gates

Pay particular attention to:
- reachable map topology: prove that every required valve, key, lift, route and boss can be reached in the intended order;
- collision and interaction ranges;
- time-based movement and simulation rather than frame-rate-dependent behaviour;
- correct save/load restoration of both player data and world state;
- restart/new-game logic resetting every relevant state field;
- touch controls that support simultaneous movement and action where intended;
- browser lifecycle, resize and input cleanup;
- no required external services, remote assets or accounts.

Add small automated checks for critical pure logic where practical. At minimum, perform a static review of map connectivity and state transitions. A syntactically valid script is not proof that the game is playable.

## 5. Testing integrity — mandatory

Never invent test execution, screenshots, browser sessions, Android-device tests, performance measurements or build results.

For every check, use one of:
- **PASS — observed:** you actually ran it and observed the result;
- **FAIL — observed:** you actually ran it and observed a failure;
- **NOT RUN:** you did not execute it;
- **BLOCKED:** the environment prevented execution.

If you cannot launch a browser or device, say so. You may provide code-level reasoning as analysis, but label it as analysis rather than a test result. Do not report a manual playthrough unless it actually occurred in an available runtime.

## 6. Required delivery

Provide:
- complete source project and required assets;
- exact launch/build instructions;
- design and architecture notes;
- changelog and known issues;
- test matrix with PASS / FAIL / NOT RUN / BLOCKED statuses;
- asset provenance and licenses;
- real gameplay screenshots/recording only if captured from an actual run;
- a final note separating implemented, observed and unverified features.

The first delivery must be frozen independently before you inspect or reuse any other participant's work.
