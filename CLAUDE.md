# CLAUDE.md — jaxco.com

This file provides guidance to Claude Code when working on this repository.

## Project Purpose

Cloudflare Pages site for **jaxco.com** — Jacqueline Patterson's existing domain. As of 2026-05-03 the live site is a 1997–2004 web-design portfolio ("JAXCO Design & Development") that's still serving over HTTP because origin SSL is broken. This repo replaces it with a quiet "we're refreshing things" placeholder while we wait for her current files.

## Status

| Item | State |
|------|-------|
| Migration snapshot of live site | ✅ `migration-snapshots/jaxco-2026-05-03/` (4 HTML + 14 GIFs + style.css) |
| Placeholder page + framework files | ✅ Built |
| Local `.git` + first commit | 🔄 This session |
| GitHub remote `Skeptic1222/jaxco.com` | 🔄 This session |
| Cloudflare Pages project on Jacqueline's account | ⏳ Pending Playwright session |
| Custom domain attached | ⏳ Same — domain already on her CF DNS |
| Real refreshed content | ❌ Out of scope this pass — Jacqueline supplies files later |

## Live-site state at snapshot time (2026-05-03)

- HTTPS returns Cloudflare error 525 (SSL handshake failed at origin)
- HTTP returns the 1997–2004 site (HTML 4.01 Transitional, GIF rollovers, "©1997-2004")
- A records point at Cloudflare IPs — domain is on her CF DNS
- Content: home page, `apropos.html` (about), `portfolio.html`, `contact.html`, `style.css`
- Email: `[email-protected]` placeholder rendered through CF email-decode script (so an obfuscated mailto exists somewhere — not extracted here)

## Accounts & Ownership

- **Cloudflare account owner:** Jacqueline Patterson — `jaxdilpat@gmail.com`
- **Cross-account admin:** Shannon Patterson — `shannon.patterson@ayitcreativity.com`
- **GitHub:** `github.com/Skeptic1222/jaxco.com`

## Hard rules for this site

- **Don't touch the migration snapshot** — it is the historical record. Any edits there break preservation.
- **Don't index the placeholder.** `robots.txt` is `Disallow: /`. When real content lands, flip it then — not before.
- **Don't make brand commitments in the placeholder.** It's intentionally generic until Jacqueline supplies files. No tagline, no dates, no claims.
- Wife-friendly Playwright rules from `..\flourandfrond\CLAUDE.md` apply — confirm before any visible change to the live site, no jargon, save before changing.

## When the new content arrives

1. Pull her files into the working tree (probably under a temporary `incoming/` directory first).
2. Decide: full replacement, multi-page site, or a simple about-page situation?
3. Replace `index.html` (and add other pages as needed).
4. Flip `robots.txt` to `Allow: /` and expand `sitemap.xml`.
5. Decide what to do with `migration-snapshots/` — keep it private (this repo) or expose at `/archive/`.
6. Commit + push; Cloudflare Pages auto-deploys.

## Pattern: Cloudflare Pages Placeholder

Identical to `..\flourandfrond\` and `..\imwalkinghere.com\` — static `index.html` + inline CSS + standard framework files. No build step. Pages auto-deploys from `main`.

## Parent-Project Conventions (inherited)

See `..\..\..\CLAUDE.md` (`D:\Projects\ayitcreativity\CLAUDE.md`) for portfolio rules.
