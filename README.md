# Air Hackathon 2027

Website for [airhackathon.com](https://airhackathon.com): an open-innovation challenge on air quality in Dhaka, run by Cedar Initiative.

A single static page (`index.html`), no build step. It deploys to GitHub Pages from `main` through `.github/workflows/deploy.yml`.

## How it works

- **Design:** a dark product page at Linear/Vercel/Apple craft, built through the Impeccable workflow. `PRODUCT.md` holds the product facts, `DESIGN.md` the design system, and `.impeccable/surfaces/` the direction contract.
- **The sky:** a WebGL Dhaka skyline (layered, with water tanks and a minaret) under smog whose density comes from the live PM2.5 reading. The pointer thins the smog, and clicking the sky fires a purifier pulse. An airship flies the Cedar Initiative livery; you can drag and throw it.
- **Live data:** [Open-Meteo](https://open-meteo.com) air-quality and weather APIs, refreshed every 10 minutes. It feeds the readings bar, the data panel, the breath counter, the pinned 48-hour scrub (the sky follows each hour), the forecast chart and the example alert.
- **Controls:** the Cmd/Ctrl+K command menu, opt-in city sound tied to wind speed, and a Pause button that stops all motion. `prefers-reduced-motion` starts the page paused.

## Editing

Copy lives in plain HTML in `index.html`. Update the 2027 plan once dates and venue are confirmed, and keep `PRODUCT.md` in step.
