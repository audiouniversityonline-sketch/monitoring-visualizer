# Monitoring Concepts Visualizer

Nine interactive demos for [Audio University](https://www.youtube.com/@AudioUniversity) members on speaker placement and room acoustics: aiming, front-wall distance (SBIR), room modes, the 38% guideline, reflections and comb filtering, the quarter-wavelength rule, absorption by material, room decay, and bass traps. Built as the on-camera visual aid for the Monitoring Upgrades tier list video, then published here for members.

Single HTML file, no build step. Everything is drawn in the browser on canvas. It loads nothing from other sites.

## Files

- `index.html` is the whole app.
- `fonts/` holds Jost 400 and 800 (SIL Open Font License, see `fonts/OFL-Jost.txt`). The CSS lists Futura PT first, so the page shows Futura PT only on a computer where it is installed. Futura PT is never served from this repo.
- `circle-embed-snippet.html` is the block to paste into the Circle page.

## Hosting

Served by GitHub Pages from `main`. A commit to `main` deploys within about a minute.

Base URL: `https://audiouniversityonline-sketch.github.io/monitoring-visualizer/`

Embedded in an iframe on a members-only Circle page. The page itself is public to anyone with the URL. The paywall is the Circle access group on the page that embeds it, the same as the Troubleshooting Lab and Ear Training Lab.

## Circle embed

Same pattern as the Troubleshooting Lab page. The Custom HTML block wraps the iframe in a div that breaks out of Circle's content column to the full browser width (`left:50%; width:100vw; margin-left:-50vw`), and the iframe is `88vh` tall so Circle's header stays visible. The visualizer fills whatever height it is given (the same layout used on camera), so every demo fits on one screen. Below 900 px wide the demos stack and scroll inside the frame.

Fullscreen (F key) works inside the iframe because the embed sets `allow="fullscreen"`.

## Updating

Edit `index.html`, push to `main`, then bump `?v=N` in the iframe `src` on the Circle page so members load the new version instead of a cached copy.

## Keyboard

Number keys 1 to 9 jump between demos. F toggles fullscreen. P hides the demo menu.
