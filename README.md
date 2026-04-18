# Mentoring Application Page

Static application form for a free 1-on-1 mentoring program in Cloud (Azure / AWS / GCP), DevOps, and Platform Engineering.

## Stack

- Single `index.html` — no framework, no build step
- Cloudflare Worker — proxy that keeps secrets server-side
- Google Apps Script + Google Sheet — stores every submission

## What's in this repo

| File | Purpose |
|---|---|
| `index.html` | The application form |

Setup files (`SETUP.md`, `sheets-script.gs`, `worker.js`) are kept locally and not published.

## Deployment

1. Follow `SETUP.md` (local) to configure the Google Sheet, Apps Script, and Cloudflare Worker.
2. Replace `YOUR_CLOUDFLARE_WORKER_URL` in `index.html` with your Worker URL.
3. Host `index.html` on GitHub Pages, Cloudflare Pages, or Netlify.
