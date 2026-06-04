# NASDAQ100 vs S&P500

This repository contains a GitHub Pages visualization and supporting data for comparing historical NASDAQ-100 and S&P 500 returns by quarterly start month.

## GitHub Pages content

- `docs/index.html` - Interactive visualization for lump-sum and monthly investing comparisons.
- `docs/llms.txt` - Reading guide for ChatGPT, other LLMs, and automated clients.
- `docs/api/README.md` - Static API usage notes.
- `docs/api/metadata.json` - Dataset metadata, field definitions, caveats, and endpoint list.
- `docs/api/summary.json` - Compact machine-readable project summary.
- `docs/api/source-notes.json` - Source coverage and limitations for total-return data.
- `docs/api/comparison-data.json` - Chart-ready comparison rows grouped by return type, investment mode, and holding period.

## Supporting data

- `data_tr/NASDAQ100_TR_monthly_official_XNDX.csv` - NASDAQ-100 Total Return monthly data from Nasdaq XNDX public endpoints.
- `data_tr/SP500_TR_monthly_yahoo_SP500TR.csv` - S&P 500 Total Return monthly data from Yahoo Finance `^SP500TR` chart data.
- `data_tr/source_notes.md` - Human-readable acquisition notes and limitations.
- `data_tr/fetch_summary.json` - Machine-readable acquisition summary.

## Purpose

Use this repository to compare historical NASDAQ-100 and S&P 500 performance across multiple start months, investment methods, return types, and holding periods.

The visualization currently covers:

- Lump-sum investing and monthly investing.
- Price return and total return views.
- 10, 15, 20, and 25 year holding periods.
- Quarterly start months.

## Machine-readable access

When the site is published from the `docs/` directory with GitHub Pages, clients can read these static endpoints directly:

- `/llms.txt`
- `/api/README.md`
- `/api/metadata.json`
- `/api/summary.json`
- `/api/source-notes.json`
- `/api/comparison-data.json`

These files are intended to make the project easier for ChatGPT, search engines, scripts, and static API clients to understand without needing to extract data from JavaScript-rendered charts.

## Notes and caveats

- Historical comparison only; this is not investment advice.
- Price return excludes dividends.
- Total return includes dividends where total-return index data is available.
- Taxes, fees, foreign exchange effects, and transaction costs are not included.
- Total-return source coverage differs between NASDAQ-100 and S&P 500. Read `docs/api/source-notes.json` and `data_tr/source_notes.md` before interpreting total-return results.
