# Static API for NASDAQ-100 vs S&P 500

This directory contains machine-readable files for the GitHub Pages visualization.

## Endpoints

When the repository is published with GitHub Pages from the `docs/` directory, these files are available under the site root:

- `/api/metadata.json` - Dataset metadata, field definitions, caveats, and endpoint list.
- `/api/summary.json` - Short project summary and recommended reading order.
- `/api/source-notes.json` - Source coverage and limitations for total-return data.
- `/api/comparison-data.json` - Chart-ready comparison rows grouped by return type, investment mode, and holding period.

## Recommended reading order

1. Read `/api/summary.json` for the purpose of the project.
2. Read `/api/metadata.json` for field definitions and caveats.
3. Read `/api/source-notes.json` before using total-return data.
4. Read `/api/comparison-data.json` for chart-ready comparison rows.
5. Read the interactive page `/` for charts and visual comparisons.

## Important caveats

- This is a historical comparison, not investment advice.
- Price return excludes dividends.
- Total return includes dividends where total-return index data is available.
- Taxes, fees, foreign exchange effects, and transaction costs are excluded.
- Total-return coverage differs by data source.
