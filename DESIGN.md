# Design system — Changing Places Realty

Two designs live in this repo. `index.html` is the **light** design, the main
demo since 2026-10-09. `dark.html` preserves the original card-derived dark
design (linked from the light footer). The light design is deliberately NOT
modeled on the business card: sunlit coastal paper, deep palm green as the
committed color, terracotta as the rare second voice.

## Light design (index.html)

### Color (OKLCH, Committed strategy: palm green carries identity on a warm paper field)

- `--paper`:     oklch(0.97 0.012 95)   — page field (warm paper, never #fff)
- `--paper-2`:   oklch(0.945 0.016 95)  — raised/alternate bands
- `--ink`:       oklch(0.30 0.035 190)  — primary text (deep sea-tinted, never #000)
- `--soft`:      oklch(0.47 0.03 190)   — secondary text
- `--line`:      oklch(0.88 0.015 120)  — borders, hairlines
- `--palm`:      oklch(0.46 0.085 175)  — brand green: links, labels, primary buttons
- `--palm-deep`: oklch(0.37 0.075 180)  — hover, footer, alerts-band overlay base
- `--palm-wash`: oklch(0.93 0.03 175)   — tinted fills (ghost hover, quota badge)
- `--clay`:      oklch(0.60 0.125 45)   — terracotta accent: price-reduced, "save" tags
- `--clay-wash`: oklch(0.94 0.03 55)    — clay tint fill (reduced badge)

### Typography

- Display: **Prata** (single 400 weight). Headings, wordmark, prices.
- Body: **Hanken Grotesk** (400/500/600 + italic). Labels are 600, uppercase,
  +0.2em tracking, palm.
- Base scale 115% (`html { font-size: 115% }`) — readability request from Rob,
  keep it. Body 1.02rem/1.7.

### Layout & components

- Sticky paper top bar: wordmark + nav + WhatsApp pill always in reach.
- Split hero (copy left, photo right), trust line under the CTAs.
- Residences: one wide feature card + auto-fit grid `minmax(300px, 1fr)`
  (300px floor keeps 5 cards as 3+2, no orphan row).
- Lead-feature badges (the Gecko fold-ins): `.badge.quota` "Foreign quota" on
  condos, `.badge.reduced` + `.was` strikethrough + `.now-tag` on reductions.
- Alerts band: photo behind `oklch(0.33 0.07 185 / 0.82)` overlay, email
  capture (demo form — no backend yet).
- Buttons: pill radius, palm fill primary / palm-border ghost.
- Motion: entrance reveals only (`.reveal`), 250ms+ ease
  `cubic-bezier(0.22,1,0.36,1)`, IntersectionObserver.

## Dark design (dark.html)

Derived from the printed business card (midnight navy field, bronze antique
clock, dusk villa) and the quiet-luxury lane.

- `--night`: oklch(0.16 0.03 255) field; raised `0.20`, hairlines `0.26`.
- `--ivory`: oklch(0.92 0.055 88) champagne text (post-readability fix — not
  white), `--mist` oklch(0.83 0.04 86) secondary.
- `--bronze`: oklch(0.70 0.085 70) accent; `--bronze-deep` oklch(0.58 0.095 60).
- Display: **Marcellus**; body + italic motto: **EB Garamond**.
- Hero carries a two-layer scrim including a left-to-right gradient so the
  headline holds against bright skies; `.tile .veil` has a text-shadow for the
  same reason. Last two grid tiles are `.wide` to avoid a half-empty row.
- Base scale is also 115%.

## Shared rules

- Full-bleed licensed Pexels imagery (IDs in README); alt text in brand voice.
  Real listing photos replace these only with owner/agent permission.
- Long-scroll single page: hero → residences → (alerts) → story → areas →
  contact. Content left-aligned, not centered.
- WhatsApp buttons carry the language tag (English line / Thai line —
  สายภาษาไทย on the light design).
- Respect reduced-motion; no scroll-jacking.
