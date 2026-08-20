# timeline-ui

**helix-core · planning ledgers** — a single-file, dependency-free HTML timeline for browsing releases, issues, and labels along a horizontally scrollable rail.

## Files

- [`ledger.html`](ledger.html) — the current standalone viewer. Open it directly in a browser; no build step or server required.
- [`ledger-v1-panels.html`](ledger-v1-panels.html) — earlier panel-based layout, kept for reference.
- [`Planning Ledgers.dc.html`](Planning%20Ledgers.dc.html) — the source artboard for the design, authored in the `.dc.html` (Claude Design canvas) format.
- [`support.js`](support.js) — generated runtime required by the `.dc.html` artboard (`dc-runtime`). Do not edit directly.

## Usage

Open [`ledger.html`](ledger.html) in any modern browser. Use the search box to filter by issue, title, or label, and the ‹ › controls to page between older/newer releases.

## License

Dual-licensed. The [AGPL-3.0](LICENSE) applies by default and covers internal use, self-hosting, and redistribution with source. See [LICENSE-COMMERCIAL.md](LICENSE-COMMERCIAL.md) for terms covering proprietary embedding or hosting a modified version without publishing source.

© Copyright 2026 Neochrome, Inc.
