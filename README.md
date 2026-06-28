# MDA Premedical — Slide System

Modern, reusable Slidev decks for the MDA premedical pre-recorded material.
Design is defined **once** (theme + components) and content flows through it, so
each new topic is fast to produce and consistent with the rest.

## Structure

```
mda-premed-slides/
└── decks/
    └── 01-macromolecules-nucleic-acids/   ← the pilot deck (template to clone)
        ├── slides.md          ← all content (13 slides)
        ├── styles/theme.css   ← shared visual theme (colors, cards, tables, badges)
        ├── components/        ← custom copyright-free graphics (SVG, Vue)
        │   ├── DnaHelix.vue        animated colored double helix
        │   ├── Nucleotide.vue      phosphate–sugar–base schematic
        │   ├── RingStructure.vue   purine / pyrimidine rings
        │   └── Ic.vue              inline MDI icons (Apache-2.0)
        ├── global-bottom.vue  ← footer/branding on every slide
        └── export/            ← generated PDF + PNGs
```

> The pilot deck is self-contained. When deck 2 is added, the `styles/` +
> `components/` will be extracted into a shared local Slidev **addon** so all
> decks share one source of truth (no copy-paste drift).

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
