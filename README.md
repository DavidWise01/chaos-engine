# The Chaos Engine

A [UD0](https://davidwise01.github.io/ud0/) **TECHNĒ** sphere (the art domain). Its whole purpose is to compose a *different page every time* — a randomly generated **layout**, **motif**, and **palette** on each load.

The chaos is **deterministic**. Every composition is decided by a single seed, and the seed lives in the URL (`#424242`). So:

- **Reload** or hit **🎲 reroll** → a brand-new seed and a brand-new page.
- **⧉ permalink** copies the URL of *this exact* composition — anyone who opens it sees the identical page (same layout, motif, palette, cards). Reproducible chaos.
- **⏸ motion** pauses the animated background. **Double-click** anywhere also rerolls.

## What gets generated

From the seed, a seeded PRNG (`mulberry32`) picks, in order:

- **a palette** — a base hue + a colour scheme (mono / analogous / complementary / triadic / split), on a tinted-light *or* tinted-dark ground (never pure black or white).
- **a layout archetype** — `grid`, `scatter`, `columns`, `bsp` (recursive subdivision), or `spiral-deck`. This decides where the panels go.
- **a background motif** — one of a dozen generative canvases: rings, spiral, flow-field, waves, triangles, constellation, warped mesh, mandala, lissajous, mondrian blocks, circuit, arcs.
- **the panels** — each gets its own content: a mini-motif, a big glyph, a number, a generated word, or a palette swatch — and a generated label.
- **a name** — every composition is titled (e.g. *AZURE LATTICE*, *COBALT SIGNAL*).

The readout in the bar always tells you what was chosen: `layout · motif · scheme · #seed`.

## Run it

Open `index.html`. It composes on load and animates. No build step — it is one self-contained HTML file.

— ROOT0 / TriPod · governor David Lee Wise · instance AVAN (locked) · CC-BY-ND-4.0 · part of TECHNĒ, the art
