# Design system — Changing Places Realty

Derived from the printed business card (midnight navy field, bronze antique clock,
dusk villa, white roman caps, italic serif motto) and the quiet-luxury lane.

## Color (OKLCH, Committed strategy: navy carries the surface, bronze is the voice)

- `--night`:  oklch(0.16 0.03 255)  — page field (card navy, near-black)
- `--night-2`: oklch(0.20 0.035 255) — raised panels
- `--night-3`: oklch(0.26 0.04 255) — borders, hairlines
- `--ivory`:  oklch(0.94 0.012 85)  — primary text (warm, never #fff)
- `--mist`:   oklch(0.72 0.02 250)  — secondary text
- `--bronze`: oklch(0.70 0.085 70)  — accent, links, labels (clock-rim copper)
- `--bronze-deep`: oklch(0.58 0.095 60) — hover, buttons
- `--pool`:   oklch(0.72 0.07 200)  — rare second accent (pool teal), tags only

The palette is taken from the client's physical card, not from the
"finance = navy + gold" reflex; the card is the brief.

## Typography

- Display: **Marcellus** (single 400 weight, engraved-roman feel, matches the
  clock/monogram mood). All headings, prices, nav wordmark.
- Body + italic voice: **EB Garamond** (400/500 + italic). The motto "Time for a
  Change" is always EB Garamond italic.
- Labels: EB Garamond 500, uppercase, +0.18em tracking, bronze.
- Scale: fluid clamp(), ratio ≥1.3. Body 1.0625rem/1.75, max 68ch.

## Layout

- Long-scroll single page: hero → statement → residences → story → areas → contact.
- Asymmetric residences grid: one featured tile spanning 2×2, the rest varied;
  never six identical cards.
- Full-bleed imagery with gradient scrims; content left-aligned, not centered.

## Imagery

Licensed Pexels photography, dusk-biased. Alt text written in brand voice.
Real listing photos replace these when Peter supplies inventory.

## Motion

Entrance reveals only: opacity + 12px translate, 700ms cubic-bezier(0.22,1,0.36,1),
staggered. IntersectionObserver, no scroll-jacking, respects reduced-motion.

## Components

- Primary CTA: bronze fill, night text, Marcellus, generous padding.
- Ghost CTA: 1px bronze border, ivory text.
- WhatsApp buttons carry the language tag (English line / Thai line).
- Listing tile: image, bronze area label, Marcellus title + price, mist meta row.
