---
name: Analyze an options chain with Massive (Polygon.io)
description: Discover contracts on an underlying, inspect one contract, and pull its aggregates and snapshot.
api: openapi/polygon-openapi-original.json
operations: [ListOptionsContracts, GetOptionsContract, GetOptionsAggregates, GetOptionsOpenClose]
generated: '2026-07-22'
method: generated
---

# Analyze an options chain

Authenticate with `?apiKey=YOUR_KEY`. Options tickers look like `O:SPY251219C00650000`.

1. **List contracts on an underlying.** Call `ListOptionsContracts`
   (`/v3/reference/options/contracts`) filtered by `underlying_ticker=<T>`; narrow with
   expiration-date and strike-price range params; page via `next_url`.
2. **Inspect a contract.** Call `GetOptionsContract`
   (`/v3/reference/options/contracts/{options_ticker}`) for strike, expiry, and exercise style.
3. **Contract price history.** Call `GetOptionsAggregates`
   (`/v2/aggs/ticker/{optionsTicker}/range/{multiplier}/{timespan}/{from}/{to}`).
4. **Daily open/close.** Call `GetOptionsOpenClose` (`/v1/open-close/{optionsTicker}/{date}`) for a
   specific session.

Rules: Greeks/IV in snapshot endpoints require paid tiers — expect missing fields on Basic keys;
all calls are GET/idempotent; on 429 back off (free tier 5 req/min); follow `next_url` cursors
verbatim with your API key appended.
