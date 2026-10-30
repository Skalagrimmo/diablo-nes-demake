# Archived initial AI benchmark submissions

This branch preserves the first exported outputs received on 2026-10-30. It is an archive, not a promoted or repaired build.

## Fixed baseline reference

- Baseline commit: `dd1a795cebb12366fd3d6062e4d33c177415ba9b`
- The branch was created from that exact commit.
- Neither `main` nor the frozen baseline branch is changed by this archive.

## Contents

- `deepseek/DeepSeek.json`: original full chat export.
- `deepseek/index.html`: complete HTML artifact from DeepSeek export entry `c5`.
- `deepseek/ASSESSMENT.md`: evidence-based initial review.
- `gemini/Gemini.json`: original full chat export.
- `gemini/index.html`: HTML artifact from Gemini export entry `c1`. Export entry `c2` is byte-identical and remains preserved in the raw JSON.
- `gemini/ASSESSMENT.md`: evidence-based initial review.

## Archive policy

The exports and extracted HTML files are preserved without fixes or editorial changes. Any later repair, continuation, or improved submission must be stored in a new revision/branch so that the initial attempts remain reproducible.

## Validation scope

JavaScript syntax was checked locally with Node.js 22.16.0 by extracting inline script content from each HTML file and running `node --check`. This is only a syntax check, not a browser gameplay test.
