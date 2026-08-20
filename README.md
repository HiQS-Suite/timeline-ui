# timeline-ui

<img width="4446" height="1930" alt="CleanShot 2026-08-19 at 21 13 01@2x" src="https://github.com/user-attachments/assets/00678f83-68a8-4e0d-a22f-41022602750b" />

**codename: helix-core "timeline-ui" · planning ledgers** — a single-file, dependency-free HTML timeline for browsing releases, issues, and labels along a horizontally scrollable rail.

> **Requires a local web server.** `ledger.html` loads its data via `fetch('./data.json')`, which browsers block on a plain `file://` page. Double-clicking the file will not work — see Usage below. If you need something that opens directly with no server, use [`ledger-static-preview.html`](ledger-static-preview.html) instead.

## Files

- [`ledger.html`](ledger.html) — the current viewer. Renders entirely from [`data.json`](data.json) at load time — no build step, but it does need to be served over HTTP (see Usage).
- [`data.json`](data.json) — all card and telemetry data: header/sync banner, stats bar, "just finished" / "what's next" strip, and the full release timeline (detours, roadmap items, marathons). Edit this file to point the viewer at your own data; the shape is documented inline by example.
- [`ledger-static-preview.html`](ledger-static-preview.html) — a frozen, self-contained snapshot of the original `ledger.html` with its data baked into the markup. Opens directly from disk (no server needed) but does not read `data.json`, so it won't reflect edits made there.
- [`ledger-v1-panels.html`](ledger-v1-panels.html) — earlier panel-based layout, kept for reference.
- [`Planning Ledgers.dc.html`](Planning%20Ledgers.dc.html) — the source artboard for the design, authored in the `.dc.html` (Claude Design canvas) format.
- [`support.js`](support.js) — generated runtime required by the `.dc.html` artboard (`dc-runtime`). Do not edit directly.

## Usage

`ledger.html` fetches `data.json` via `fetch()`, so it must be served over HTTP — opening it directly as a `file://` URL will fail in most browsers due to CORS. From this directory:

```
python3 -m http.server 8080
```

then open `http://localhost:8080/ledger.html`. Use the search box to filter by issue, title, or label, and the ‹ › controls to page between older/newer releases.

## License

Dual-licensed. The [AGPL-3.0](LICENSE) applies by default and covers internal use, self-hosting, and redistribution with source. See [LICENSE-COMMERCIAL.md](LICENSE-COMMERCIAL.md) for terms covering proprietary embedding or hosting a modified version without publishing source.

© Copyright 2026 Neochrome, Inc.
