# Axiomancer: Table Edition — assets

Rendered card art for virtual tabletops, served by GitHub Pages.

**Sitemap: https://no-trbl-2-u.github.io/axiomancer-assets/**

Every virtual tabletop imports a deck the same way — one grid image plus its
column and row count, sliced in reading order. This repo is those images, plus
`manifest.json` describing each one's grid, cell size, back group and hash.

## Do not hand-edit

Everything here is generated. The source of truth is the (private)
`board-brainstorm` repo:

```bash
node render-kit.mjs --sheets    # render the sheets + manifest
node publish-assets.mjs         # build this repo's contents
```

## Filenames carry a content hash

`deck-malison.a1b2c3d4.png`. Tabletop Simulator caches by URL **permanently** —
republish changed art to the same filename and everyone who already loaded the
mod keeps the stale version, with no symptom. A content hash means a changed
sheet gets a new URL and refetches, while unchanged sheets keep theirs and stay
cached. The hash list also doubles as a changelog of which decks moved.

## Attribution

Icons by Lorc, Delapouite, sbed, Faithtoken, Heavenly Dog, Guard13007,
DarkZaitzev and Skoll from [game-icons.net](https://game-icons.net), licensed
[CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). The three die
quality faces (MISS / MANA / SPECIAL) are original to Axiomancer: Table Edition.
