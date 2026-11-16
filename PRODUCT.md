# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Two audiences, weighted equally:

- **Participants:** students, developers, designers and scientists, mostly in and around Dhaka, deciding whether this hackathon is worth their time and whether they could contribute.
- **Partners and sponsors:** organisations that might fund, host, mentor, or supply data, deciding whether the event is serious and worth backing.

Both arrive with no prior knowledge of the event. Most will meet it through a shared link, often on a phone.

## Product Purpose

Air Hackathon 2027 is an open-innovation challenge on air quality in Dhaka, organised by Cedar Initiative. It exists to get people building tools that measure, forecast and reduce Dhaka's air pollution. Success for the site right now: a visitor understands what the event is and why it matters, and follows Cedar Initiative so they hear when the call for teams opens.

## Positioning

It is about one city's air, and that air is measurable right now. The site can show live, real readings for Dhaka, which a generic hackathon page cannot.

## Capabilities and Constraints

- Static site on GitHub Pages at airhackathon.com. Single `index.html`, no build step.
- Live data: Open-Meteo air-quality (Copernicus CAMS model) and weather APIs, no key. Modelled, not street-sensor data.
- Primary action: follow Cedar Initiative at https://cedar-initiative.org. No registration, form or community link exists yet.
- **Undecided:** dates, venue, format, prizes, judging, team size, eligibility, partners. The page must say these are not set rather than invent them.

## Brand Commitments

- Name: "Air Hackathon 2027". Organiser: Cedar Initiative.
- Cedar Initiative logo: `assets/cedar-initiative-logo.svg` (green mark #1a5029 with black wordmark), supplied by the user.
- **Standing direction (chosen 2026-11-16):** the category standard, played straight: a polished tech-event landing page with no cultural costume. Craft bar: Linear, Vercel and Apple product pages. Offered alternatives (a Bangla TV-broadcast world, a rickshaw-art world) were declined.
- Interactive pieces to keep: the live smog sky (WebGL), the 48-hour PM2.5 scrub, the breath counter, the airship, the command menu, city sound and the intro.
- Earlier site had a playful illustrated Dhaka scene with an airship carrying the Cedar flag; the user liked it as "an experience". The airship is a known, liked element.

## Evidence on Hand

- Live air-quality and weather readings (Open-Meteo).
- WHO Global Air Quality Guidelines 2021: PM2.5 24-hour guideline 15 µg/m³.
- Berkeley Earth rule of thumb: a day at 22 µg/m³ PM2.5 ≈ one cigarette.
- **Absent, must not be fabricated:** no past edition (2027 is the first), so no past winners, photos, attendance numbers, testimonials, partner logos or quotes.

## Product Principles

1. Show the air, don't describe it. Real, live data beats claims.
2. Never invent facts about the event. "Not set yet" is an honest answer.
3. Speak to builders and backers in the same plain voice.
4. Dhaka is the subject, not a backdrop.

## Accessibility & Inclusion

WCAG 2.2 AA. Motion must be pausable and respect reduced-motion preferences. Works on low-end phones and slow connections common in Dhaka.
