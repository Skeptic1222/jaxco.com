# jaxco.com

Cloudflare Pages placeholder for **Jaxco** — Jacqueline Patterson's domain. Pre-refresh as of 2026-05-03.

## Status

Single-page neutral placeholder. The real content/files are coming from Jacqueline shortly. The historical 1997–2004 archive (still serving over HTTP because origin SSL is broken) is captured under `migration-snapshots/jaxco-2026-05-03/`.

## Files

| Path | Purpose |
|------|---------|
| `index.html` | Single placeholder page |
| `404.html` | Custom 404 |
| `_headers` | Cloudflare Pages security headers |
| `_redirects` | `www` → apex, 308 |
| `robots.txt` | `Disallow: /` until refresh content lands |
| `sitemap.xml` | One URL — root |
| `favicon.svg` | Italic "J" monogram |
| `migration-snapshots/jaxco-2026-05-03/` | Full snapshot of the live HTTP site (4 HTML pages + 14 GIFs + style.css) |
| `CLAUDE.md` | Per-site rules for future Claude sessions |

## Migration archive

The live site at `http://jaxco.com/` (HTTPS broken — 525 SSL handshake) is "JAXCO Design & Development" from 1997–2004 ("premier Los Angeles web shop"). Pulled in full to `migration-snapshots/jaxco-2026-05-03/` per the migration rule in `..\flourandfrond\CLAUDE.md` ("Save files to disk before any change").

When the new content arrives, that archive can either:
- Live at `/archive/` as a deliberate retrospective, or
- Be removed from production and kept only in this folder for memory-keeping.

## Deploy

Cloudflare Pages auto-deploys from `main` on `github.com/Skeptic1222/jaxco.com` once the project is connected. The Pages project lives on Jacqueline's Cloudflare account.

## Brand tokens (placeholder period)

Intentionally neutral so it's easy to swap when the real content arrives:

- **Palette:** Bone `#F5F1E8` (background), Warm Gray `#5C5751` (text)
- **Type:** Newsreader (italic for the wordmark)
- **No bold accent colour** — keeping it quiet during the transition.
