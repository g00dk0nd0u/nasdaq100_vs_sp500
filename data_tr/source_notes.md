# Total Return Data Acquisition Notes

Generated: 2026-06-02T22:59:22.955021+00:00

## Files created

- `nasdaq_xndx_total_return_raw_official.xlsx`
- `nasdaq_xndx_total_return_raw_official_historydata.json`
- `NASDAQ100_TR_monthly_official_XNDX.csv`
- `sp500_total_return_raw_yahoo_SP500TR.json`
- `SP500_TR_monthly_yahoo_SP500TR.csv`
- `fetch_summary.json`

## NASDAQ-100 Total Return

Source tried: Nasdaq Global Index Watch official `XNDX` endpoints.

- Export endpoint: `https://indexes.nasdaqomx.com/Index/ExportHistory/XNDX?startDate=1985-01-01&endDate=2026-05-31&timeOfDay=EOD`
- HistoryData endpoint: `https://indexes.nasdaqomx.com/Index/HistoryData` with `id=XNDX`
- Result: success.
- Returned daily rows: 6853
- Monthly rows after taking the last available trading day in each month: 327
- Coverage: 1999-03 through 2026-05

Important limitation: the request asked for 1985-01-01 onward, but the public XNDX endpoint returned data starting at 1999-03. This does not preserve the current 1985 start date.

## S&P 500 Total Return

Source tried: S&P DJI public site, then Yahoo Finance chart API for `^SP500TR` as a reachable secondary distribution.

- Yahoo endpoint: `https://query1.finance.yahoo.com/v8/finance/chart/%5ESP500TR?period1=0&period2=1780617600&interval=1mo&events=history&includeAdjustedClose=true`
- Result: success.
- Monthly rows after de-duplicating by calendar month: 462
- Coverage: 1988-01 through 2026-06

Important limitation: this is not a direct S&P DJI raw download. It should be treated as a candidate/fallback source until an official S&P DJI historical export or licensed data source is selected. The latest calendar month may be partial and should be excluded for month-end-only analysis.

## Recommendation before recalculation

Do not update `docs/index.html` from these files yet. First decide whether the comparison period should be shortened to the common total-return coverage period, or whether an official/licensed source with longer XNDX history is required.
