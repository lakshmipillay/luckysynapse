# Lucky Synapse

Clean architecture. Real AI. No hype.

## Tech stack

- **Hugo** — static site generator
- **PaperMod** — minimal theme
- **Giga.mobile (Fora)** — comments with edge-native performance
- **Cloudflare Workers** — hosting (via wrangler)

## Theme: Giga.mobile Harmony

Custom CSS theme matching giga.mobile's clean, modern aesthetic:

- **Design tokens**: Blue accent (#3b82f6), clean grays, smooth transitions
- **Dark/light mode**: Seamless integration with Fora's theme toggle
- **Typography**: System font stack for fast loading
- **Components**: Rounded cards, subtle shadows, hover effects
- **Spacing**: Consistent 8px grid
- **Accessibility**: Focus styles, prefers-reduced-motion support

Theme file: `assets/css/extended/blank.css`

## Local dev

```bash
hugo server -D
```

## Deploy

Push to master → Cloudflare Workers auto-deploys (via wrangler).

## Giga.mobile (Fora) comments

1. Sign up at [giga.mobile](https://giga.mobile)
2. Get your site key
3. Already configured in `hugo.toml` — replace the placeholder key

## Structure

- `content/tech/` — architecture, AI, backend posts
- `content/personal/` — personal essays (ready when you are)
- `layouts/partials/comments.html` — Fora integration
