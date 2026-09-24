# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

- Add durable project-specific notes here as they are discovered through real work.
- Every mock's `style.tex` (question-paper and marking-scheme) must load `\usepackage[T1]{fontenc}` before `\usepackage{helvet}`. LuaLaTeX (used by `.github/workflows/compile-mocks.yml`) defaults to the `TU` font encoding, under which classic PostScript font packages like `helvet` (and previously `mathptmx`) have no defined shapes; without `T1`, `\sffamily`/`\familydefault{\sfdefault}` silently falls back to Latin Modern instead of Helvetica, with only an easy-to-miss "Font shape ... undefined" warning in the log. Always confirm font changes with `pdffonts main.pdf` (should show `NimbusSanL-*`, never `Times`/`NimbusRomNo9L`), not just a clean compile.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
