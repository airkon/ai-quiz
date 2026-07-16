# The Kaki Trek

A mobile-first, single-file HTML quiz prototype — an AI fluency self-check
disguised as an island adventure. Built to be played on phones via QR code at
a company townhall.

## Run it

Open `index.html` in any modern browser. There is no build step, no server,
and no external requests — everything (markup, styles, logic, content) lives in
that one file.

```
open index.html
```

## Editing content

All copy, questions, options, scores, personas and tips live in a single
commented `DATA` object at the top of the `<script>` in `index.html`. Edit text
there without touching the app logic below it.

## Illustrations

Illustrations are placeholders: dashed-border boxes labelled with an ID and the
intended content (e.g. `ill-story-boat`). Each is one element you can later
swap for an `<img>` without touching anything else.

The hero screens (landing + the three story beats) use a **full-bleed
background** with a floating cream content card near the bottom, so those
assets are edge-to-edge (`object-fit: cover`) and their bottom ~45% sits behind
the card — keep the focal subject in the upper-middle. Questions + the tally
share one faint background asset (`ill-bg-jungle`). Results uses an
edge-to-edge persona hero band (`ill-persona-1…6`, subject in the top half)
with the results card overlapping its bottom edge.

**Asset spec (design at 430px wide, export @2x and @3x):**

| Asset | Where | Treatment |
|---|---|---|
| `ill-landing`, `ill-story-boat`, `ill-story-pack`, `ill-story-kaki` | landing + story | full-bleed ~9:19.5; subject upper-middle; bottom ~45% behind card |
| `ill-ch1` … `ill-ch8` | each chapter's scene screen | full-bleed ~9:19.5; subject upper-middle; bottom ~45% behind card |
| `ill-bg-jungle` | all 8 question screens + tally | one faint/desaturated full-bleed backdrop |
| `ill-persona-1` … `ill-persona-6` | results | edge-to-edge 4:3 hero band; subject in top half |

Each chapter is now told over two screens: a **scene-setter** (`ill-chN` + the
scene text) and then the **question** (prompt + options, with the scene text
repeated faintly as a light-grey recap). The `ill-chN` art therefore uses the
same full-bleed hero treatment as the landing/story backgrounds.

## Design notes

- Mobile-first, ~390px, centered phone column with a sunset backdrop on larger screens.
- Tropical palette: jungle greens, sandy tones, sunset accents.
- Directional slide transitions between screens; staggered/idle motion on story
  and question screens; a drawn trail on the tally screen; a persona-stamp reveal
  with a leaf-fall burst on results.
- Respects `prefers-reduced-motion` (animations fall back to simple fades).

## What it measures

An island costume for Anthropic's AI Fluency Framework — Delegation,
Description, Discernment, Diligence — mapped loosely onto AISA fluency tiers.
Light-touch and just for fun, not a formal assessment.
