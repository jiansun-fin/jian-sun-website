# CLAUDE.md — Jian Sun academic website

This repo is a **single-file static website** hosted on GitHub Pages at `www.jian-sun.com`.
The entire site is `index.html` (HTML + inline CSS + a small inline `<script>`). No build step, no framework, no dependencies.

## How to work on this repo

- Edit `index.html` directly. There is nothing to compile.
- To preview: open `index.html` in a browser, or use the VS Code **Live Server** extension (right-click `index.html` → "Open with Live Server") for auto-refresh on save.
- To publish: commit and push to `main`. GitHub Pages redeploys automatically (~1 minute).

## Design conventions — keep these consistent

**Aesthetic:** minimalist academic, restrained, precise. Design subtly echoes the field (market microstructure / market design): ordered, structured information; monospace used for metadata/labels.

**Color tokens** (defined as CSS variables in `:root`):
- `--ink: #16181d` — primary text
- `--ink-soft: #3d4048` — secondary text
- `--muted: #8b8983` — captions, meta
- `--paper: #fafaf8` — background
- `--line: #e4e2dc` — hairline rules
- `--accent: #2d4a6b` — deep slate-blue accent (links, journal tags, hover). This is the ONLY accent color; do not introduce new hues without asking.

**Typography:**
- `Fraunces` (serif) — display, titles, paper titles, intro prose
- `Inter` (sans) — body, author lines, UI
- `JetBrains Mono` (mono) — section numbers, labels, years, venue tags. The monospace metadata is the signature element — preserve it.

**Layout:** sticky left rail (name, role, nav, contact) + scrolling content column. Collapses to a stacked single column below 900px.

**Interactions:** nav link hover extends a short rule and turns accent-colored; active section highlights on scroll; publication rows show a left accent bar and shift right on hover; sections fade in on scroll (respect `prefers-reduced-motion`).

## Content structure

- **About** — intro (2 paragraphs) + research-interest tags
- **Research** — Publications (journal-tagged), then Working Papers
- **Teaching** — grouped by institution (SMU, then MIT as TA)
- **Contact** — email + education colophon (in the left rail)

## Editing rules

- Keep it a single self-contained file. Do not split into multiple files or add a framework/bundler.
- Paper titles: serif, italic where the existing pattern uses it. Journal names get the accent `venue-tag journal`; R&R gets `venue-tag rr`; unpublished gets `venue-tag wp`.
- When adding a publication, follow the existing `.pub` block markup exactly (title / authors / meta with the right venue tag).
- Maintain the quality floor: responsive to mobile, visible keyboard focus, reduced-motion respected.
- Keep the current professional tone. This is a public-facing academic profile.

## Facts to keep accurate

- Title: **Associate Professor of Finance (with tenure)**, Lee Kong Chian School of Business, Singapore Management University; courtesy appointment in the School of Economics.
- PhD: MIT Sloan, 2022. MS: Toulouse School of Economics. BS: Tsinghua (Economics + Mathematics).
- Email: jiansun@smu.edu.sg
