# QNH Lookup — Installable PWA

## Files
- `index.html` — the original QNH calculator with PWA metadata and service-worker registration added.
- `manifest.json` — app name, display mode, colors and icon declarations.
- `service-worker.js` — caches the app shell for offline use.
- `icons/` — 192px and 512px app icons.

## Hosting and installation
A PWA must be served from **HTTPS** (or `localhost` for development). Do not open `index.html` directly with `file://` if you want installation and offline caching.

1. Upload the contents of this folder to an HTTPS web host, keeping the folder structure unchanged.
2. Open the hosted address in Chrome or Edge on Windows, or Chrome on Android.
3. Use the browser's **Install app** option (or **Add to Home screen** on Android).
4. Open the app once while online so the service worker can cache the files. It should then load offline.

## iPhone
The PWA can be added using Safari's Share → Add to Home Screen. The service worker also provides offline caching after the first successful online load.

## Updating
When you publish a changed version, change `qnh-lookup-v1` in `service-worker.js` to a new cache version (for example `qnh-lookup-v2`) so installed copies refresh their cached files.

The QNH lookup table and lookup logic from the supplied calculator have been retained.
