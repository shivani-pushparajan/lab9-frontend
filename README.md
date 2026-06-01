# SpeedScore — Lab 9 Frontend Starter

This repository contains the SpeedScore frontend (React) at the end of Chapter 16 of
*Full Stack Web Development from the Ground Up*. It is the starting point for **Lab 9: Deployment**.

## What's In Here

- A React app (`src/`) with user authentication UI, rounds mode, and courses mode
- Static assets in `public/` (HTML entry point, icons, manifest)
- Playwright end-to-end tests in `tests/`
- `package.json` with `start`, `build`, `test`, and `eject` scripts

## Getting Started Locally

```bash
npm install
```

Create a `.env` file at the repo root:

```
REACT_APP_GOOGLE_PLACES_API_KEY=your_key_here
```

Start the dev server:

```bash
npm start
```

The app is available at `http://localhost:3000`.

## Building for Production

```bash
npm run build
```

This creates an optimized production build in `build/`. Serve the contents of `build/`
from your hosting platform.

## Known Deployment Gotchas

- **Google Places API key** — `REACT_APP_GOOGLE_PLACES_API_KEY` must be injected as a
  build-time environment variable on your hosting platform. A local `.env` value is
  baked into the build at `npm run build` time, but most platforms require you to set
  this in their environment variable settings so it is available when the platform runs
  the build command.
- **Backend URL** — The frontend calls the SpeedScore backend API. In development it
  defaults to `http://localhost:3000`. When deploying, you will need to configure the
  API base URL to point at your deployed backend.