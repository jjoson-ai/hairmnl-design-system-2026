# HairMNL Design System

**HairMNL** is a Metro-Manila-based professional hair-care retailer and salon brand ("**HairMNL Studio**"). They curate professional hair-care products from international pro-brands (L'Oréal Professionnel, Kérastase, Davines, Redken, Olaplex, K18, Schwarzkopf, Biolage, TIGI Bed Head, Dyson, BaByliss PRO, etc.), plus a "Backbar" B2B wholesale arm and a brick-and-mortar studio at Brixton St., Pasig, Metro Manila.

Brand essence: **Your Mane Authority** — a trusted, expert friend for real-life hair concerns.

This design system captures the **2020 rebrand by Serious Studio** — a quiet, editorial, neutral-luxury identity — **extended for 2026 multi-channel e-commerce.** The original paper, type, and voice system is unchanged; this revision adds the surfaces the 2020 guide didn't cover: mobile app, responsive web, social, YouTube, email, ads, motion, and accessibility.

## Sources

- **Local codebase** (Shopify theme, Pipeline v6.1.3 by Groupthought):
  `HairMNL 2020 Rebrand/` — mounted via the File System Access API
- **Brand guide PDFs**: Brand Guide (Apr 2020), Tone & Language Guide v2.0 (Mar 2020), Photography Guidelines v2 (Mar 2020) — by Serious Studio
- **Brand Collaterals** (Website top-folds, Service Menu, Blog Page, Newsletter, Relaunch Ads, Social Media Templates)
- **Brand Identity** (Color Palette AI/PNG, Icons, Illustrations, Logo set, Patterns, Typesetting)
- **Theme repo**: `jjoson-ai/hairmnl-theme` (GitHub; Shopify "Pipeline" theme v6.1.3 with HairMNL custom font uploads + settings)

All raw assets are preserved in the source mount; curated copies live under `assets/` and `fonts/`.

---

## Index

- `README.md` — this document (brand context, fundamentals, foundations, iconography)
- `SKILL.md` — agent-skill entrypoint, cross-compatible with Claude Code
- `colors_and_type.css` — CSS variables for colors, type, spacing, motion + base element styles
- `fonts/` — brand OTFs (Self Modern, Self Modern Italic, Basis Grotesque Pro Regular/Medium/Bold/Black, Basis Grotesque Mono) and `fonts.css`
- `assets/`
  - `logo/` — horizontal, vertical, seal, HairMNL Studio variants (black/white/inverse)
  - `patterns/` — hair-strands line motif + coloured graphic ribbons
  - `illustrations/` — hair-type line illustrations (wavy, curly, short, straight, men's styling)
  - `icons/hair_type/`, `icons/ecom/`, `icons/solutions/`, `icons/product/`
- `preview/` — self-contained design-system cards shown in the Design System tab
- `motion.css` — motion primitives (durations, easings, scroll-reveal, toast-in, modal-in, skeleton shimmer) with `prefers-reduced-motion` respected
- `responsive_and_a11y.css` — breakpoint tokens (sm/md/lg/xl), fluid type clamp, focus-visible ring, 44 px tap-target guardrails
- `accessibility_spec.md` — WCAG 2.2 AA contrast matrix, focus, targets, ARIA, forms, motion, testing checklist
- `photography_and_video_2026.md` — 9:16-first shoot rules, UGC &amp; creator brief floor, LUT, what we won't shoot
- `ui_kits/web/` — UI kit recreating core HairMNL.com screens (home, category, product, blog, cart)
- `ui_kits/web/Responsive Web UI Kit.html` — mobile 390 + tablet 820 addendum
- `ui_kits/social/Social Media UI Kit.html` — IG post, carousel, stories/reels, Pinterest, TikTok, avatars
- `ui_kits/youtube/YouTube UI Kit.html` — channel banner, five thumbnail shows, lower-thirds, end-card
- `ui_kits/email/Email UI Kit.html` — welcome, order confirmation, newsletter, abandoned cart
- `ui_kits/ads/Ads UI Kit.html` — display (leaderboard, med-rect, skyscraper), Meta (square + story), Google search
- `assets/icons/sprite.svg` — 2026 thin-stroke UI icon fallback set (search, bag, heart, user, menu, play, share, filter, chevrons, etc.)
- **HairMNL iOS App** — companion project, used as the app-product reference for this system (studio booking, shop, journal, bag + checkout)

---

## Content Fundamentals

HairMNL's voice comes from two people in one: **a knowledgeable friend** and **a real-life expert**. The brand has three named "pillars" that you can dial up or down depending on the touchpoint — they are *not* mutually exclusive.

### The three pillars

| # | Pillar | Goal tone | Vocabulary | Best for |
|---|---|---|---|---|
| 01 | **The Real Deal** | Knowledgeable · Instructive · Relatable · Accessible | Expert, professional, authority, study, diagnose, formula, prescription, treatment | Brand introductions, explainers, technical tutorials, ingredient lists |
| 02 | **No Stress Tresses** | Light · Easy · Simple · Colloquial | Mane, tresses, locks, everyday words | Trend lists, hairstyle tutorials, customer support, transactional emails |
| 03 | **At the Root** | Warm · Friendly · Understanding · Compassionate | "We understand you", "We get it", "We speak curl", "It's yours to define" | Brand intros, issue-specific content, curated collections |

### Casing, person, mood

- **Second person** ("**you**, **your**" hair) is constant. First person is **"we"** (the brand, the HairMNL team), never "I".
- **Sentence case** for body and headings. Exceptions: nav labels, button text, eyebrow labels, pillar names, section indices — these are **ALL CAPS** with wide letter-spacing (e.g. `BY HAIR ISSUE`, `SHOP NOW`, `01 THE REAL DEAL`).
- **Italic emphasis inside a roman serif line** is a signature treatment: *Your* **Mane** *Authority* — the noun the reader cares about gets the italic.
- **No exclamation marks**, no ALL-CAPS SHOUTING. The brand is warm but composed.
- **Hair terms as mood switchers**: "hair" in technical contexts; "mane/tresses/locks/curls" in casual/editorial contexts. "We speak curl." is the emblematic line.
- **Emoji**: only under pillar 02 (No Stress Tresses) — customer support, social replies, transactional/reply emails. Never in editorial, product, or brand-intro copy. Use them like a human would, not as decoration.
- **Unit style**: peso prices as `P 1,800` (capital P with thin space, not `₱`). Phone numbers as `(+63) 908 897 7364`. Hours as `MON–THU 0930–1900` (mono, en-dashes).
- **Dates**: "Sept. 22-30, 2020" style.

### Examples from the real collateral

- Brand intro: *"We go great lengths to curate and personalize professional hair care products from all over the world just for you, not just to take care of your hair, but to celebrate who you are. At HairMNL, let your hair down for expert mane care that goes down to the root."*
- Pillar 02 headline: *"New Decade, New Hair: Trends to Ring in 2020"* — light, time-sensitive, playful.
- Pillar 03 curation headline: *"We Speak Curl. Here, every curl gets a voice — and the power to define itself."*
- Sale-promo headline (pillar 03 + 01 together): *"Celebrating 3 Years of Professional Hair Care with a Treat for You."*

### Writing do / don't

- **Don't** dump research statistics ("participants ingesting keratin 500mg in a double-blind trial…") as-is. **Do** translate: "Genetics are the most common cause of hair loss. But don't blame Mom."
- **Don't** impose one standard of beauty. **Do** affirm uniqueness: "As unique as you and your hair."
- **Don't** lead a concern-piece with sales copy. **Do** name the feeling first, the product second.

---

## Visual Foundations

### Colors

Palette order of use: **primary → secondary → tertiary → ink → accent**.

**Primary** — brand grounds, hero backgrounds, newsletter bodies.
- `#F3EBE6` Blush — the signature warm cream page ground.
- `#E0E1E0` Stone — the cooler neutral companion.

**Secondary** — categorised backgrounds (by Hair Issue / Type / Brand sub-pages), social tiles.
- `#CAD1D3` Sage · `#E5DEE7` Lilac · `#E7D8C3` Sand · `#D6DEEE` Sky

**Tertiary** — accent moments, illustration accents, duotone photography.
- Shells/Ashes: `#EFE6E3` · `#E4E5E6`
- Warms: `#F0E6D0` Cream · `#EAC4A1` Peach · `#CFAF8B` Honey · `#AC604F` Terracotta · `#665A44` Espresso
- Cools: `#E7DAEB` Mauve · `#B4B5D2` Lavender · `#CCD9F0` Powder · `#82B4BD` Teal

**Ink** is near-black `#1A1A1A`, never pure `#000`. The seal/logo print-black is the exception. Text ink softens to `#3C3A38`, meta/caption to `#6F6B66`.

**Vibe**: every palette is dusty, desaturated, low-chroma. The brand avoids saturated neon/primary hues. If you find yourself reaching for pure red, blue, or green, stop — use a tertiary accent instead. Warm > cool in a tie.

### Typography

- **Display serif**: *Self Modern* — a modern didone with high stroke contrast. Used for **all** headlines, editorial pull quotes, and expressive moments. Inline italic is common and signature ("Your *Mane* Authority").
- **UI sans**: *Basis Grotesque Pro* — Regular 400 body, Medium 500 for button labels and UI emphasis, Bold 700 reserved for tiny caps labels and pillar titles.
- **Mono**: *Basis Grotesque Mono* — hours, phone numbers, small technical meta (price codes, item numbers, coordinates).
- **Tracking**: display serif sits at `-0.02em` (slightly tight). All-caps grotesque labels go **wide** (`0.18em` / `tr-xwide`). Body is neutral.
- **Hierarchy move**: the brand often pairs a **big italic+roman serif headline** with a **tiny all-caps mono/sans eyebrow** directly above, and a small grotesque paragraph below. Three voices in one block; never four.
- **Capitalisation**: headlines sentence-case. Eyebrows, nav, buttons, pillar indices, badges — all caps.

### Layout

- **Generous paper**: a 1440px canvas typically uses a 120–160px side margin. Breathing room is the mood. Density is the enemy.
- **Hairline dividers** (1px @ ~14% opacity of ink) separate numbered blocks vertically. No box shadows on cards by default — hairlines instead.
- **Numbered sequences**: "01 / 02 / 03" with a thin rule between rows is a recurring pattern for pillars, service menus, and feature lists.
- **Two-voice grids**: the website's top-folds often juxtapose an **editorial left column** (big headline + paragraph + ghost button) with a **full-bleed photograph right column**. The split is roughly 40/60.
- **Aligned, not centered**: body copy is left-aligned. Headlines can be left or (rarely) centered for editorial covers. Buttons are left-aligned under the content they belong to.

### Backgrounds & surfaces

- **Page ground** is the cream blush `#F3EBE6` (or near-white `#FAF6F2`). Never pure white unless behind photography.
- **Hair-strand line motif** (`assets/patterns/hair_strands.png`) is a signature — vertical wavy lines behind empty right columns, cover pages, or as a low-opacity watermark. Use at low contrast (10–25% opacity on paper ground) — it whispers, never shouts.
- **Coloured graphic ribbons** in the secondary/tertiary palette (beige/blue/gray/green/purple/yellow) exist as full-bleed backdrops for categorised pages (by hair issue, by brand, etc.).
- **Full-bleed photography** is the second surface style: airy, editorial, pro-beauty. Real hands, real hair, real products — never stock composites. Photography Guidelines mandate natural light, low saturation, warm tones.

### Imagery vibe

- **Warm, airy, desaturated**. Models look relaxed, mid-gesture (spraying product, running hands through hair, mid-laugh), never glossy catalogue poses.
- Product shots are generous — product occupies ≤40% of the frame; the rest is negative space or tactile surface (stone, sand, paper).
- A subtle film-grain warmth is common; no heavy HDR, no clinical white backgrounds.
- Monochrome / B&W is reserved for editorial moments (blog inserts, spa-journey pieces).

### Motion

- **Subtle fades + 4–8px lifts** on hover (images only).
- **No bounces, no spring overshoot, no spinning icons.** The brand is composed.
- Easing: `cubic-bezier(0.22, 0.61, 0.36, 1)` (standard), 220ms for most interactions, 420ms for page-level transitions.
- Scroll-parallax on hero photos is fine (Pipeline theme supports it) but gentle.
- `prefers-reduced-motion` is respected; fades only.

### Interactive states

- **Hover** (link): opacity drops to 0.6; border-bottom rule remains 1px.
- **Hover** (image tile): 4–8px upward translate, optional second-image swap (the Shopify theme's `image_hover_enable` flag).
- **Hover** (button): border + text stay; background fills to ink OR softens to blush, with a 120ms ease. Never grow/shrink.
- **Press**: 1px inset shift, no squash.
- **Focus**: 2px offset outline in ink for accessibility; never removed.

### Borders, radii, shadows

- **Radii**: default 0 (buttons and cards are square). A subtle 2px is allowed on form inputs. Seals/avatars get `radius-full`. The theme setting defaults `button_radius` to 0.
- **Borders**: 1px solid ink (buttons, primary CTA) or 1px hairline at 10–14% opacity (cards, dividers, inputs).
- **Shadows**: none by default. Tier-1 (`--shadow-1`) is a barely-there lift (0 1px 2px + 0 2px 8px at 4% alpha). Tier-3 is reserved for modals/popovers only.
- **Protection gradients**: avoid. If text sits over photography, find a darker corner of the photo or use a solid tint block — not an over-photo gradient mask.
- **Transparency & blur**: used sparingly, on the announcement bar and sticky nav (backdrop-blur ~10px, paper at 85% alpha).

### Cards

A "HairMNL card" is: **cream or white surface, 0 radius (or 2px), 1px hairline border, no shadow, generous internal padding (24–32px), a small eyebrow + serif headline + body paragraph, sometimes a small product photo at top or left.**

### Layout rules

- **Announcement bar**: sticky at top, cream/blush ground, mono text at 11–13px, centered.
- **Main nav**: logo left, centered caps labels ("BY HAIR ISSUE · BY HAIR TYPE · BY BRAND · BY COLLECTION"), utility icons + "TOUSLED" (their loyalty/rewards) right.
- **Footer**: HairMNL seal + address block + social, on blush ground, with mono hours.

---

## Iconography

HairMNL ships a **custom, drawn icon set** created for the 2020 rebrand. It is **not** a CDN icon font — it's a finite PNG set living in `assets/icons/`. Stroke style is **thin, single-weight, editorial line-art** that visually rhymes with the "Self Modern" serif — not Material/Feather/Lucide chunkiness.

### Sets present

- **Hair Type** (`assets/icons/hair_type/`) — straight, wavy, curly, short, and two men's-styling variants. Thin line sketches of hair shapes.
- **E-Com Labels** (`assets/icons/ecom/`) — Award Winning, Best Seller, New, Special Offer. Round seals with scripted wordmark inside a thin ring. Used as product-tile corner ribbons.
- **HairMNL Solutions Seals** (`assets/icons/solutions/`) — Colored Hair, Damaged, Dandruff Control, Defined Curls, Frizz Control, Hairfall & Thinning, Remove Brassiness. Round seals used on curated-collection landing pages.
- **Product Labels** (`assets/icons/product/`) — Paraben Free, Sulfate-Free, Vegan. Round seals for ingredient claims.

### Illustrations

Larger decorative drawings (wavy/curly/short/straight heads, men's styling) live in `assets/illustrations/`. They appear on by-hair-type landings, the service menu cover, and print collateral.

### Emoji, unicode, third-party icons

- **Emoji**: allowed only in pillar-02 contexts (customer support, transactional replies, casual social). Never in product UI, product pages, or brand-introduction copy.
- **Unicode glyphs as icons**: used for quantity selectors (`−` / `+`), arrows (`←` `→`), checkmarks (`✓`). Don't stack emoji as a pseudo-bullet system.
- **Font Awesome 5 Brands**: present in the Shopify theme (`FontAwesome5Brands-Regular-400`) and used for the footer social row only (Facebook, Instagram, Pinterest, Tiktok, Vimeo). Never for UI actions.
- **Fallback set**: if a required icon is missing from the HairMNL set (e.g. cart, search, account), use a **thin-stroke 1.25px** icon from [Phosphor Icons](https://phosphoricons.com) "regular" weight, via the [@phosphor-icons/web](https://unpkg.com/@phosphor-icons/web) CDN. Phosphor's stroke weight best matches HairMNL's custom set. **Flag this substitution** in your output — a note like `/* substituted from Phosphor */`.

### Logo usage

- **Primary lockup**: `assets/logo/horizontal_black.png` — HAIR + a hair-swoosh on the H + MNL, horizontal.
- **Vertical**: `assets/logo/vertical_black.png` for square placements.
- **Seal**: `assets/logo/seal_black.png` / `seal_white.png` — "YOUR MANE AUTHORITY / HAIRMNL" around a stylised H. Used as a stamp in footers and print covers.
- **HairMNL Studio** (the salon sub-brand): separate lockup at `assets/logo/studio_horizontal_black.png`. Uses the same letterforms with "STUDIO" below.
- **Clearspace**: equal to the height of the "H" cap on all sides.
- **Minimum sizes**: horizontal lockup 120px wide on screen; seal 48px.

---


---

## 2026 Channel Map

The 2020 guide was built for one surface: the web. In 2026 HairMNL runs across eight. Every piece of copy or imagery gets a primary channel, and inherits the rules below.

### Channel × Voice-pillar cross-reference

| Channel | Dominant pillar | Also uses | Emoji? | Notes |
|---|---|---|---|---|
| Web home / PDP | 01 Real Deal + 03 At the Root | 02 for toasts &amp; confirmations | No | Editorial foundation. Serif italic sparingly. |
| Mobile app | 01 + 03 | 02 for tab labels, empty states | No | Tighter copy, larger tap targets, dark-ready. |
| Email — transactional | 02 No Stress Tresses | 01 for order details | Preheader only | Clear, kind, unfussy. |
| Email — newsletter (*The Brief*) | 03 + 01 | | Preheader only | Monthly, editorial, one feature + one routine. |
| Instagram feed | 03 | 01 for product drops | Captions only | One idea per post. Serif italic once per frame. |
| Instagram stories / reels | 02 + 03 | | Yes, in moderation | Polls, swipe-ups, behind-the-scenes, talent. |
| TikTok | 02 | 03 for emotional beats | Yes | Talk-y, fast, honest. Original audio preferred. |
| YouTube | 01 + 03 | 02 in GRWM | Titles only | Long-form tutorials, routines, reviews, collabs. |
| Pinterest | 01 | 03 for taglines | No | Evergreen routines and journal pins — text-forward. |
| Paid ads (display + Meta) | 03 for brand · 01 for product | | No | One idea per ad. Discount never larger than headline type. |
| Customer support (email/chat) | 02 | 03 when consoling | Yes | Warm, human, fast. |
| Studio collateral (print) | 03 + 01 | | No | Service menus, cards, packaging. Editorial, quiet. |

### What's new in 2026 (summary)

1. **Vertical video is the primary format.** Every shoot plans for 9:16, with 1:1 and 16:9 derived from the same source. See `photography_and_video_2026.md`.
2. **Emoji are allowed on social surfaces** (captions, stories, TikTok voice) — *never* in owned UI, subject lines, thumbnails, or editorial copy. Pillar 02 gets more breathing room than before.
3. **UGC &amp; creator-led content** gets a floor (daylight only, no beauty filters, one product per shot) and a frame (HairMNL reel-cover chrome is always applied when reposting). Full brief template in the photo/video addendum.
4. **Motion is codified.** `motion.css` defines durations, easings, scroll-reveal, page-transitions, toast + modal entrances, skeleton shimmer — all respecting `prefers-reduced-motion`.
5. **Accessibility has its own doc.** `accessibility_spec.md` sets contrast minimums, focus ring, touch targets, ARIA patterns, and a launch checklist.
6. **The component library grew.** Toasts, modals, badges, stock pills, sale tags, tabs, accordions, reviews, rating summaries, filter drawer, sticky add-to-cart, quantity steppers, wishlist, free-ship progress, empty states, skeletons — see `preview/51_… 57_`.
7. **An icon fallback kit** (`assets/icons/sprite.svg`) covers all UI needs with a thin-stroke hand that matches the custom seal set.
8. **Responsive breakpoints** (sm 390, md 820, lg 1280, xl 1440) are tokenised in `responsive_and_a11y.css`.

### Cadence

| Surface | Frequency | Owner |
|---|---|---|
| IG feed | 4–6 / week | Social |
| IG stories | daily | Social |
| Reels / TikTok | 3–5 / week | Social + creator |
| YouTube | 1 / week (Thu 6 PM PHT) | Video |
| Pinterest | 10 / week (batched) | Social |
| Newsletter (*The Brief*) | monthly (1st Wed) | Editorial |
| Transactional email | on-event | Ops |
| Paid ads | always-on, rotated weekly | Growth |
| Studio collateral | seasonal | Studio lead |

### Content pillars ↔ YouTube formats

| YouTube format | Pillar | Frame colour |
|---|---|---|
| Routine | 03 + 01 | ink chip |
| Tutorial | 01 | honey chip |
| Review | 01 | honey chip on ink |
| Collab | 03 | ink chip |
| GRWM | 02 + 03 | ink chip on blush |

---
