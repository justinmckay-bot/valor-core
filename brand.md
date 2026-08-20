# brand.md (Valor Church)

The non-negotiables, plus the full Valor design system. Apply these to every visual, printed, social, slide, web, and digital asset.

This file is internal working documentation. Em dashes are fine here. They are not fine in public-facing Valor copy.

> Source: consolidated from the original `brand.md` and the **Valor Church Design System** (Remix), which mirrors `justinmckay-bot/valor-print-design-skill`. The design system's living files (CSS tokens, fonts, six logo lockups, slide and website kits, reference PDFs) are the production assets behind these rules.

---

## Naming

- Full name: **Valor Church**
- Short form: **Valor** (acceptable in casual or repeated reference)
- Former name: **The Local Church (TLC)**, used through February 2026
- Identity: an SBC and Send Network church plant in NW Arvada, Colorado
- Never write: Ballard, Ballard Church, or any voice-to-text corruption

## Venue

- Always **Excel Academy** or **Excel Academy Charter School**
- Never "Excel Charter Academy"
- Address: **11500 W 84th Ave, Arvada, CO 80005**
- Service times: **two Sunday services begin August 30, 2026, at 8:30a and 10:30a** (one service at 10a before that date). Lowercase `a`, no space, no period.

## Digital

- URL: **valor.church** (always lowercase, never `Valor.church`, never `https://valor.church` in display copy)
- Social handle: **@myvalorchurchco** (verbatim, lowercase)
- Partner site: **partnerwithvalor.church**

## Verbatim recurring copy

Use these exact words. Do not paraphrase.

| What | Exact wording |
|---|---|
| Mission | Exalt God by boldly making disciples of valor, uniting as a faith family, and serving our city. |
| Tagline | Stop Drifting. Build Resilient Faith. |
| Motto | All for Him. All Excellent. All In. |
| Four pillars (always this order) | Unapologetic Preaching. Unashamed Worship. Unafraid Witness. Unceasing Prayer. |
| URL | valor.church |
| Social | @myvalorchurchco |
| Address | 11500 W 84th Ave, Arvada, CO 80005 |
| Service times | Two services from Aug 30, 2026: 8:30a and 10:30a (10a before then) |

---

## The two visual modes

Every Valor artifact belongs to one of two modes. Choose before you design. They are intentionally in tension. Don't smooth it out.

**MODE 1 — DARK AUTHORITY.** Full-bleed black (`#0d0d0d`) with a ghost V-mark cropping off the right edge, Archivo Black headlines in white, PT Serif Italic sub-lines in khaki, a top khaki accent strip, and a left burgundy rail. Register: *"We know who we are."* Use for campaign covers, directional signage, lanyards, event cards, outreach pieces, sermon-series openers.

**MODE 2 — WARM CLARITY.** Off-white (`#f7f4f0`) page with a dark header bar over a khaki rule, a left burgundy rail in the content zone, Archivo Bold labels, PT Serif Bold questions, PT Serif Regular body, warm-mid callout boxes with a left burgundy accent. Register: *"Come in. There's room here."* Use for small group guides, pastoral letters, sermon notes, discipleship resources, forms.

---

## Color

### Official brand sheet (the four)

| Color | Hex |
|---|---|
| Black | #000000 |
| Burgundy | #4D3033 |
| Khaki | #9F936B |
| Slate | #3B4A50 |

### Working / extended tokens (screen + Mode 2 surfaces)

| Token | Hex | Use |
|---|---|---|
| `--black` | #0d0d0d | Mode 1 background (softer than pure black) |
| `--dark` | #1a1a1a | headers, primary text, footer bars |
| `--burgundy` | #4D3033 | rails, badges, callouts (primary accent) |
| `--khaki` | #b5a97a | working khaki, lighter for screens |
| `--khaki-dim` | #8a7a55 | URLs, subdued accents |
| `--white` | #ffffff | text on dark / on burgundy |
| `--off-white` | #f7f4f0 | Mode 2 page background |
| `--warm-mid` | #ede8e0 | callout box background only |
| `--rule-warm` | #cdc5bb | write lines, warm dividers |
| `--body-text` | #2e2e2e | all paragraph body copy |
| `--ghost` | #232323 | ghost V-mark stroke (Mode 1) |

### The maroon rule (global, non-negotiable)

Whenever burgundy `#4D3033` is the background — a rail, strip, badge, callout border, header band, sidebar, anything — the text on top of it must be **WHITE**. Never dark. Never near-black. Khaki on burgundy is allowed only for ≤8pt secondary labels, never primary copy. Before rendering any text, ask: what color is the fill directly behind these characters?

### Distribution

Color is never distributed evenly. Two-thirds of every surface is black (Mode 1) or off-white (Mode 2). Khaki is an accent, never a primary fill. Burgundy is reserved for rails, badges, and small accents, never a large background. No gradients, anywhere, ever. Slate is used sparingly.

---

## Type

Two families, ever. **Archivo** for display and labels (Black for headlines, Bold for labels, Regular only for sub-body). **PT Serif** for body and emphasis (Regular for paragraphs, Bold for questions, Italic for framing lines). Never Helvetica, Times, system-ui, Inter, Roboto, or any "sensible default." Type carries the brand more than color does. Both families ship locally (Archivo as a variable font plus statics, PT Serif as the four-style set); no Google Fonts dependency at runtime.

### Scale (preserve all four distinct levels, never flatten)

| Role | Size | Font / weight |
|---|---|---|
| Display (Mode 1 headline) | 36px (28px small) | Archivo Black |
| Series title (Mode 2) | 18px | Archivo Black |
| Question | 17px | PT Serif Bold |
| Body | 15px | PT Serif Regular |
| Callout | 14px | PT Serif Regular |
| Wordmark | 28px | Archivo Black |
| Label | 10px tracked +0.14em | Archivo Bold |
| Tagline / footer | 11px | PT Serif Italic / Regular |

Body copy never goes below 11pt in print or 15px on screen.

### Casing

- **ALL CAPS — Archivo Bold/Black only.** Section labels, document-type labels, wordmarks, top-of-page directional labels. Tracked +1.5. Never ALL CAPS in PT Serif.
- **Title Case** for series titles, document titles, event names.
- **Sentence case** for body copy, questions, callouts, captions.
- Never Title Case inside body copy or buttons.

---

## Voice and content

Posture: **bold but human**. Not corporate, not casual-cool, not winking at the camera. A pastor who's done the reading, talks plainly, and means what he says.

- **Tone.** Direct. Short sentences, verbs first. Theological without jargon ("disciples of valor," not "spiritual formation outcomes"). Warm authority. Hospitable, not chummy ("You're welcome here," never "Hey friend!").
- **Person.** "We" = the church as a family (we exalt, we build, we serve), never "we" = the staff. "You" addresses the reader. "I" only in pastoral letters, signed simply *Justin*.
- **No em dashes in public-facing copy** (emails, social, print, handouts, slides, signage). Use a period or colon. Fine in internal `.md` only.
- **Slogans/taglines/mottos end with a period.** "Stop Drifting. Build Resilient Faith."
- **Numerals for time.** `8:30a`, `10:30a`. En dash for ranges only: `10:00–11:00a`.
- **No emoji. Ever.** Print, social, web, slides, email. Emoji break the serious register.
- **No corporate jargon** ("outcomes," "scalable," "high-impact"). No casual-cool ("check us out").

---

## Layout

- **Left-aligned, always.** Type aligns to the rail or content margin. Centered headlines only for vertical lockups and signage. Never center body copy.
- **Generous margins.** US Letter at 0.65" margin, content width 7.2". Web at `min(120px, 8vw)` outer padding.
- **Vertical rhythm in tokens.** Spacing xs/sm/md/lg/xl = 8 / 14 / 23 / 35 / 50px. Never half-values.
- **Right-edge clip is the most common production error.** Always wrap to content width minus right margin.
- **Fixed structures.** Top khaki strip (Mode 1) and left burgundy rail (both modes) are page-fixed, never floated, never optional. Rail width 6px; khaki strip 4px.
- **Sections stack vertically**, separated by double rules or section labels, never by colored backgrounds. No "hero with three feature cards in a grid."

### Backgrounds

Full-bleed black (Mode 1) with the ghost V-mark cropped off the right edge at 8–12% opacity. Solid off-white (Mode 2), never patterned, never gradient; warm-mid (`#ede8e0`) reserved for callout boxes only. No images as backgrounds; photography lives inside a card or frame. No gradients.

### Borders, radii, shadows

- Crisp rectangles. Badges max 2px radius; cards max 4px (often 0); images 0; inputs 2px.
- Hairline borders are 0.6px warm-rule color, not gray, not black.
- **Double rule** (the signature move): a 0.9pt khaki line over a 0.3pt dark line, 4px gap. Section opener (after series titles, Mode 2) and closer (above tagline footers). Never a single rule where a double rule belongs.
- No drop shadows. Mode 1 has none. Mode 2 cards are flat warm-mid with a left burgundy accent; if lift is needed, a thin warm hairline under the card, never a soft shadow. No backdrop blur, no glassmorphism.

### Imagery

Warm, slightly desaturated, softly grainy. No cold blues, no high-saturation pastels, no teal/orange cinematic grades. B&W acceptable for pastoral portraits. Always framed by structural elements, never bled behind type. The mark and a photo are never overlaid.

### Animation (print-first; rare)

Ease-out `cubic-bezier(0.2, 0.8, 0.2, 1)` or linear for rails. Never bouncy. 180–280ms hover/press, 400–600ms entrance. Fades and slight upward translates (8–16px). No carousels, parallax, or Lottie. Hover: khaki underline on links, 92% opacity on buttons, no scale. Press: burgundy darkens to `#3a2326`. Focus: 2px khaki outline at 2px offset, never browser blue.

---

## Iconography

The wordmark and the V-mark do the work an icon system would do elsewhere.

- **The V-mark** (two stacked hollow chevrons) is the primary icon at any size: ghost background (~95% canvas height, cropped, 8–12% alpha, from `mark-light.png`); full-opacity logo on covers and slides; or part of a lockup (horizontal for inline, vertical for stacked/centered).
- **Six logo lockups** live in `assets/logo/`: mark / horizontal / vertical, each in dark-ink and light-ink. 3000×3000 transparent PNGs.
- **Numbered badges** are typographic: burgundy fill, white Archivo Bold numerals at 7.5pt, 2pt radius. Used to number questions, form steps, commitments.
- **Functional icons** (web nav, form indicators only): **Lucide**, 1.75px stroke, outline only, sized in steps of 4 (16/20/24/32px). `--dark` on light, `--khaki` on dark, `--burgundy` for small accent rows. Never filled. Never mix icon libraries.
- **No emoji, no decorative unicode glyphs** (• ◦ † ★). Bullets render as `•` only when no Archivo Bold label hierarchy is available.

---

## Logo asset naming (read carefully)

The `-dark` / `-light` suffix names the **ink color of the asset**, not the background it sits on.

- `*-dark.png` = dark ink, use on **LIGHT** backgrounds.
- `*-light.png` = light ink, use on **DARK** backgrounds.

Selection is inverted from the fill: dark fill → light asset; light fill → dark asset.

---

## The motto

**All for Him. All Excellent. All In.**

Render as three stacked lines, or one line with periods between phrases. Never with em dashes between the phrases.

---

## What we do not do

- No generic AI aesthetic. No stock-feeling gradient swirls. No over-rounded "modern church" sans-serif templates.
- No em dashes in any public-facing copy. No emoji anywhere.
- No fonts outside Archivo and PT Serif. No colors outside the palette. No gradients.
- No dark or near-black text on a burgundy fill.
- No watercolor, pastel washes, or gradient millennial pinks.
- No backdrop blur, glassmorphism, drop shadows, or carousel/parallax motion.
- No softening the four pillars into something less direct.

## When in doubt

Pick a mode. Black, burgundy, khaki, slate. Archivo Black, PT Serif. White on burgundy, always. Excel Academy, two Sunday services (8:30a and 10:30a from Aug 30, 2026), valor.church. The four pillars in order. Left-aligned, crisp rectangles, the ghost V-mark and the rail. That is the brand.
