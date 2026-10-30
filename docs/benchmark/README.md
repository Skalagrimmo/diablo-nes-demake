# AI benchmark — participant instruction pack

This folder contains the common task prompt and the participant-specific addenda.

## Fixed inputs

- **Baseline archive:** [baseline-2026-10-30 ZIP](https://github.com/Skalagrimmo/diablo-nes-demake/archive/refs/heads/benchmark/baseline-2026-10-30.zip)
- **Baseline commit:** `dd1a795cebb12366fd3d6062e4d33c177415ba9b`
- **Shared brief:** [AI-BENCHMARK-BRIEF.md at commit 66b5c97098400a447ac8fe65d43477ee50a5c8d5](https://github.com/Skalagrimmo/diablo-nes-demake/blob/66b5c97098400a447ac8fe65d43477ee50a5c8d5/docs/AI-BENCHMARK-BRIEF.md)

Every implementation participant must receive the same baseline archive and the same shared brief, plus only the relevant addendum below. Do not give implementation participants other participants' source or results before their first submission.

## Implementation participants

- [Common instructions](COMMON-PROMPT.md)
- [OpenCode + Nemotron](OPENCODE-NEMOTRON.md)
- [Google AI Studio — native Kotlin/Android](AI-STUDIO-KOTLIN.md)
- [Claude](CLAUDE.md)
- [DeepSeek](DEEPSEEK.md)
- [Mistral](MISTRAL.md)
- [Gameplay AI](GAMEPLAY-AI.md)

For each participant, paste the **Common instructions first**, then the matching addendum. The addendum adapts workflow and delivery to the tool; it does not change the shared game-design requirements or evaluation rubric.

## Independent review / validation

These are support roles, not implementation contestants:

- [Z.ai — blind reviewer](ZAI-REVIEW.md)
- [Harness — reproducible test and build validation](HARNESS-TEST.md)

Keep their reports separate from implementation submissions. The reviewer should not score a submission until the implementation and evidence package have been frozen.
