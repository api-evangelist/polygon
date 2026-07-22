---
name: Research a stock with Massive (Polygon.io)
description: Resolve a ticker, pull its profile, recent news, and price history, and read the current snapshot.
api: openapi/polygon-openapi-original.json
operations: [ListTickers, GetTicker, ListNews, GetStocksAggregates, GetPreviousStocksAggregates, GetStocksSnapshotTicker]
generated: '2026-07-22'
method: generated
---

# Research a stock

Authenticate every call with `?apiKey=YOUR_KEY` (or `Authorization: Bearer YOUR_KEY`). All
operations are GET and idempotent — retries are always safe.

1. **Resolve the symbol.** Call `ListTickers` (`/v3/reference/tickers`) with `search=<company name>`
   and `market=stocks&active=true`. Page with `limit`, follow `next_url` for more.
2. **Get the profile.** Call `GetTicker` (`/v3/reference/tickers/{ticker}`) for name, market,
   locale, primary exchange, and identifiers (FIGI, CIK).
3. **Pull recent news.** Call `ListNews` (`/v2/reference/news`) with `ticker=<T>`; each article
   lists all related `tickers[]`.
4. **Price history.** Call `GetStocksAggregates`
   (`/v2/aggs/ticker/{stocksTicker}/range/{multiplier}/{timespan}/{from}/{to}`) — e.g.
   `1/day/2026-01-01/2026-07-22`, `adjusted=true`. For just yesterday use
   `GetPreviousStocksAggregates` (`/v2/aggs/ticker/{stocksTicker}/prev`).
5. **Current state.** Call `GetStocksSnapshotTicker`
   (`/v2/snapshot/locale/us/markets/stocks/tickers/{stocksTicker}`) for the day bar, last trade,
   and last quote in one shot.

Rules: on `{"status":"ERROR"}` read `error` and keep `request_id` for support; on 429 back off one
minute (free tier is 5 req/min); paginate only via the returned `next_url` (append your API key).
