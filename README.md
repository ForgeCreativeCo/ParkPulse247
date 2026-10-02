# Park Pulse: WDW Edition

A pixel-art, 24/7-style newscast covering Walt Disney World — built as a single self-contained `index.html`.

## What's in it

- Three hand-drawn pixel-art scenes (anchor desk, field report, data board) rendered on `<canvas>` and cross-faded on a timer
- Real headlines, live-snapshot ride wait times, and current weather, baked in as data at build time
- A scrolling wait-time/weather ticker
- Browser text-to-speech (Web Speech API) so the two anchors actually read headlines aloud and react to each other, synced to mouth animation
- Retro synthesized sound effects (Web Audio) for segment transitions

## Running it

It's one static HTML file with no build step and no dependencies to install — open `index.html` directly in a browser, or serve the folder with anything static (`npx serve`, GitHub Pages, etc.).

## Keeping it current

This file is a **snapshot**, not a live feed — the page itself can't poll outside websites on its own. The data (`NOW_CAPTURED`, `WAITS`, `WEATHER`, `HEADLINES` near the top of the `<script>` block) gets refreshed and republished to the [Claude artifact version](https://claude.ai/artifact/8hyiQKbEd1urLH2qoNNTDX) of this page roughly every hour by a scheduled Claude task. That scheduled refresh does **not** currently push back to this repo — pull the latest data block from the artifact (or ask Claude) if you want this copy back in sync.

## Credits

Headlines sourced from Disney Parks Blog, WDW News Today, and AllEars. Wait times from [queue-times.com](https://queue-times.com). Weather from AccuWeather. Built with Claude.
