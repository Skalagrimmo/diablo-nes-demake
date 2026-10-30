# Participant addendum — Claude

Read [COMMON-PROMPT.md](COMMON-PROMPT.md) and the shared brief first. All common requirements and scoring weights apply.

## Implementation focus

Produce a complete, self-contained playable browser game based on the supplied project. A single `index.html` with embedded CSS and JavaScript is acceptable and may be preferable when it makes the result easier to run and inspect. A small multi-file project is also acceptable if it includes every required file and clear instructions.

Do not return a design mockup, isolated code fragments or a partial HTML shell. The browser must be able to launch the game locally using the documented method.

Prioritize:
- preserving responsive controls and the core action loop;
- a strong and coherent industrial-fantasy visual identity at low resolution;
- clear enemy behaviours and encounter feedback;
- one meaningful machine/environment interaction;
- rewards and an understandable upgrade choice;
- save/continue and robust restart behaviour;
- mobile touch controls that do not interfere with keyboard play.

Avoid unrequested libraries, remote assets and network calls. If a browser security restriction requires a local server instead of opening the file directly, document the exact command.

## Delivery

Return the complete source tree or a repository/archive, plus run instructions, a concise architecture note, changelog, test report and actual gameplay evidence. Clearly identify which browser and device sizes were tested and which were not.
