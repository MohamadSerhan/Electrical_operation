Electrical Operations PWA — iPhone / iPad

IMPORTANT: A PWA cannot be installed by opening index.html directly from the iPhone Files app. It must be served over HTTPS (or localhost during development).

Deploy the complete contents of this folder to the same HTTPS server that serves Electrical Operations. Keep index.html, manifest.webmanifest, service-worker.js and the icons folder together.

iPhone installation:
1. Open the HTTPS site in Safari.
2. Tap Share.
3. Tap Add to Home Screen.
4. Confirm Add.

Design notes:
- Original Betta V1 application logic is retained.
- CSP worker-src was changed from none to self/blob so the service worker can run.
- API requests are never cached by the service worker.
- Navigation uses network-first with an offline app-shell fallback.
