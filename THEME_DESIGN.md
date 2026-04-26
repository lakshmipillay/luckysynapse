# Lucky Synapse — Theme Design System

## Design Philosophy
**"Engineered Elegance"** — Clean enough for a backend architect, warm enough for personal stories. No decoration for decoration's sake.

---

## Color Palette

### Light Mode
| Token | HEX | Usage |
|-------|-----|-------|
| `--bg-primary` | `#FAFBFC` | Page background |
| `--bg-surface` | `#FFFFFF` | Cards, modals |
| `--bg-elevated` | `#F3F4F6` | Code blocks, TOC |
| `--text-primary` | `#111827` | Headings, body |
| `--text-secondary` | `#6B7280` | Meta, captions |
| `--text-tertiary` | `#9CA3AF` | Timestamps, hints |
| `--accent` | `#2563EB` | Links, CTAs |
| `--accent-hover` | `#1D4ED8` | Link hover |
| `--accent-soft` | `#EFF6FF` | Tag bg, highlights |
| `--border` | `#E5E7EB` | Dividers, card borders |
| `--border-focus` | `#93C5FD` | Input focus rings |

### Dark Mode
| Token | HEX | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0F1117` | Page background |
| `--bg-surface` | `#1A1D27` | Cards, modals |
| `--bg-elevated` | `#242836` | Code blocks, TOC |
| `--text-primary` | `#F3F4F6` | Headings, body |
| `--text-secondary` | `#9CA3AF` | Meta, captions |
| `--text-tertiary` | `#6B7280` | Timestamps, hints |
| `--accent` | `#60A5FA` | Links, CTAs |
| `--accent-hover` | `#93C5FD` | Link hover |
| `--accent-soft` | `#1E293B` | Tag bg, highlights |
| `--border` | `#2D3142` | Dividers, card borders |
| `--border-focus` | `#3B82F6` | Input focus rings |

### Semantic Colors (both modes)
| Token | Light | Dark | Usage |
|-------|-------|------|-------|
| `--success` | `#059669` | `#34D399` | Success states |
| `--warning` | `#D97706` | `#FBBF24` | Warnings |
| `--error` | `#DC2626` | `#F87171` | Errors |

---

## Typography

### Font Stack
| Role | Font | Fallback |
|------|------|----------|
| **Display** | `Inter` | `-apple-system, BlinkMacSystemFont, sans-serif` |
| **Body** | `Inter` | `-apple-system, BlinkMacSystemFont, sans-serif` |
| **Code** | `JetBrains Mono` | `'Fira Code', monospace` |

### Type Scale
| Token | Size | Weight | Line Height | Letter Spacing | Usage |
|-------|------|--------|-------------|----------------|-------|
| `--text-xs` | `0.75rem` (12px) | 500 | 1.5 | `+0.01em` | Badges, labels |
| `--text-sm` | `0.875rem` (14px) | 400 | 1.6 | `0` | Meta, captions |
| `--text-base` | `1rem` (16px) | 400 | 1.7 | `-0.01em` | Body |
| `--text-lg` | `1.125rem` (18px) | 400 | 1.7 | `-0.01em` | Post content |
| `--text-xl` | `1.25rem` (20px) | 600 | 1.4 | `-0.02em` | Section headers |
| `--text-2xl` | `1.5rem` (24px) | 700 | 1.3 | `-0.02em` | Card titles |
| `--text-3xl` | `2rem` (32px) | 700 | 1.2 | `-0.025em` | Page titles |
| `--text-4xl` | `2.5rem` (40px) | 800 | 1.1 | `-0.03em` | Hero titles |

---

## Spacing Scale
Based on 4px grid:
`4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96`

---

## Border Radius
| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `6px` | Buttons, tags |
| `--radius-md` | `8px` | Cards, inputs |
| `--radius-lg` | `12px` | Modals, hero sections |
| `--radius-full` | `9999px` | Avatars, pills |

---

## Shadows
| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-sm` | `0 1px 2px rgba(0,0,0,0.05)` | Subtle lift |
| `--shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | Cards |
| `--shadow-lg` | `0 8px 24px rgba(0,0,0,0.12)` | Hover, modals |
| `--shadow-glow` | `0 0 0 3px rgba(37,99,235,0.15)` | Focus ring |

---

## Component Specs

### Navigation Bar
- Background: `--bg-surface` with `border-bottom: 1px solid --border`
- Height: 56px
- Logo: `--text-xl`, weight 800, `--accent` color
- Links: `--text-sm`, weight 500, `--text-secondary` → `--accent` on hover
- Active link: `--accent` with 2px bottom border
- Max width: 1024px, centered

### Post Cards
- Background: `--bg-surface`
- Border: `1px solid --border`
- Radius: `--radius-lg`
- Padding: 24px
- Shadow: `--shadow-sm` → `--shadow-md` on hover
- Hover: translateY(-2px), border → `--accent` at 30% opacity
- Title: `--text-2xl`, weight 700
- Excerpt: `--text-base`, `--text-secondary`, 2-line clamp
- Meta: `--text-sm`, `--text-tertiary`

### Tags
- Background: `--accent-soft`
- Text: `--accent`, `--text-xs`, weight 600
- Padding: 4px 12px
- Radius: `--radius-full`
- Hover: background → `--accent`, text → white

### Buttons
- Primary: bg `--accent`, text white, `--radius-sm`
- Padding: 8px 20px
- Font: `--text-sm`, weight 600
- Hover: bg `--accent-hover`, shadow `--shadow-md`
- Focus: `--shadow-glow`

### Code Blocks
- Background: `--bg-elevated`
- Border: `1px solid --border`
- Radius: `--radius-md`
- Padding: 16px
- Font: `--text-sm` JetBrains Mono
- Line numbers: `--text-tertiary`

### Fora Comments Integration
- Container: no extra border/shadow — let Fora breathe naturally
- Gap: 48px above (matches post footer spacing)
- Separator: thin 1px `--border` line with "Discussion" label
- Fora config: `data-theme="auto"` to follow site dark/light mode

---

## Responsive Breakpoints
| Breakpoint | Width | Adjustments |
|------------|-------|-------------|
| Mobile | < 640px | Single column, 16px gutters, hero h1 → 1.75rem |
| Tablet | 640–1024px | Max-width 720px content |
| Desktop | > 1024px | Max-width 720px content, 1024px nav |

---

## Accessibility
- All text: WCAG AA contrast (4.5:1 body, 3:1 large text)
- Focus rings visible on all interactive elements
- Reduced motion: respect `prefers-reduced-motion`
- Font size: never below 12px
