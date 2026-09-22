# PronoteXPr — PRONOTE Exporter

PronoteXPr is the original PronoteXP export interface, extracted into its own static repository.

It keeps the original PronoteXP visual identity and export workflow while delegating every PRONOTE operation to **PronoteXP-api**.

## Responsibilities

- QR Code login input and client-side QR decoding
- Token / URL login input
- Credentials / ENT login input
- Category selection
- JSON export
- XLSX / ODS workbook generation in the browser
- Split category exports
- Original tutorial and visual design

It intentionally contains **no Python backend** and **no `pronotepy` dependency**.

## API

The frontend calls the API configured in `script.js`:

```js
const RENDER_BACKEND_URL = "https://pronotexp-api.onrender.com";
```

For local development, use `window.PRONOTEXP_API_URL` before loading `script.js`, or serve the frontend from a local static server and point `RENDER_BACKEND_URL` at the local API.

## Local use

Serve the repository as static files:

```bash
python -m http.server 5500
```

Then open `http://localhost:5500`.

## Deployment

This repository is ready for GitHub Pages through the included workflow.

## Data handling

Exports are generated in the browser. PronoteXPr does not persist PRONOTE data.

## License

MIT — Copyright (c) 2026 Pyronixus.
