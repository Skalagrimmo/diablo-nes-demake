# AI Benchmark Brief v1 — The Last Reactor

**Status:** concept and implementation challenge, version 1  
**Baseline repository:** `Skalagrimmo/diablo-nes-demake`  
**Baseline commit:** `dd1a795cebb12366fd3d6062e4d33c177415ba9b`  
**Baseline snapshot:** `benchmark/baseline-2026-10-30`

## 1. Purpose

Build an independent, playable evolution of the supplied dungeon-crawler prototype. This is a comparative engineering and game-design experiment: every participant receives the same baseline and this exact brief. Participants must work independently and must not inspect other participants' submissions before their first delivery.

Do not merely reskin Diablo or reproduce a generic retro platformer. Preserve the satisfying exploration–encounter–reward–progression loop while giving the game a distinct identity.

## 2. Working concept

**Working title: The Last Reactor**

A vast fortified city was built around an ancient alchemical reactor. For generations, the reactor powered workshops, lifts, heating systems, foundries and civic infrastructure. After a catastrophic failure, it continued operating in an uncontrolled state. The city has become an unstable labyrinth of abandoned districts, sealed laboratories, industrial machinery and older ruins beneath its foundations.

The player explores the city, discovers what happened, gathers equipment and alchemical materials, restores or bypasses parts of its infrastructure, and eventually reaches the reactor.

This is a working direction, not a demand for a fixed plot. Participants may improve names, lore and presentation, but should retain the central identity: **gothic industrial fantasy, alchemy, a decaying vertical city, and a mysterious reactor at its heart.**

### Visual language

- Gothic stonework, fortified streets, towers, chapels and monumental civic architecture.
- Foundries, pipes, pressure valves, lifts, gears, boilers, cable runs and mechanical workshops.
- Alchemical laboratories, glass vessels, formulae, strange energy conduits and aged instruments.
- Strong readable silhouettes and restrained palettes suitable for small screens and low-resolution rendering.
- An atmospheric sense of scale without relying on expensive effects or high-resolution assets.

Avoid generic steampunk decoration without gameplay purpose. Machinery should help explain the world and, where feasible, participate in play.

## 3. Core gameplay pillars

1. **Explore:** navigate connected districts, rooms, corridors and vertical routes.
2. **Encounter:** fight readable enemy types with distinct behaviours and clear feedback.
3. **Acquire:** find equipment, currency, consumables and alchemical reagents.
4. **Develop:** improve the character through levels, equipment and meaningful build choices.
5. **Interact:** operate mechanisms, unlock routes, restore power or alter environmental hazards.
6. **Uncover:** reveal the history of the city through short events, locations and boss encounters.

A successful version should make exploration and interaction matter alongside combat.

## 4. World structure

Use a multi-layered city rather than six unrelated dungeon floors. The following zones are a suggested progression, not a mandatory exact map:

1. **Upper City:** fortified streets, civic buildings, chapels and abandoned residential blocks.
2. **Industrial Belt:** foundries, workshops, boilers, production halls and freight lifts.
3. **Sealed Laboratories:** research chambers, alchemical storage and experimental machinery.
4. **Substructure:** waterworks, mines, ventilation, service tunnels and transit infrastructure.
5. **Buried Ruins:** remnants of the civilization beneath the city.
6. **Reactor Complex:** the central mechanism and the source of the disaster.

At least some routes should communicate spatial continuity: lifts, stairs, shafts, gates, shortcuts or revisited hubs. Procedural generation is welcome, but handcrafted landmarks and navigable structure should prevent the world from feeling interchangeable.

## 5. Systems to preserve or evolve

The supplied prototype already contains a useful starting set. Do not remove a working system without replacing its player-facing value.

- Three distinct playable archetypes (currently Warrior, Rogue and Sorcerer), or a clearly justified equivalent.
- Distinct combat styles and readable hit/ability feedback.
- Multiple enemy types with different movement or attack behaviours.
- Boss encounters with recognizable patterns.
- Character progression, experience and levels.
- Equipment, rarity, inventory and meaningful equipment choices.
- Consumables and a reward loop.
- Save/continue and a reliable restart path.
- Mobile touch controls as well as keyboard controls.
- Procedural or semi-procedural replayable spaces.
- Audio feedback and a coherent sound identity.

### New systems encouraged

- Alchemical reagents and recipes with a small, understandable set of combinations.
- Environmental mechanisms: switches, pressure valves, generators, powered doors and lifts.
- Persistent world changes, such as restoring a lift or opening a shortcut.
- Distinct district hazards and environmental puzzles.
- Optional discoveries and compact narrative events.

Do not add complexity merely to increase feature count. Each new system should be demonstrable in play.

## 6. Platform and performance targets

The reference experience is a browser game that should remain practical on modest Android hardware.

- Primary target: modern desktop browser and Android mobile browser.
- Touch controls must be usable with thumbs and must not obscure essential information.
- Keyboard support should remain available.
- Aim for a stable, responsive experience on low- to mid-range phones; avoid unnecessary per-frame allocations, huge textures and expensive full-screen effects.
- Offline/self-contained launch is strongly preferred. If external assets or services are required, document them and provide a fallback where practical.
- Keep the internal resolution and pixel-art approach if useful, or justify a different low-cost rendering strategy.
- Do not claim Android compatibility, performance, or offline operation without actually testing it.

The baseline is a single-file HTML/CSS/JavaScript Canvas 2D game with Web Audio synthesis and localStorage saves. Participants may keep this architecture or replace it. A multi-file project, engine-based implementation, or other stack is acceptable if the submission is complete, reproducible and suitable for the target devices.

This is not a requirement to produce a genuine NES ROM or emulate NES hardware. Retro presentation is a design constraint, not a demand for cycle-accurate hardware emulation.

## 7. Technical freedom and constraints

Participants may choose their own tools and architecture, including but not limited to vanilla JavaScript/Canvas, a game engine, modular HTML/JS, or a cross-platform approach.

- Do not depend on paid services or inaccessible proprietary assets.
- Identify all third-party assets and their licenses or sources.
- Keep game logic, rendering, input, audio and content data reasonably separated where the chosen stack permits.
- Provide a clear entry point and exact launch/build instructions.
- Include source code; a binary-only delivery is not sufficient.
- Do not silently remove baseline features. List deliberate changes and explain why.
- Avoid unnecessary rewrites of working systems if a smaller, safer improvement is possible.

## 8. Required deliverables

Each participant must provide:

1. A complete playable project, not isolated code snippets or mockups.
2. All source files and required assets.
3. A concise README with exact launch/build instructions.
4. A short design note explaining the game loop, world structure and key decisions.
5. An architecture note describing major modules and data flow.
6. A changelog listing additions, removals and known limitations.
7. A test report distinguishing tests actually performed from tests not performed.
8. Evidence of play on desktop and, where available, Android (screenshots, short recordings or reproducible test notes).
9. Asset/source/license notes.
10. A short list of the three strongest features and three largest remaining weaknesses.

A submission that cannot be launched from its instructions is incomplete, even if its source looks promising.

## 9. Minimum acceptance checklist

- [ ] The project launches from the documented entry point.
- [ ] A new game can be started and completed through a meaningful playable loop.
- [ ] Player movement and primary actions work.
- [ ] Enemies can be encountered and defeated or otherwise overcome.
- [ ] At least one meaningful reward or progression mechanic works.
- [ ] At least one environment interaction changes access, state or player options.
- [ ] At least one boss or major encounter exists.
- [ ] Save/continue works, or a clearly documented equivalent is implemented.
- [ ] Touch controls are present and usable on a phone.
- [ ] Keyboard controls are present.
- [ ] The game communicates damage, interaction and important state changes clearly.
- [ ] No known blocker prevents ordinary play through the submitted slice.
- [ ] Documentation accurately describes what was and was not tested.

The minimum can be a polished vertical slice rather than a huge unfinished campaign. A smaller complete experience is better than a large collection of nonfunctional systems.

## 10. Evaluation rubric

Score each category from 0 to 10, then apply the weight.

| Category | Weight |
|---|---:|
| Playability and functional completeness | 20% |
| Compliance with the brief and preservation of core pillars | 15% |
| Architecture, code clarity and maintainability | 15% |
| Mobile usability and low-end performance | 15% |
| Gameplay depth and meaningful system design | 10% |
| Visual and audio identity | 10% |
| Robustness and quality of test evidence | 10% |
| Documentation and reproducibility | 5% |
| **Total** | **100%** |

Reviewers should distinguish observed behaviour from claims in documentation. Missing evidence is not proof of failure, but it should not receive the same confidence as a reproducible test.

## 11. Fair-comparison protocol

- Use the same baseline snapshot and the same unmodified copy of this brief.
- Work in isolated branches, forks or project folders.
- Do not view competing submissions before the first delivery.
- Record the tools/model and approximate workflow used.
- Record substantial prompts or task instructions so the result can be reproduced.
- Do not merge code or assets between participants before the first comparison.
- Submit the complete project and test evidence together.
- After the independent comparison, selected ideas may be combined in a separate integration phase.

## 12. Final objective

The best result is not necessarily the largest or most technically elaborate project. It is the most convincing playable game: a distinctive world, a coherent loop, responsive controls, meaningful systems, reliable operation and an architecture that can be developed further.
