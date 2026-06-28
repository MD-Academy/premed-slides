# MDA Premedical — Slide System

Modern, reusable Slidev decks for the MDA premedical pre-recorded material.
Design is defined **once** (theme + components) and content flows through it, so
each new topic is fast to produce and consistent with the rest.

## Structure

```
mda-premed-slides/
├── site/index.html         ← course landing page (lists every lesson)
├── .github/workflows/      ← builds all decks + index → GitHub Pages
└── decks/
    ├── 01-macromolecules-nucleic-acids/   → /nucleic-acids/   (13 slides)
    ├── 02-macromolecules-carbohydrates/   → /carbohydrates/   (15 slides)
    ├── 03-macromolecules-lipids/          → /lipids/          (15 slides)
    └── 04-macromolecules-proteins/        → /proteins/        (14 slides)
        ├── slides.md          ← all content
        ├── styles/theme.css   ← shared visual theme (colors, cards, tables, badges)
        ├── components/        ← custom copyright-free graphics (original SVG, Vue)
        │   └── Ic.vue              inline MDI icons (Apache-2.0)
        ├── global-top.vue     ← collapsible slide menu (per-deck TOC)
        └── global-bottom.vue  ← footer/branding on every slide
```

Live site: **https://md-academy.github.io/premed-slides/** (index → each lesson).

> Each deck is self-contained (proven, build-safe). `styles/theme.css` + `Ic.vue`
> are identical copies across decks; the diagram components and TOC are per-topic.
> A future cleanup may extract the shared parts into a local Slidev **addon**.

## Commands (run inside a deck folder)

```bash
npm install          # first time only
npm run dev          # live preview at localhost:3030
npm run build        # static site -> dist/
npm run export       # -> export/nucleic-acids.pdf
npm run export-png   # one PNG per slide -> export/png/
```

## Adding a new topic deck

1. Copy `decks/01-macromolecules-nucleic-acids/` to `decks/0N-<topic>/`.
2. Replace the content in `slides.md` (keep the layout patterns + theme classes).
3. Add any new topic-specific diagram to `components/`.
4. `npm install && npm run dev`.

## Graphics policy

- **Custom SVG components** for scientific diagrams (fully ours, copyright-free).
- **MDI icons** baked inline (`Ic.vue`) — Apache-2.0, free for commercial use.
- For AI-generated hero/concept art: drop images in a deck `assets/` folder and
  reference them in `slides.md`. (Prompts to be supplied per deck.)
