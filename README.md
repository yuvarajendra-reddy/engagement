# Engagement Invite

An interactive, single-page engagement invitation built as a playful homage to the Google Chrome offline dinosaur game. Guests "boot up" a mock collaboration engine, play a short dino mini-game to reveal the event details, and land on the full invitation.

**Event:** 17 June 2026 · 10:00 AM onwards · Amita Rasa, Nandi Hills, India

## Overview

The whole thing is one self-contained `invite_dino.html` file. Open it and it plays out in three acts:

1. **Boot sequence** — a faux terminal "booting" a *Human Collaboration Engine*, themed around AI/ML and thermodynamics, ending in the engagement announcement.
2. **Dino mini-game** — the classic Chrome T-Rex runner. Tap or press space to jump. Hit the birds (each carries a question banner) to reveal the answers: *What? Who? When? Where? Directions?* and finally *You're invited*.
3. **The invitation** — a scrollable section with profiles of the couple, a compatibility report, schedule, and closing note.

## Features

- Real Chrome T-Rex sprite (extracted from the open-source Chromium `t-rex-runner` assets) recolored to match the gold theme, with running animation.
- Birds fly across dragging question banners; jump into one to pop up its answer.
- Animated terminal boot screen with progress bar and tap-to-pause.
- Responsive layout — the couple's profile cards stack cleanly on phones.
- Pixel-art canvas game with cacti, ground detail, and a hits/misses counter.

## How to run

It's just a static HTML file. Any of these work:

- **Open locally** — double-click `invite_dino.html` in any modern browser.
- **Serve it** — `python3 -m http.server` then visit `http://localhost:8000/invite_dino.html`.


## Project structure

```
.
├── invite_dino.html   # the entire invite — markup, styles, game, and embedded images
└── README.md
```

Everything (HTML, CSS, JavaScript, the dino sprite, and the couple's photos) is embedded directly in the single HTML file, so there are no asset paths to manage.

## Dependencies

None to install. The only external resource is **Google Fonts** (Playfair Display, DM Mono, DM Sans), loaded over the network. If the fonts fail to load, the page falls back to system serif / monospace / sans-serif fonts.

## Customizing

A few common edits, all inside `invite_dino.html`:

- **Boot terminal text** — edit the `bootLines` array.
- **Game questions & answers** — edit the `QUESTIONS` array (label shown on the bird's banner, plus the popup title and body).
- **Couple's details** — the profile cards live in the `#datasets` section; the schedule is in `#schedule`.
- **Theme colors** — the gold / accent palette is defined as CSS variables in the `:root` block at the top of the `<style>`.
- **Dino size** — tweak the `dw` value in the `drawDino` function.

## Browser support

Works in current versions of Chrome, Edge, Firefox, and Safari, on desktop and mobile. The game uses the HTML5 `<canvas>` and supports tap, click, and spacebar to jump.

## Credits

- Dino sprite adapted from the open-source [Chromium T-Rex Runner](https://github.com/wayou/t-rex-runner) assets.
- Fonts by Google Fonts.

---

Made with love for Madhura & Yuvarajendra. 💍
