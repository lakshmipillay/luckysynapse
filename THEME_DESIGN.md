# Lucky Synapse — "The Architect" Theme

## Design Philosophy
**"Warm Precision"** — An architect's blog that reads like a well-engineered document. Serif headings give editorial weight; sans-serif body keeps it scannable. Teal accent says "modern builder" without the corporate blue cliché.

---

## Typography

### Font Pairing: DM Serif Display + Inter
| Role | Font | Why |
|------|------|-----|
| **Display** | DM Serif Display | Modern optical serif — editorial weight without old-world stiffness. Distinctive vs Playfair (HoraNow uses Playfair). |
| **Body** | Inter | The gold standard for UI readability. Clean, neutral, excellent at all sizes. |
| **Code** | JetBrains Mono | Ligatures, clean geometry, pairs well with Inter. |

### Google Fonts Load
```
DM Serif Display: 400
Inter: 300, 400, 500, 600, 700
JetBrains Mono: 400, 500
```

### Type Scale
| Token | Size | Weight | Spacing | Usage |
|-------|------|--------|---------|-------|
| `--text-xs` | 0.75rem | 500 | +0.01em | Badges, pills |
| `--text-sm` | 0.875rem | 400 | 0 | Meta, captions |
| `--text-base` | 1rem | 400 | -0.01em | Body |
| `--text-lg` | 1.0625rem | 400 | -0.01em | Post content |
| `--text-xl` | 1.25rem | 600 | -0.02em | Card titles |
| `--text-2xl` | 1.5rem | 700 | -0.02em | Section headers |
| `--text-3xl` | 2rem | 700 | -0.025em | Page titles |
| `--text-4xl` | 2.5rem | 400 | -0.02em | Hero (serif, natural weight) |

**Key:** Headings use DM Serif Display at its natural weight (400) — the serif does the heavy lifting, no need for bold. Body uses Inter with varied weights for hierarchy.

---

## Color: Teal Accent

### Why Teal for Tech
- **Not corporate blue** (every SaaS uses #2563EB)
- **Not generic green** (too "success state")
- **Warm but technical** — bridges the personal/tech divide
- **Distinctive from HoraNow's gold** — no visual confusion in Fora showcase

### Light Mode
| Token | HEX | Usage |
|-------|-----|-------|
| `--bg` | `#F8F9FA` | Page — warm white |
| `--surface` | `#FFFFFF` | Cards |
| `--elevated` | `#F1F3F5` | Code blocks, TOC |
| `--text` | `#1A1D23` | Body — soft black |
| `--text-secondary` | `#5C6370` | Meta |
| `--text-tertiary` | `#9098A3` | Timestamps |
| `--accent` | `#0D9488` | Teal-600 — links, CTAs |
| `--accent-hover` | `#0F766E` | Teal-700 |
| `--accent-soft` | `#F0FDFA` | Tags, highlights |
| `--border` | `#E2E5EA` | Dividers |
| `--border-accent` | `#99F6E4` | Focus rings |

### Dark Mode
| Token | HEX | Usage |
|-------|-----|-------|
| `--bg` | `#0F1219` | Page — blue-black |
| `--surface` | `#181C25` | Cards |
| `--elevated` | `#222730` | Code blocks |
| `--text` | `#E8EBF0` | Body |
| `--text-secondary` | `#8B93A0` | Meta |
| `--text-tertiary` | `#5C6370` | Timestamps |
| `--accent` | `#2DD4BF` | Teal-400 — links |
| `--accent-hover` | `#5EEAD4` | Teal-300 |
| `--accent-soft` | `#134E4A` | Tags |
| `--border` | `#2A2F3A` | Dividers |
| `--border-accent` | `#0D9488` | Focus rings |

---

## Spacing & Layout
- **Max content width:** 720px (readable measure)
- **Nav max width:** 1024px
- **Grid:** 4px base → 4, 8, 12, 16, 24, 32, 48, 64
- **Border radius:** 8px (cards), 6px (buttons), 9999px (pills)

---

## Component Specs

### Navigation
- 56px height, sticky, `bg-surface` with 1px border-bottom
- Logo: DM Serif Display, 1.25rem, `--text` color
- Links: Inter 0.875rem, weight 500, `--text-secondary` → `--text` on hover
- Active: `--accent` color + 2px bottom border

### Post Cards
- `bg-surface`, 1px `--border`, 8px radius
- Padding: 24px
- Shadow: 0 1px 2px rgba(0,0,0,0.04) → 0 4px 12px on hover
- Hover: translateY(-2px), border tints to accent at 25%
- Title: DM Serif Display, 1.25rem, natural weight feels heavier
- Excerpt: Inter, 0.9375rem, `--text-secondary`, 2-line clamp

### Tags
- `--accent-soft` background, `--accent` text
- 0.75rem, weight 600, pill shape
- Hover: fills to `--accent` background, white text

### Code Blocks
- `--elevated` bg, 1px `--border`, 8px radius
- JetBrains Mono, 0.8125rem
- Inline code: same bg + `--accent` text color

### Buttons
- `bg-surface`, 1px `--border`, 6px radius
- Weight 600, 0.875rem
- Hover: border → `--accent`, text → `--accent`

### Fora Comments
- 48px gap above, thin 1px border separator
- "Discussion" label in `--text-tertiary`, DM Serif Display
- `data-theme="auto"` — follows site mode
- No extra container styling — let Fora breathe

---

## What Makes This Different from HoraNow
| Aspect | HoraNow | Lucky Synapse |
|--------|---------|---------------|
| Serif | Playfair Display (high contrast, dramatic) | DM Serif Display (geometric, modern) |
| Accent | Gold (#d4af37) — warm, celestial | Teal (#0D9488) — technical, fresh |
| Mood | Cosmic, mystical | Architectural, precise |
| Background | Pure black-blue (#0a0a12) | Warm grey (#F8F9FA / #0F1219) |
| Framework | Astro + Tailwind | Hugo + PaperMod |

---

## Accessibility
- All text meets WCAG AA (4.5:1 minimum)
- Teal accent passes on both light and dark backgrounds
- Focus rings on all interactive elements
- `prefers-reduced-motion` respected
