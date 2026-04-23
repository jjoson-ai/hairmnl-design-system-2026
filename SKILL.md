# HairMNL Design System — skill

Use this skill when designing anything for **HairMNL** (hairmnl.com, the Backbar B2B channel, or the HairMNL Studio salon sub-brand): landing pages, product pages, editorial content, blog posts, social templates, email newsletters, in-store signage, print collateral, and internal pitch decks.

## Start here

1. Read `README.md` **in full** before drawing anything. It has the brand context (who HairMNL is, what Serious Studio's 2020 rebrand established), the three brand pillars, tone/voice rules, and visual foundations.
2. Link or copy `colors_and_type.css` and `fonts/fonts.css` into your output file — they define the tokens and load the custom OTFs (Self Modern, Basis Grotesque Pro, Basis Grotesque Mono) from this directory.
3. Browse `preview/` cards for a fast visual index of the system (colors, type scale, buttons, pillars, seals, patterns).
4. For full website recreations, reference `ui_kits/web/Website UI Kit.html` — it shows the home, category, and product-detail screens using the system end-to-end.

## Token quick reference

Use CSS variables from `colors_and_type.css`. Never hard-code hex values in designs — use the token.

- Page grounds: `--hm-paper` (#FAF6F2) or `--hm-paper-warm` (#F3EBE6). Never pure white.
- Ink on paper: `--hm-ink` (#1A1A1A) — headlines · `--hm-ink-soft` (#3C3A38) — body · `--hm-ink-muted` (#6F6B66) — meta · `--hm-ink-subtle` (#9A958F) — disabled.
- Primary / secondary / tertiary palettes: `--hm-blush`, `--hm-stone`, `--hm-sage`, `--hm-lilac`, `--hm-sand`, `--hm-sky`, `--hm-peach`, `--hm-honey`, `--hm-terracotta`, `--hm-espresso`, `--hm-lavender`, `--hm-teal`, etc.
- Type: `--font-display` (Self Modern) · `--font-sans` (Basis Grotesque Pro) · `--font-mono` (Basis Grotesque Mono).
- Spacing is 8-pt based: `--space-1` through `--space-24` (= 4px through 96px).
- Radii: default 0. Inputs may use `--radius-sm` (2px). Seals/avatars use `--radius-full`.
- Shadows: `--shadow-1` (barely-there) · `--shadow-2` (card) · `--shadow-3` (modal). Use `none` by default; prefer 1px hairline borders (`--color-hairline`).
- Motion: 220ms standard, easing `cubic-bezier(0.22, 0.61, 0.36, 1)`.

## Copywriting checklist

Every piece of copy you write should pass this checklist before you hand it over.

- [ ] Addresses the reader as **"you / your hair"**. Never "customers" or "users".
- [ ] Picks **one dominant pillar** (The Real Deal / No Stress Tresses / At the Root) and optionally layers a second. Never mixes all three at once.
- [ ] Body is **sentence case**. ALL-CAPS is reserved for nav, buttons, eyebrows, badges, pillar indices.
- [ ] Prices are `P 1,800` (capital P + space), not `₱` or `PHP`.
- [ ] Hours in mono with en-dashes: `MON–SAT 1000–1900`.
- [ ] **No exclamation marks.** No emoji outside pillar-02 (customer support, casual social replies).
- [ ] Headlines use Self Modern with optional italic on the emphasised noun ("We speak *curl*.").
- [ ] Technical content gets translated to plain language. No raw ingredient-study jargon.
- [ ] "We" = the HairMNL team. Never "I".

## Visual checklist

Before you call a composition done, walk this list top-to-bottom.

- [ ] Page ground is paper (`#FAF6F2`) or blush (`#F3EBE6`), not pure white.
- [ ] Text ink is `#1A1A1A` (or softer), not pure black.
- [ ] Every section has **an eyebrow** (mono caps, tracked wide) above its serif headline.
- [ ] Serif headlines use Self Modern with `letter-spacing: -0.02em` and tight line-height (0.95–1.05).
- [ ] Buttons are **square** (0 radius), 1px ink border, caps label at 11–12px with `0.18em` tracking.
- [ ] Cards use 1px hairlines, not drop shadows. Shadows only on elevated surfaces (modals, sticky nav on scroll).
- [ ] Dividers are 1px at 10–14% ink opacity.
- [ ] Category pages use a **secondary-palette ground** (Sage / Lilac / Sand / Sky) for the hero band.
- [ ] Photography is warm, airy, desaturated, mid-gesture — never clinical or overlit. If you don't have real photography, use a solid pastel tint block with a mono caption like `[ PHOTOGRAPHY — EDITORIAL HAIR ]` rather than stock.
- [ ] Patterns: the hair-strand line motif (`assets/patterns/hair_strands.png`) whispers at 15–25% opacity over a paper ground. Never at 100%.
- [ ] Iconography: the custom HairMNL sets in `assets/icons/` (solutions, ecom, product, hair_type) come first. Any missing UI icon is a thin-stroke Phosphor icon (regular weight) — flag it as a substitution.
- [ ] Spacing is generous. 120–160px side margins on desktop. 80px between sections. Deny density.

## When to ask

- If the user wants a **new palette extension** (a sub-brand, a seasonal campaign colour): ask before inventing. Tertiary warms/cools have room — but every new colour must be dusty and low-chroma.
- If the user wants a **different type pairing**: push back. Self Modern + Basis Grotesque Pro is the identity. Alternatives live in `fonts/` only as fallbacks.
- If the user wants **stock photography**: ask for real HairMNL photography or reach for solid tint blocks + captions. Don't insert generic beauty stock.
- If copy feels like it wants an exclamation mark: rewrite so it doesn't need one.

## Files in this system

- `README.md` — full brand context, fundamentals, foundations, iconography
- `SKILL.md` — this file
- `colors_and_type.css` — tokens + base styles (import this into everything)
- `fonts/` — Self Modern, Basis Grotesque Pro (400/500/700/900), Basis Grotesque Mono + `fonts.css`
- `assets/logo/` — horizontal, vertical, seal, HairMNL Studio lockups
- `assets/patterns/hair_strands.png` — signature line motif
- `assets/illustrations/` — hair-type line illustrations
- `assets/icons/{hair_type, ecom, solutions, product}/` — custom icon/seal sets
- `preview/` — design-system cards shown in the Design System tab
- `ui_kits/web/Website UI Kit.html` — reference screens (home, category, product)
