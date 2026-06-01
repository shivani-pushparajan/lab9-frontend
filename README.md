# SpeedScore --- Lab 9 Frontend Starter

This repository contains the SpeedScore frontend (React) at the end of Chapter 16 of *Full Stack Web Development from the Ground Up*. It is the starting point for **Lab 9: Deployment**.

## What's In Here

- A React app (`src/`) with user authentication UI, rounds mode, and courses mode
- Static assets in `public/` (HTML entry point, icons, manifest)
- Playwright end-to-end tests in `tests/`
- `package.json` with `start`, `build`, `test`, and `eject` scripts

## Getting Started Locally

```bash
npm install
```n
Create a `.env` file at the repo root:

```env
REACT_APP_GOOGLE_PLACES_API_KEY=your_key_here
```n
Start the dev server:

```bash
npm start
```n
The app is available at `http://localhost:3000`.

## Building for Production

```bash
npm run build
```n
This creates an optimized production build in `build/`. Serve the contents of `build/` from your hosting platform.

## Known Deployment Gotchas

- **Google Places API key** --- `REACT_APP_GOOGLE_PLACES_API_KEY` must be set as a build-time environment variable on your hosting platform. Most platforms require you to configure this in their environment settings so it is available when they run `npm run build`.
- **Backend URL** --- The frontend calls the SpeedScore backend API. In development it defaults to `http://localhost:3000`. When deploying, configure the API base URL to point at your deployed backend.
