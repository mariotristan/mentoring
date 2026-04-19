# Mentoring Application Page

Static application form for a free 1-on-1 mentoring program in Cloud (Azure / AWS / GCP), DevSecOps, IaC & CI/CD, and Platform Engineering.

## Stack

- Single `index.html` — no framework, no build step
- Cloudflare Worker — proxy that keeps secrets server-side
- Cloudflare Turnstile — bot protection with server-side token verification
- Google Apps Script + Google Sheet — stores every submission

## Features

- Mentor bio with LinkedIn link
- Real-time form progress bar
- Per-field validation with inline error messages
- Honeypot + Turnstile bot protection
- CTA button hides after successful submission
- Open Graph + Twitter Card meta tags for social sharing

## What's in this repo

| File | Purpose |
|---|---|
| `index.html` | The application form |

Setup files (`SETUP.md`, `sheets-script.gs`, `worker.js`) are kept locally and not published.

## Deployment

1. Follow `SETUP.md` (local) to configure the Google Sheet, Apps Script, Turnstile, and Cloudflare Worker.
2. Replace `YOUR_CLOUDFLARE_WORKER_URL` in `index.html` with your Worker URL.
3. Replace `YOUR_TURNSTILE_SITE_KEY` in `index.html` with your Turnstile site key.
4. Host `index.html` on GitHub Pages, Cloudflare Pages, or Netlify.
