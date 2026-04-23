# HairMNL · Accessibility spec

> Minimum bar for every surface shipping under the HairMNL brand. Designers and engineers both sign off on this before launch.

---

## 1. Contrast

We target **WCAG 2.2 AA** on all body text and interactive elements. Large display type (≥32 px) may use AA-Large (3:1), but only when the composition explicitly calls for a quiet pairing.

### Approved foreground × background pairings

| Foreground | Background | Ratio | Status |
|---|---|---:|---|
| `#1A1A1A` Ink | `#FAF6F2` Paper | **17.1 : 1** | AAA |
| `#1A1A1A` Ink | `#F3EEE7` Paper warm | **16.1 : 1** | AAA |
| `#1A1A1A` Ink | `#EFE6E3` Blush | **15.0 : 1** | AAA |
| `#1A1A1A` Ink | `#E5DEE7` Lilac | **14.6 : 1** | AAA |
| `#1A1A1A` Ink | `#DDE3D8` Sage | **14.6 : 1** | AAA |
| `#1A1A1A` Ink | `#D6CFC6` Stone | **12.6 : 1** | AAA |
| `#1A1A1A` Ink | `#C9A959` Honey | **6.1 : 1** | AA |
| `#FAF6F2` Paper | `#1A1A1A` Ink | **17.1 : 1** | AAA |
| `#FAF6F2` Paper | `#3E3A36` Ink soft | **11.0 : 1** | AAA |
| `#5D564E` Ink muted | `#FAF6F2` Paper | **6.9 : 1** | AA |
| `#3E3A36` Ink soft | `#FAF6F2` Paper | **10.4 : 1** | AAA |

### Banned pairings (fail AA)
- Honey on paper for body copy (2.5:1) — display only.
- Blush on paper (1.1:1) — surface on surface, never text.
- Paper on honey for body copy (2.5:1).

### Status pills
All status pills have been tuned to ≥4.5:1 against their background. Source: `colors_and_type.css` — `--status-*-fg` on `--status-*-bg`.

---

## 2. Typography

- **Body minimum:** 14 px (0.875 rem). 16 px preferred.
- **Mobile minimum:** 15 px body. Never smaller than 12 px for captions, and captions must be paired with a 14 px+ label.
- **Line-height:** 1.5–1.65 for body prose; 1.1–1.2 for display.
- **Line length:** 45–75 characters. Enforce via `max-width: 65ch` on long-form blocks.
- **Never letter-space lower-case body copy.** Tracking is reserved for the mono caps eyebrows.

---

## 3. Focus

A visible focus indicator is **required** on every focusable element. Our default is a 2 px offset Ink ring:

```css
:focus-visible {
  outline: 2px solid var(--hm-ink);
  outline-offset: 2px;
  border-radius: 2px;
}
```

On Ink surfaces, the ring switches to Paper. Never remove the outline; never replace with a shadow only. See `responsive_and_a11y.css`.

---

## 4. Touch targets

- **Minimum target size:** 44 × 44 px on mobile and tablet. iOS HIG compliant.
- **Minimum spacing between adjacent targets:** 8 px.
- Icon-only buttons must have 44 px hit area even if the icon itself is 24 px. Pad the button; don't scale the icon.
- The mobile tab bar uses a 60 px height minimum, with 48 px per tab.

---

## 5. Motion

Every animation in `motion.css` honours `prefers-reduced-motion`. When the preference is set:
- Durations collapse to 0.01 ms (functionally instant).
- Parallax, scroll-reveal, and autoplay video are disabled.
- State changes happen; they just don't animate.

**Never auto-play video with sound.** Reels-style silent autoplay is fine; unmuted autoplay breaks trust and accessibility.

---

## 6. Forms

- Every input has a visible label. Placeholder is **never** the label.
- Required fields are marked in copy ("Required"), not with an asterisk alone.
- Error states pair a colour cue with an icon and text. Never colour alone.
- Error text sits **directly below** the field it describes, announced via `aria-describedby`.
- Success confirmations are announced to screen readers via a live region (`role="status"`).

---

## 7. ARIA &amp; semantics

- Use semantic HTML first. ARIA is the fallback.
- Headings are hierarchical. One `<h1>` per screen. Don't skip levels.
- Landmarks on every page: `header`, `nav`, `main`, `footer`.
- Icon-only buttons must have `aria-label`.
- Images: informative = meaningful `alt`; decorative = `alt=""`.
- Modal dialogs use `role="dialog"` + `aria-modal="true"` + focus trap on open + focus restore on close + Esc to dismiss.
- Live announcements (cart updated, quiz progress) use `aria-live="polite"`. Reserve `assertive` for errors.

---

## 8. Content

- Plain language. Grade 8 reading level for body copy. The serif italic phrase is the one place we flourish.
- Sentence case for headlines. Title Case only in the mono caps eyebrows.
- Abbreviations and acronyms spelled out on first use.
- Emoji are allowed in captions and preheaders but **never** in UI labels, button text, or error messages — screen readers announce them and it gets tedious fast.
- Alt text describes the **purpose** of the image in context, not a literal scene description. "Conditioner bottle" is fine for a PDP. "Kérastase Résistance Bain 250 ml bottle" is better.

---

## 9. Video &amp; audio

- All video ships with **captions**. Auto-captions are the floor; hard-subs in our typography are the ceiling.
- Transcripts available for every YouTube episode (pasted into the description).
- Audio descriptions are not required for current content but should be considered when we start producing long-form visual content without voiceover.

---

## 10. Testing checklist (every launch)

- [ ] Keyboard-only walk-through of every flow.
- [ ] Screen reader pass with VoiceOver (iOS/macOS) and TalkBack (Android).
- [ ] Contrast check via axe DevTools — **zero serious violations**.
- [ ] Tap-target check at 320 px viewport.
- [ ] Reduced-motion check (macOS: System Settings → Accessibility → Display → Reduce motion).
- [ ] Zoom to 200% — layout still works, no content lost.
- [ ] Colour-blind preview (deutan + protan) — no info conveyed by colour alone.

Ship only when all pass.

---

*Owner: design. Engineering signs off. v2026.1 — April 2026*
