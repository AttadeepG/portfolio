# Portfolio Project — Claude Instructions

## Token Optimisation Rules

- **Read only the targeted section** before editing. Never read the whole file; use `offset`+`limit` or `grep -n` to locate the exact lines first.
- **Edit, don't rewrite.** Use the Edit tool for surgical changes. Only use Write for full rewrites when explicitly asked.
- **No exploratory reads.** If a line number is already known from a grep result, go straight to Edit.
- **Skip confirmation prose.** No "I'll now…" or "Done!" summaries — just make the change and state what changed in one sentence.
- **Grep before Read.** Always `grep -n` for a symbol or string before opening the file to read context.
- **No whole-file dumps.** Never read or output the entire `index.html` — it is ~1800 lines and blows the context window.

## Project Facts

- Single-file portfolio: `index.html` (~1800 lines, React/JSX compiled in-browser via Babel).
- Edit password: `portfolio2026` (set at `const EDIT_PASSWORD` near line 1322).
- All content lives in `const PROFILE`, `const PROJECTS`, `const TESTIMONIALS`, `const CLIENTS`, `const POSTS` near lines 450–600.
- Tweaks panel toggled via the `✏ Edit` FAB — password required.
- Deploy: GitHub Pages via the Deploy tab inside the editor panel.
- `portfolio.html` is a backup/source copy; `index.html` is the live file.

## What NOT to do

- Do not add hardcoded `height` or fractional `padding` values to JSX style props — they break layout across viewports.
- Do not add comments unless the WHY is non-obvious.
- Do not install packages or create new files unless asked.
