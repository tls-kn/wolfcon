# AGENTS.md

## Project Overview

Zero-build static web app displaying recent worldwide earthquakes from the USGS GeoJSON feed (`all_day.geojson`). Single-file app (`index.html`) — vanilla HTML/CSS/JS, no framework, no dependencies, no build step.

## Key Files

- `index.html` — All application code (HTML, CSS, JS) in one file
- `README.md` — Project documentation

## Commands

- **Serve locally:** `python3 -m http.server 8000`
- There are no build, test, lint, or format commands.
- **Deploy:** push to `main` — GitHub Pages auto-publishes to `https://tls-kn.github.io/wolfcon/`.

## Filtering

- Search (by place), minimum-magnitude select, and a tsunami filter button.
- The tsunami button cycles through three states: `off` (no filter), `flagged` (`tsunami > 0`), and `alert` (`tsunami === 1`). State is tracked in `tsunamiFilter` with labels in `TSUNAMI_LABELS`.

## Data Source

USGS Earthquake Hazards Program — `https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_day.geojson`

## Conventions

- No package manager or build tooling — keep it that way.
- All code lives in `index.html`. Maintain the single-file structure.
- CSS uses custom properties and `prefers-color-scheme` for dark mode.
- System font stack for typography.
- No external dependencies.

## Things to Watch For

- Breaking the single-file architecture (don't introduce build tools or split files).
- Introducing dependencies — the app is intentionally dependency-free.
- Changes to the USGS API contract that could break feed parsing.
