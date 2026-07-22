---
name: Market-aware daily scan with Massive (Polygon.io)
description: Check market status/holidays, then pull grouped daily bars and top movers only when markets traded.
api: openapi/polygon-openapi-original.json
operations: [GetMarketStatus, GetMarketHolidays, GetGroupedStocksAggregates, GetStocksSnapshotDirection]
generated: '2026-07-22'
method: generated
---

# Market-aware daily scan

Authenticate with `?apiKey=YOUR_KEY`. Gate any market-wide pull on the calendar first.

1. **Check status.** Call `GetMarketStatus` (`/v1/marketstatus/now`); if the market is closed,
   call `GetMarketHolidays` (`/v1/marketstatus/upcoming`) to pick the last completed session date.
2. **Whole-market daily bars.** Call `GetGroupedStocksAggregates`
   (`/v2/aggs/grouped/locale/us/market/stocks/{date}`) with the chosen session date and
   `adjusted=true` — one OHLCV row per traded ticker.
3. **Top movers.** Call `GetStocksSnapshotDirection`
   (`/v2/snapshot/locale/us/markets/stocks/{direction}`) with `gainers` or `losers`.

Rules: never request grouped bars for a weekend/holiday date (empty results); everything is GET
and safe to retry; on `{"status":"ERROR"}` inspect `error` and keep `request_id`; respect the
free-tier 5 req/min ceiling.
