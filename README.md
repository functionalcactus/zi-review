# Zi Review 字

A personal Mandarin study app for the Boya 中级冲刺 course: spaced-repetition reviews (FSRS), finger handwriting with stroke checking, flashcards and 听写 tests. Works offline as a home-screen web app; all progress is stored on each user's own device.

## Layout

- `public/` – the app (static files, no build step)
  - `index.html` – the whole app, including the built-in lessons
  - `sw.js` – offline support; bump `CACHE` when files change so phones pick up updates
  - `strokes.js`, `hanzi-writer.min.js` – stroke data and handwriting library ([Hanzi Writer](https://hanziwriter.org), MIT; stroke data from Make Me a Hanzi, Arphic Public License, see `ARPHICPL.TXT`)
- `wrangler.jsonc` – Cloudflare Workers config (static assets from `public/`)

## Deploy

Pushing to `main` deploys automatically once the Cloudflare Worker is connected to this repo (Workers & Pages → zi-review → Settings → Build).

Manual deploy: `npx wrangler deploy`

Auto-deploy from GitHub connected on 2026-11-24.
