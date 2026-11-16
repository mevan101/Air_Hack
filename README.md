# Air Hackathon 2027

Website for [airhackathon.com](https://airhackathon.com): an open-innovation challenge on air quality in Dhaka, run by Cedar Initiative.

A single static page (`index.html`), no build step. It deploys to GitHub Pages from `main` through `.github/workflows/deploy.yml`.

## How it works

- **Intro:** a short "inhale" loader that opens into the city, shown once per session. Click or any key skips it.
- **The sky** is one WebGL shader behind the page: a procedural Dhaka skyline with traffic, tower beacons, a plane, and a sun or moon that the smog dims and reddens. Smog density follows the live PM2.5 reading and drifts with the live wind. The pointer clears it (and reveals stars at night), and clicking the sky fires a purifier shockwave.
- **Airship:** flies the Cedar Initiative banner. Drag and throw it; it springs back to its route.
- **Live air:** [Open-Meteo](https://open-meteo.com) air-quality and weather APIs, no key needed, refreshed every 10 minutes. There's a scrolling ticker in the header plus a full panel. Location is only requested when the visitor presses **Use My Location**.
- **Your breath:** counts the litres of air and micrograms of PM2.5 inhaled since the page opened, with a guided breathing orb and a cigarette comparison (Berkeley Earth's 22 µg/m³ ≈ 1 cigarette/day rule).
- **48 hours:** a pinned scroll section. Scrolling scrubs through the real hourly PM2.5 from yesterday into tomorrow's forecast, and the sky, sun, moon and smog change with it.
- **Command menu:** ⌘K / Ctrl K opens it (it's also the menu button on phones). Commands cover theme, motion, sound, location, copying the reading and jumping to sections.
- **Accessibility:** the sun/moon theme toggle follows the system setting by default. A Pause button stops all motion (WCAG 2.2.2), and with `prefers-reduced-motion` everything starts paused. City sound is opt-in.

## Editing

Copy for the problems and the 2027 plan sits in plain HTML in `index.html`. Change the plan steps once dates and venue are confirmed.
