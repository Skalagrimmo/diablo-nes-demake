# Common prompt — The Last Reactor

You are participating in an independent game-development benchmark.

## Inputs you must use

1. Baseline source archive: https://github.com/Skalagrimmo/diablo-nes-demake/archive/refs/heads/benchmark/baseline-2026-10-30.zip
2. Baseline commit: `dd1a795cebb12366fd3d6062e4d33c177415ba9b`
3. Shared design and acceptance brief: https://github.com/Skalagrimmo/diablo-nes-demake/blob/66b5c97098400a447ac8fe65d43477ee50a5c8d5/docs/AI-BENCHMARK-BRIEF.md

Read the complete shared brief before implementation. Treat the baseline as the common starting point and the brief as the authoritative requirements.

## Your task

Create an independently playable evolution of the supplied game under the working title **The Last Reactor**. The creative direction is gothic industrial fantasy: a fortified city built around an ancient alchemical reactor, now damaged and operating uncontrollably. The game should combine exploration, encounters, rewards, character development, environmental mechanisms and story discovery.

This must become a distinct game, not just a palette swap or a generic Diablo clone. Give the setting a recognizable visual identity and make its machinery and alchemy matter to play.

## Rules for a fair comparison

- Work only from the supplied baseline archive and shared brief.
- Do not inspect, reuse, or request another participant's implementation.
- Do not assume hidden context from previous conversations. Treat this as a fresh, self-contained task.
- You may refactor or replace the implementation where justified, but preserve the player-facing value of existing systems. Document deliberate removals or substitutions.
- Do not claim a feature works unless it is implemented and checked.
- Do not claim Android/mobile, performance, offline or save compatibility unless tested. State the exact device/browser/emulator and test method where applicable.
- Do not add paid services, required accounts, analytics, network dependencies or remote assets.
- Identify third-party assets and their licenses/sources. Prefer original, generated-at-build-time or clearly licensed assets.
- Do not spend the entire task on planning. Deliver a playable build, then document the remaining work.

## Minimum expected gameplay

Deliver a coherent, playable vertical slice that includes:
- character movement and responsive primary controls;
- at least two enemy behaviours that are meaningfully different;
- combat or another clear encounter-resolution mechanic;
- rewards and at least one meaningful character/equipment progression choice;
- at least one environmental interaction that changes access or world state;
- at least one boss or major encounter;
- a save/continue path or an explicitly justified equivalent;
- a distinctive district of the industrial city, with at least one visible route or landmark that makes the world feel connected;
- desktop keyboard controls and usable mobile touch controls, unless the participant-specific addendum specifies a native platform implementation—in that case native touch input is required.

You may retain more of the baseline campaign and systems. A smaller complete and polished slice is preferable to a broad but broken feature list.

## Delivery package

Provide:
1. Full source project and all required assets.
2. Exact launch/build instructions from a clean checkout.
3. A short design note and architecture overview.
4. Changelog: what was added, changed, removed and why.
5. Test report separating passed tests, failed tests and untested areas.
6. Known issues and next steps.
7. Screenshots or a short recording of actual gameplay.
8. Asset/source/license notes.

## Final response format

At the end, report:
- project/archive/repository location;
- exact entry point and build/run command;
- what is genuinely playable;
- tests actually performed and their environment;
- important limitations;
- the three strongest features and three biggest weaknesses.

The common evaluation rubric is in the shared brief. Do not optimize for superficial feature count. Optimize for a stable, expressive and reproducible game.
