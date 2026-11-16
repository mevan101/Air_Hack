---
name: Air Hackathon 2027
description: A dark, precise product page whose product is Dhaka's live air.
colors:
  bg: "#08090a"
  bg-raised: "#0e0f11"
  bg-raised-2: "#141518"
  ink: "#f4f5f6"
  ink-2: "#9ba1ab"
  ink-3: "#737983"
  line: "rgb(255 255 255 / 0.08)"
  line-2: "rgb(255 255 255 / 0.14)"
  line-3: "rgb(255 255 255 / 0.24)"
  safe: "#8fdcc2"
  smog: "#e4a660"
  cedar: "#2e7a46"
  aqi-good: "#3fae5a"
  aqi-moderate: "#e3c11d"
  aqi-sensitive: "#f08a24"
  aqi-unhealthy: "#e0403a"
  aqi-very-unhealthy: "#9b59b6"
  aqi-hazardous: "#a3283f"
typography:
  display:
    fontFamily: "Mona Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(3rem, 1.4rem + 6.4vw, 6rem)"
    fontWeight: 620
    lineHeight: 0.98
    letterSpacing: "-0.038em"
  headline:
    fontFamily: "Mona Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 1.5rem + 2.8vw, 3.75rem)"
    fontWeight: 600
    lineHeight: 1.02
    letterSpacing: "-0.035em"
  statement:
    fontFamily: "Mona Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 1.1rem + 2.5vw, 3.25rem)"
    fontWeight: 560
    lineHeight: 1.2
    letterSpacing: "-0.028em"
  body:
    fontFamily: "Mona Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "0em"
  label:
    fontFamily: "Mona Sans, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0em"
  bangla-display:
    fontFamily: "Anek Bangla, Noto Sans Bengali, sans-serif"
    fontSize: "min(12.5rem, 17vw)"
    fontWeight: 600
    lineHeight: 1.05
    letterSpacing: "0em"
rounded:
  s: "6px"
  m: "10px"
  l: "16px"
  pill: "999px"
spacing:
  gutter: "max(20px, min(5vw, 56px))"
  cell: "clamp(20px, 2.4vw, 32px)"
  section: "clamp(96px, 14vh, 160px)"
  max-width: "1200px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.bg}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "#ffffff"
  button-ghost:
    backgroundColor: "rgb(8 9 10 / 0.4)"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "44px"
  panel:
    backgroundColor: "{colors.bg-raised}"
    rounded: "{rounded.l}"
    padding: "{spacing.cell}"
  tab-selected:
    backgroundColor: "{colors.bg-raised-2}"
    textColor: "{colors.ink}"
  chip:
    textColor: "{colors.ink-2}"
    rounded: "{rounded.pill}"
    padding: "6px 10px"
---

# Design System: Air Hackathon 2027

## Overview

The category standard played straight, at the craft level of Linear, Vercel and Apple product pages: one near-black world, one typeface, hairline structure. The "product" on show is Dhaka's live air. A full-screen WebGL sky (a layered Dhaka skyline under smog whose density comes from the live PM2.5 reading) sits behind the hero and the pinned 48-hour section; every other section is opaque `bg`. The page refuses neon glows, gradient blobs, glass cards, countdowns, sponsor walls and eyebrow labels.

## Colors

- **Ground and ink:** `bg` #08090a carries every section. `bg-raised` and `bg-raised-2` lift panels and the selected tab. Text is `ink`, secondary text `ink-2` (7.4:1), tertiary meta `ink-3` (4.6:1, meta only, never on `bg-raised-2`).
- **Structure:** hairlines in `line` / `line-2` / `line-3`, white at 8 / 14 / 24 % opacity.
- **Colour only ever encodes data.** `smog` amber marks pollution figures, `safe` mint marks the WHO guideline line and safe air, and the six US EPA AQI band colours mark readings. Nothing decorative is coloured. `cedar` green appears only inside the Cedar Initiative logo.

## Typography

Mona Sans for every Latin line, using its width axis for display (`font-stretch` 102 to 104 %). Display headlines run tight (-0.038em) and stay on two lines. Section headlines use `headline`; the scroll-lit paragraph uses `statement`. Body copy is 17 px at 1.55. Tabular figures only on numbers that tick (the breath counters); Mona's tabular zero is dotted, so static figures stay proportional. Anek Bangla appears once, for the closing line "নির্মল বাতাস", loaded as a subset of only those characters.

## Layout

A 1200 px column with a fluid gutter. Every section after the hero is one or two screens tall with generous block padding (`section`). Data sits in a 12-column hairline grid inside a rounded panel: cells are separated by 1 px rules, never by gaps or shadows. The hero is exactly one viewport: headline upper left, the airship in the right half below the moon, and a live readings bar pinned to its bottom edge. The 48-hour section is 400 vh with a sticky viewport. Below 1000 px, grids collapse to one column and the tab list becomes three horizontal tabs. Below 720 px, the live bar becomes a 3-cell grid (AQI, PM2.5, WHO multiple) with Pause as its own row.

## Elevation & Depth

Depth comes from the WebGL sky and from surface steps (`bg` → `bg-raised` → `bg-raised-2`), not from shadows. The only shadows are on floating UI: the command menu (0 24px 64px -16px black 70 %) and the example alert card. The nav gains a blurred `bg` at 82 % only once the page scrolls, for legibility over the sky.

## Shapes

Radii: `s` 6 px for small boxes, `m` 10 px for menu rows, `l` 16 px for panels and the dialog, `pill` for buttons and chips. Nested radii stay concentric (menu rows at 10 px inside 6 px padding in a 16 px dialog). Circles mark points in data (AQI dot, timeline markers, scrub head).

## Components

- **Buttons:** primary is solid `ink` on `bg`, ghost is a hairline pill. Both are 44 px tall, press to `scale(0.96)` in 160 ms, and change colour on hover only for `(hover: hover) and (pointer: fine)`. Labels are Title Case, following Vercel's Web Interface Guidelines.
- **Live readings bar:** hairline cells, label in `label` style over a 15 px value, with the global Pause control at the end.
- **Data panel:** the hairline grid described in Layout; the big AQI figure is a proportional 9rem numeral.
- **Tabs:** ARIA tabs with arrow keys and Home/End. Selection is shown by `bg-raised-2` plus `ink`; on mobile, by a 2 px bottom rule. Each tab carries a title and a one-line description, never a label above it.
- **Timeline:** a hairline with three markers; the current stage's marker is filled `ink`, and the rest are outlined with `ink-2` headings.
- **Command menu (Cmd/Ctrl+K):** a native dialog with combobox and listbox semantics. It opens and closes with no animation because it is keyboard-triggered.
- **Motion:** one authored entrance (the sky resolves from black and headline characters rise in sequence, 22 ms apart, ease `cubic-bezier(0.16, 1, 0.3, 1)`). The statement lights word by word with scroll; the 48-hour scrub drives the sky. Every other transition is ≤ 240 ms ease-out. Everything pauses with the global Pause control and starts paused under `prefers-reduced-motion`.

## Do's and Don'ts

- Do let live data drive the visuals (sky density, chart, alert copy). Don't use demonstration numbers without labelling them illustrative.
- Do keep colour for data. Don't add accent colour to decoration, gradients outside the WebGL sky, or glows.
- Do separate grid cells with hairlines. Don't use cards-in-cards or drop shadows on in-page panels.
- Don't put eyebrow or kicker labels above headings, or a coloured side stripe on selected items.
- Don't animate keyboard-triggered UI, and don't gate meaning on motion; every animated state also has a static cue.
- Don't invent facts about the event: dates, venue, prizes and partners stay "not set yet" until they exist.
