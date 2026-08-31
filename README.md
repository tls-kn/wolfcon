# Recent Earthquakes

A zero-build static web app that fetches the USGS "all earthquakes, past day" GeoJSON feed and lists recent events.

## Run locally

From this directory, start any static web server, for example:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Features

- Live USGS past-day GeoJSON feed
- Search by location
- Minimum-magnitude filter
- Localized date/time and relative age
- Depth and tsunami flag
- Responsive layout and automatic dark mode
- No framework, build step, or backend
