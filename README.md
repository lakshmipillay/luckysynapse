# Lucky Synapse

Clean architecture. Real AI. No hype.

## Tech stack

- **Hugo** — static site generator
- **PaperMod** — minimal theme
- **Fora** — comments (giga.mobile)
- **Cloudflare Pages** — hosting

## Local dev

```bash
hugo server -D
```

## Deploy

Push to GitHub → Cloudflare Pages picks it up.

## Fora comments

1. Sign up at [giga.mobile](https://giga.mobile)
2. Get your site key
3. Add `foraSiteKey = "your-key"` to `hugo.toml` under `[params]`

## Structure

- `content/tech/` — architecture, AI, backend posts
- `content/personal/` — personal essays (ready when you are)
- `layouts/partials/comments.html` — Fora integration
