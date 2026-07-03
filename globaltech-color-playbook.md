# GlobalTech Website — Color Playbook

A reference guide for the design/dev team. Four blue tiers, each with a defined job. Use the CSS variable names when building components so everyone stays consistent.

---

## 1. Dominant — Deep Royal Blue
**Hex:** `#1B2A6B`
**CSS var:** `--color-dominant`

**Role:** The anchor color. Highest visual weight, lowest lightness, used sparingly but always in the same spots so it reads as "structure," not decoration.

**Where it lives:**
- Main navigation bar background
- Footer background
- Hero section background (full-bleed)
- Page section dividers (thin bars/borders between major sections)

**Do not use for:** body text, small UI elements, or anything a user needs to read for long — too dark/heavy for large text blocks.

---

## 2. Sub-dominant — Cobalt Blue
**Hex:** `#2E45B8`
**CSS var:** `--color-subdominant`

**Role:** Secondary structural color. One step lighter than dominant, used to create depth without competing with it. This is your "brand blue" — closest match to the actual shirt/logo color, so it's the one people will visually associate with GlobalTech.

**Where it lives:**
- Card backgrounds (program cards, course cards, testimonial cards)
- Secondary section backgrounds (alternating with white/light-neutral sections)
- Sidebar panels
- Tab/pill backgrounds (active state, non-hover)
- Icon fills on light backgrounds

**Do not use for:** primary nav or footer — that's dominant's job. Mixing them there flattens the hierarchy.

---

## 3. Child — Soft Indigo
**Hex:** `#5A72E0`
**CSS var:** `--color-child`

**Role:** Interaction feedback. This color should only appear *in response to user action* — hover, focus, active states. If it's showing up on page load with nothing touching it, it's being misused.

**Where it lives:**
- Link hover color
- Nav item hover/underline
- Card hover border or shadow tint
- Icon hover state
- Input field focus border
- Non-primary button hover state

**Do not use for:** static/default states. It should always signal "you're interacting with this right now."

---

## 4. Sub-child — Sky Accent
**Hex:** `#3DA9FC`
**CSS var:** `--color-accent`

**Role:** The attention-getter. Deliberately breaks from the navy family into a brighter, more saturated blue so it never gets lost against the darker tiers. Reserve this for things you actually want clicked or read first.

**Where it lives:**
- Primary CTA buttons ("Register Now," "Apply Now," "Get Free Laptop")
- Highlighted stats/numbers (e.g., "25 Years," "500+ Graduates")
- Badges/tags ("New," "Enrolling Now")
- Key text you want to pull the eye to inside body copy (dates, deadlines)

**Do not use for:** large backgrounds or big blocks of text — it's built to pop in small doses, not to be stared at.

---

## Supporting Neutrals

**Background:** `#F5F7FC` — `--color-bg`
Light blue-white, not pure white. Used for default page/body background so the whole site stays in the blue family even where there's no blue.

**Body text:** `#1A1A2E` — `--color-text`
Near-black with a blue undertone. Use for all paragraph/body copy — never use dominant or sub-dominant for long-form text, they're too saturated to read comfortably at length.

---

## Quick Reference Table

| Tier | Name | Hex | CSS Var | Primary Use |
|------|------|-----|---------|--------------|
| 1 | Dominant | `#1B2A6B` | `--color-dominant` | Nav, footer, hero |
| 2 | Sub-dominant | `#2E45B8` | `--color-subdominant` | Cards, panels, section backgrounds |
| 3 | Child | `#5A72E0` | `--color-child` | Hover/focus states only |
| 4 | Sub-child | `#3DA9FC` | `--color-accent` | Buttons, CTAs, badges, highlighted text |
| — | Background | `#F5F7FC` | `--color-bg` | Page/body background |
| — | Text | `#1A1A2E` | `--color-text` | Body copy |

---

## CSS Variables (drop-in)

```css
:root {
  --color-dominant: #1B2A6B;
  --color-subdominant: #2E45B8;
  --color-child: #5A72E0;
  --color-accent: #3DA9FC;
  --color-bg: #F5F7FC;
  --color-text: #1A1A2E;
}
```

## Team Rule of Thumb

If you're unsure which tier to use, ask: **"Is this structure, surface, interaction, or action?"**
- Structure → Dominant
- Surface → Sub-dominant
- Interaction (hover/focus) → Child
- Action (click me) → Sub-child
