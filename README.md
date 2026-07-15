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
