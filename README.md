# Air Hackathon 2027

Website for [airhackathon.com](https://airhackathon.com): an open-innovation challenge on air quality in Dhaka, run by Cedar Initiative.

A single static page (`index.html`), no build step. It deploys to GitHub Pages from `main` through `.github/workflows/deploy.yml`.

## How it works

- **The header** is a WebGL shader: a procedural Dhaka skyline under smog. The smog's density comes from the live PM2.5 reading, wind direction drives its drift, and the pointer clears it. It follows the system light/dark setting, has a Pause control, and stays still under `prefers-reduced-motion`.
- **Live air** uses the [Open-Meteo](https://open-meteo.com) air-quality and weather APIs (no key needed). It refreshes every 10 minutes. Location is only requested when the visitor presses **Use My Location**.
- **Assets:** `favicon.svg` and `assets/cedar-initiative-logo.svg` come from the Cedar Initiative logo. `og.png` is the 1200×630 share image.

## Editing

Copy for the problems and the 2027 plan sits in plain HTML in `index.html`. Change the plan steps once dates and venue are confirmed.
