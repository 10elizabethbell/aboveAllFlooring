---
name: Above All Flooring
description: Basement carpet pitch site. The page is the finished basement from their own photo.
colors:
  wall: "#1d2943"
  wall-2: "#253353"
  wall-3: "#33426a"
  line: "#7a8497"
  trim: "#efebe4"
  trim-shade: "#dcd6cc"
  ink: "#ece7de"
  ink-soft: "#bcc3d2"
  ink-faint: "#98a1b3"
  carpet: "#c4b6a6"
  chalk: "#7fb6ff"
  err: "#ffb4a8"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.7rem, min(12.4vw, 15svh), 6rem)"
    fontWeight: 900
    lineHeight: 0.98
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2rem, 8.5vw, 3.6rem)"
    fontWeight: 900
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(20px, 5.6vw, 28px)"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: "0.01em"
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 20px)"
    fontWeight: 400
    lineHeight: 1.55
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 800
    lineHeight: 1
  small:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "13.5px"
    fontWeight: 700
    lineHeight: 1.1
rounded:
  swatch: "9px"
  field: "10px"
  button: "12px"
  panel: "14px"
  round: "50%"
spacing:
  pad: "clamp(16px, 5vw, 48px)"
  tight: "8px"
  gap: "12px"
  stack: "24px"
  sec-head: "28px"
  section: "56px"
  section-desktop: "80px"
  gutter: "64px"
components:
  button-fill:
    backgroundColor: "{colors.trim}"
    textColor: "{colors.wall}"
    typography: "{typography.label}"
    rounded: "{rounded.button}"
    padding: "0 24px"
    height: "56px"
  button-fill-hover:
    backgroundColor: "{colors.chalk}"
    textColor: "{colors.wall}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.button}"
    padding: "0 24px"
    height: "56px"
  button-line-hover:
    textColor: "{colors.chalk}"
  input:
    backgroundColor: "{colors.wall}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.wall}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "0 16px"
    height: "48px"
  chip-checked:
    backgroundColor: "{colors.trim}"
    textColor: "{colors.wall}"
  service-row:
    textColor: "{colors.ink}"
    typography: "{typography.title}"
    padding: "12px 2px"
    height: "72px"
  row-arrow:
    backgroundColor: "{colors.wall-3}"
    textColor: "{colors.ink}"
    rounded: "{rounded.round}"
    size: "46px"
  row-arrow-hover:
    backgroundColor: "{colors.chalk}"
    textColor: "{colors.wall}"
  swatch:
    rounded: "{rounded.swatch}"
    size: "44px"
  quote-panel:
    backgroundColor: "{colors.wall-2}"
    rounded: "{rounded.panel}"
    padding: "26px 18px"
---

# Design System: Above All Flooring

Everything lives in `index.html`: tokens on `:root`, one `<style>` block, and plain-JS IIFEs at the bottom. Motion constants, shadows and component snippets that the frontmatter can't hold are in `.impeccable/design.json`.

## Overview

**Creative North Star: "The Finished Basement"**

The page is the room from their own job photo: a navy wall, a white baseboard, and fresh greige carpet with vacuum lines in it. The wall is the ground on every screen. Trim-white carries type and the primary button. The carpet appears as the hero floor, the photo and the step numerals. The installer's kit supplies the rest: a showroom swatch ring, the blue chalk line snapped to mark a straight edge, and their stencil logo recolored as a mask.

The page is dense but calm: one column on a phone, heavy uppercase headings, and generous rows and fields sized for a thumb in Facebook's in-app browser. Blue appears only when the visitor does something (hover, focus, form outlines, the chalk powder). The two effects are both real materials you can touch: you brush the carpet pile, and the chalk string twangs when you cross it.

**Key Characteristics:**
- Navy-wall ground, never black; trim-white is the light, not pure white.
- One accent (chalk blue), shown only on interaction and in the chalk-line powder.
- System sans at weight 900, uppercase, tight leading for headings; 17px body.
- Real-material motion only: carpet nap and a chalk-line string, sharing one rAF loop.
- Thumb-sized controls: 44px minimum hit area, 56px buttons, 72px service rows.

## Colors

A dark, cool, tonal palette taken from the photo, with a warm greige and a warm white for material and one cool blue for interaction.

### Primary
- **Chalk-Line Blue** (`chalk`): the only accent. Hover and focus on everything; outlines on form controls; the filled arrow on a hovered service row; the powder left by a snapped chalk line; text selection; caret color. Never a resting fill.

### Secondary
- **Fresh Greige Carpet** (`carpet`): the carpet in their photo. It is the hero canvas's default swatch (`rgb(196,182,166)`) and the color of the step numerals. Use it as a material, not as a UI accent.

### Neutral
- **Basement Navy Wall** (`wall`): page ground, the `theme-color`, input and chip fills, and the text on filled buttons.
- **Raised Wall** (`wall-2`): raised surfaces (the quote panel, the photo frame's fill).
- **Wall Rule** (`wall-3`): hairline rules between rows and in the footer, the resting arrow circle, the "sent" box border.
- **Control Edge** (`line`): the 2px border on inputs and chips (3:1 on the panel).
- **Baseboard Trim** (`trim`): primary button fill, button-line borders, the checked chip, the logo, and the top stop of the baseboard gradient.
- **Trim Shadow** (`trim-shade`): the bottom stop of the baseboard gradient (`linear-gradient(trim, trim-shade)`).
- **Warm Ink** (`ink`): main text.
- **Soft Ink** (`ink-soft`): secondary text (the promise, step copy, "(optional)", notes, footer).
- **Faint Ink** (`ink-faint`): placeholders only.
- **Error Peach** (`err`): error text and the border of invalid fields. It is a state color, not part of the palette.

### Named Rules
**The Accent-On-Touch Rule.** Chalk blue appears only on hover, focus, form outlines and chalk powder. Nothing is blue at rest; an arrow or button that is blue by default is a bug.

**The Wall-Not-Black Rule.** Dark surfaces step through `wall`, `wall-2` and `wall-3`. Don't add black or neutral grays; shadows are tinted navy (`rgba(6,10,24,…)`) or warm brown over carpet (`rgba(20,16,10,…)`).

## Typography

**Display Font:** system stack (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`)
**Body Font:** the same stack

**Character:** one family carried by weight. 900 uppercase with tight leading for headings, 800 for labels and controls, 400 for reading. The heaviness echoes the stencil logo. The system stack is Ellie's pitch-site house style (`ellie-taste.md` §2).

### Hierarchy
- **Display** (900, `clamp(2.7rem, min(12.4vw, 15svh), 6rem)`, 0.98, -0.02em, uppercase): the hero h1 only. The `svh` term keeps it from crowding short phone screens.
- **Headline** (900, `clamp(2rem, 8.5vw, 3.6rem)`, 0.98, -0.01em, uppercase, `text-wrap: balance`): section h2s.
- **Title** (800, `clamp(20px, 5.6vw, 28px)`, uppercase): service rows. Step h3s use 900 at `clamp(20px, 5.4vw, 26px)`.
- **Numeral** (900, `clamp(34px, 9vw, 44px)`, in `carpet`): CSS-counter step numbers.
- **Lede** (400, `clamp(17px, 4.6vw, 20px)`, `ink-soft`, max 34ch on phones): the hero promise.
- **Body** (400, 17px/1.55): all reading text. Step copy is capped at 46ch.
- **Label** (800, 17px): buttons, form labels and legends, the header phone number, the carpet hint.
- **Small** (700–900, 13.5px): the wordmark beside the logo mark (900, 0.08em, uppercase), the swatch label, the line under the send button.

The text steps are 13.5 / 17 / 20px. Don't add sizes in between; 17px is the floor for anything a visitor has to read or tap.

### Named Rules
**The Three Steps Rule.** Fixed text uses 13.5px, 17px or the 17–20px lede, and only headings use clamps. 13.5px is for short labels and the one-line note under the send button, never for body copy.

## Layout

The page is one column on phones with `--pad` side gutters (`clamp(16px, 5vw, 48px)`), and `.wrap` caps content at 1180px. The hero fills `min(100svh, 980px)` as a flex column: header, copy, swatch ring, then the carpet floor takes the rest (`flex: 1`, at least 230px).

- Sections have 56px vertical padding (80px at 1024px and up). Section heads sit 28px above their content. Stacks use 24px, button gaps 12px, chips and swatches 8px.
- **700px and up:** hero buttons sit side by side (at least 230px each), the photo stops bleeding to the edges (max 560px, rounded and lifted), and the quote panel gets 40px of padding.
- **1024px and up:** two-column grids with a 64px gutter. Services and proof use 5fr/6fr; the quote section uses 4fr/6fr. Proof and quote heads are `position: sticky; top: 32px`. Steps become three columns. The swatch ring moves right, overlapping the hero copy row (`margin-top: -56px`). The closing logo block moves into the quote column (`.side-close`) and the standalone `.close` is hidden.
- Sections are separated by chalk-line dividers (56px tall), not by background changes.
- Hover styles are inside `@media (hover:hover)`, so touch devices never get stuck hover states.

## Elevation & Depth

The page is mostly flat and tonal (`wall` → `wall-2`), with lift where a real object would cast a shadow: the baseboard on the carpet, the swatches, the quote panel, and the framed photo.

### Shadow Vocabulary
- **Lift** (`--shadow-lift: 0 18px 40px rgba(6,10,24,.45)`): the quote panel, and the photo frame at 700px and up.
- **Baseboard** (`0 2px 2px rgba(20,16,10,.35), 0 6px 12px rgba(20,16,10,.22)`): the trim strip casting onto the carpet. On the photo's bottom band it is reversed (`0 -3px 8px rgba(20,16,10,.25)`).
- **Swatch** (`0 3px 8px rgba(8,12,20,.45)`): a sample sitting on the wall. When selected it rises 5px and gets a double ring (`0 0 0 3px wall, 0 0 0 5px trim`).

### Named Rules
**The Real-Shadow Rule.** A shadow means an object casts it: trim, a swatch, a panel, a framed photo. Rows, chips and text get no shadows.

## Shapes

Corners are soft and step up with the size of the object: 9px swatches, 10px fields, chips and the sent box, 12px buttons, 14px (`--radius`) panels and the framed photo. Arrows are full circles (46px). Borders are 2px on interactive edges (buttons, inputs, chips) and 1px `wall-3` hairlines for rules. The baseboard is a straight 14–16px trim-gradient band. It sits along the top of the carpet in the hero and along the bottom of the work photo, tying the photo to the page.

## Components

### Header
- Logo mark on the left (54×21px, 66×26px at 700px and up), drawn as a CSS mask over `currentColor` so it takes the ink color. Beside it is the two-line wordmark (Small, 900 uppercase), which becomes one line at 700px and up. The whole brand link is at least 44px tall.
- The phone number is in the top right: a `tel:` link in Label weight, 17px. On hover it turns chalk with a 2px chalk underline (a transparent border at rest). This is the only phone number on the first screen.

### Buttons
- **Shape:** gently rounded (12px), at least 56px tall, 24px side padding, 2px trim border, Label type, optional 20px SVG icon with a 10px gap.
- **Fill (primary):** trim background, wall text. On hover the background and border turn chalk.
- **Line (secondary):** transparent with ink text and a trim border. On hover the border and text turn chalk.
- **Active:** `translateY(1px)`. Focus: the global 3px chalk outline, offset 3px.
- **Pairing:** the hero has exactly one Fill ("Get a quote") and one Line ("Text a photo of the room"). The Facebook link under the photo is a full-width Line button (60px tall, 24px icon). The form submit is a full-width Fill; its focus state fills it chalk.

### Swatch ring
- A row of 44px rounded squares on the wall just above the baseboard, with a "Color" label in Small. Each swatch is its color plus a tiled fiber texture (`--fiber`, a 64px canvas tile generated at load).
- `aria-pressed` toggles. When selected the swatch rises 5px and gets a wall/trim double ring. On hover it rises 3px. Choosing a swatch eases the carpet to that color and pre-fills the form's color field ("Something like Slate") until the visitor types there.
- The colors are in `SWATCHES` in the script: Greige, Oatmeal, Slate, Moss, Cocoa.

### Service rows
- A full-width list of links, at least 72px tall, in Title type, separated by `wall-3` hairlines. Each row opens a pre-filled text for that room (`ROOMS` in the script).
- **Only the arrow changes.** The 46px arrow circle rests at `wall-3`. On hover it fills chalk with wall text and shifts 3px right. On keyboard focus it does the same and gets a 3px chalk outline. The row itself never gets an outline, background or shadow.

### Inputs / Fields
- **Style:** wall fill, 2px `line` border, 10px radius, 14px padding, at least 52px tall (the textarea is at least 96px and resizes vertically), 17px/500 text, chalk caret. Labels are Label weight, and "(optional)" is 500 in `ink-soft`.
- **Hover:** the border turns chalk. **Focus:** chalk border plus a `0 0 0 3px rgba(127,182,255,.25)` halo.
- **Error:** the border and message use `err`, the message is 17px/700 below the field, and `aria-invalid` is set. The first bad field gets focus.

### Chips (form only)
- Radio chips for "Which room?": wall fill, 2px `line` border, 10px radius, at least 48px tall, weight 700.
- **Hover and keyboard focus:** chalk border. **Checked:** trim fill with wall text and a trim border; when it also has focus or hover, the border is chalk.
- These are the only chip-shaped things on the page because they are the only ones you can tap.

### Quote panel
- `wall-2` panel, 14px radius, Lift shadow, 26/18px padding (40px at 700px and up, 44px at 1024px and up). Submitting shows a "sent" box (wall fill, `wall-3` border) with the message in a `pre`, a Line "Copy the message" button (with fallbacks for in-app browsers), and a call link for when the text app doesn't open.

### Proof photo
- The work photo in a `wall-2` frame. It bleeds to the screen edges on phones (negative `--pad` margins) and becomes a rounded, lifted frame at 700px and up (max 560px). A 14px trim baseboard band is pinned to its bottom edge. There is no caption. The Facebook Line button sits directly under it.

### Chalk-line divider
- An inline SVG between sections, 56px tall and full width. It has two paths: the **powder**, a straight 5px chalk-blue stroke roughened by the `#chalky` turbulence filter, which fades in to 0.9; and the **string**, a 1.6px trim polyline that fades from 0.85 to 0.35 after snapping. Both are inset `min(24px, 4% of width)` from each end.

### Carpet hero (signature)
- Two stacked canvases under the baseboard. **Pile** is a low-res nap field (one cell per `CELL` px, blurred 1.4px), shaded by each cell's brush direction against a fixed light. **Fiber** is a tuft tile drawn once at device pixel ratio, overlay-blended. A shade layer darkens near the baseboard and toward the corners. The hint ("Drag across the carpet") is wall-colored with a trim glow, switches to white with a dark glow on dark swatches, and fades out after the first brush.
- `touch-action: none`, and the canvas rect is read every frame, so drags in any direction brush instead of scrolling. `overscroll-behavior-y: none` on `html` stops pull-to-refresh.

### Motion: shared loop and tunables
Both effects subscribe to one `Loop` (requestAnimationFrame that stops itself when no subscriber is active, with dt capped at 50ms) and read one shared `Pointer` (client coordinates; touch and mouse both feed it; the previous position is recorded last each frame). Off-screen elements are paused by IntersectionObserver.

**Carpet** (constants at the top of the "Carpet: brushable pile" IIFE):
| Constant | Value | Effect |
|---|---|---|
| `CELL` | 4 (phone) / 5 | px per nap cell; lower means finer and slower |
| `SHADE` | 0.16 | how much brushing direction lightens or darkens |
| `RELAX` | 0.055 /s | how fast brush marks settle back to the resting grain |
| `BRUSH_R` | 30 / 38 px | finger or mouse brush radius |
| `LANE` | 54 / 70 px | vacuum stripe width (lanes overlap at 0.82) |
| `VAC_SPEED` | 300 / 420 px/s | auto-vacuum speed |
| `IDLE` | 3.5 s | wait after the last touch before the vacuum resumes |
| `LIGHT` | [0.22, -0.975] | light direction for nap shading |

Brush strength is 0.55 for touch or a pressed mouse and 0.32 for hover. The vacuum brushes at 0.42 with a sine wobble. The floor starts already striped like their photo. Color eases toward the chosen swatch at a rate of `dt*6`. A resize keeps the brushing if the size didn't change (for example when the phone's address bar shows or hides).

**Chalk line** (constants at the top of the "Chalk-line dividers" IIFE):
| Constant | Value | Effect |
|---|---|---|
| `N` | 64 | points along each string |
| `SPEED` | 480 | wave speed (sets the twang's pitch) |
| `DAMP` | 2.6 /s | how fast it stops ringing |
| `PLUCK` | 220 px/s | how hard a crossing pointer plucks it |
| `SNAP` | -22 px | lift before release on first view |

Each line snaps once, the first time more than 90% of it is visible: it is lifted into an arc, released, and the powder appears 200ms later. After that, any pointer crossing the line plucks it with a Gaussian of 5 points, scaled by vertical speed. It is a wave equation with 14 substeps per frame and goes to sleep below an energy of 0.002.

**Reduced motion** (`prefers-reduced-motion: reduce`): no auto-vacuum, but the visitor's own brushing still works (the loop runs only for 400ms after pointer movement). Swatch color changes instantly. Chalk lines render already snapped and are never plucked. Swatches, arrows and buttons lose their transforms (color transitions stay), and smooth scrolling is off.

**Easing:** `--ease: cubic-bezier(.16,1,.3,1)` for swatch lifts, arrow shifts and chalk fades. UI color transitions take 0.2s.

## Do's and Don'ts

### Do:
- **Do** keep chalk blue for hover, focus, form outlines and chalk powder only (The Accent-On-Touch Rule).
- **Do** give every form control (inputs, textarea, chips, form buttons) a chalk outline or border on both hover and focus.
- **Do** keep the phone number in the header's top-right as a `tel:` link, once on the first screen. The footer and the post-send note can repeat it.
- **Do** keep the hero to one short display headline, the promise, and one Fill plus one Line button.
- **Do** put the Facebook Line button directly under the work photos, and in the footer.
- **Do** keep tap targets at least 44px, buttons at least 56px, and rows at least 72px.
- **Do** tune motion through the named constants above, not by rewriting the loops.
- **Do** keep hover styles inside `@media (hover:hover)`.

### Don't:
- **Don't** outline, tint or shadow a service row on hover or focus; only its arrow changes.
- **Don't** make non-interactive labels look like chips or buttons. Towns, tags and service lists are plain text; chips exist only as form radios.
- **Don't** put a Call button under the hero title, a sticky bottom contact bar, or any email link outside the footer.
- **Don't** let canvas texture, chalk lines or the baseboard run behind text. The hint keeps its glow, and the copy stays above the floor.
- **Don't** add captions under photos or a lede sentence above them.
- **Don't** add effects that don't read as a real flooring material or tool (no sheens, films or glints over the photo).
- **Don't** introduce a second accent color or pure black/white surfaces.
