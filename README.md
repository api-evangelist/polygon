# Polygon (polygon)

Polygon (Polygon.io, rebranded as Massive in early 2026) provides real-time and historical market data APIs across US stocks, options, indices, forex, cryptocurrencies, and futures. Coverage is delivered through REST endpoints and WebSocket streams under a single api.polygon.io surface plus an S3 flat files product, with tiered subscription plans for retail developers and Business contracts for redistribution and exchange-licensed data.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/polygon/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/polygon/refs/heads/main/apis.yml)

## Tags

- Finance
- Fintech
- Market Data
- Stocks
- Options
- Forex
- Crypto
- Indices
- Futures
- WebSockets
- Real-time
- Historical
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### Polygon Stocks API

Real-time and historical US equity market data including aggregate (OHLC) bars at minute/hour/day granularity, trades, NBBO quotes, snapshots, ticker reference, splits, dividends, and financials. Available via REST and the stocks WebSocket cluster.

- **Human URL:** [https://polygon.io/docs/stocks](https://polygon.io/docs/stocks)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Stocks
- Equities
- Market Data
- Real-time

#### Properties

- [Documentation](https://polygon.io/docs/stocks)
- [API Reference](https://polygon.io/docs/stocks)
- [OpenAPI](openapi/polygon-stocks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-stocks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-stocks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://polygon.io/docs/getting-started)
- [JSON Schema](json-schema/polygon-aggregate-bar-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/polygon-aggregate-bar-structure.json)
- [Example](examples/polygon-stocks-aggregate-bars-example.json)

### Polygon Options API

OPRA-licensed options market data via REST and WebSocket: aggregates, trades, quotes, snapshots, contract reference, and option chains. Greeks and implied volatility are available on paid tiers.

- **Human URL:** [https://polygon.io/docs/options](https://polygon.io/docs/options)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Options
- OPRA
- Market Data

#### Properties

- [Documentation](https://polygon.io/docs/options)
- [API Reference](https://polygon.io/docs/options)
- [OpenAPI](openapi/polygon-options-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-options.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-options.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/polygon-options-contract-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/polygon-options-contract-structure.json)
- [Example](examples/polygon-options-chain-snapshot-example.json)

### Polygon Indices API

Real-time and historical index values for major US and global indices via REST and WebSocket. Includes aggregates, snapshots, and index reference data.

- **Human URL:** [https://polygon.io/docs/indices](https://polygon.io/docs/indices)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Indices
- Market Data

#### Properties

- [Documentation](https://polygon.io/docs/indices)
- [API Reference](https://polygon.io/docs/indices)
- [OpenAPI](openapi/polygon-indices-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-indices.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-indices.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Polygon Forex API

Real-time and historical FX prices for 1,000+ currency pairs via REST and WebSocket. Covers aggregates, quotes, snapshots, conversions, and previous-close.

- **Human URL:** [https://polygon.io/docs/forex](https://polygon.io/docs/forex)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Forex
- FX
- Currencies
- Market Data

#### Properties

- [Documentation](https://polygon.io/docs/forex)
- [API Reference](https://polygon.io/docs/forex)
- [OpenAPI](openapi/polygon-forex-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-forex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-forex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/polygon-forex-conversion-example.json)

### Polygon Crypto API

Aggregates, trades, snapshots, and level-2 order books for crypto pairs sourced across major exchanges, plus WebSocket streaming on the crypto cluster.

- **Human URL:** [https://polygon.io/docs/crypto](https://polygon.io/docs/crypto)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Crypto
- Cryptocurrency
- Market Data

#### Properties

- [Documentation](https://polygon.io/docs/crypto)
- [API Reference](https://polygon.io/docs/crypto)
- [OpenAPI](openapi/polygon-crypto-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-crypto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-crypto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Polygon Reference API

Reference data covering tickers, ticker types, markets, exchanges, market holidays, market status, conditions, stock splits, dividends, and ticker news. Shared across all asset classes.

- **Human URL:** [https://polygon.io/docs/stocks/get_v3_reference_tickers](https://polygon.io/docs/stocks/get_v3_reference_tickers)
- **Base URL:** `https://api.polygon.io`

#### Tags

- Reference
- Tickers
- Exchanges
- Calendars

#### Properties

- [Documentation](https://polygon.io/docs/stocks/get_v3_reference_tickers)
- [OpenAPI](openapi/polygon-reference-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/polygon-reference.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-reference.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/polygon-ticker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/polygon-ticker-structure.json)
- [Example](examples/polygon-reference-tickers-example.json)

### Polygon WebSocket API

Real-time streaming WebSocket clusters per asset class (stocks/options/indices/forex/crypto). Subscribers authenticate with an API key and subscribe to channels for trades, quotes, aggregates, and book updates.

- **Human URL:** [https://polygon.io/docs/stocks/ws_getting-started](https://polygon.io/docs/stocks/ws_getting-started)
- **Base URL:** `wss://socket.polygon.io`

#### Tags

- WebSocket
- Streaming
- Real-time

#### Properties

- [Documentation](https://polygon.io/docs/stocks/ws_getting-started)
- [AsyncAPI](asyncapi/polygon-websocket-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/polygon-trade-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/polygon-quote-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/polygon-websocket-subscribe-example.json)
- [Postman Collection](collections/polygon-crypto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-crypto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/polygon-forex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-forex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/polygon-indices.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-indices.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/polygon-options.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-options.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/polygon-reference.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-reference.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/polygon-stocks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/polygon-stocks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://polygon.io/)
- [Documentation](https://polygon.io/docs)
- [API Reference](https://polygon.io/docs)
- [Getting Started](https://polygon.io/docs/getting-started)
- [Sign Up](https://polygon.io/dashboard/signup)
- [Login](https://polygon.io/dashboard/login)
- [Pricing](https://polygon.io/pricing)
- [Status Page](https://status.polygon.io/)
- [Blog](https://polygon.io/blog)
- [Support](https://polygon.io/contact)
- [Terms of Service](https://polygon.io/terms)
- [Privacy Policy](https://polygon.io/privacy)
- [GitHub Organization](https://github.com/polygon-io)
- [Tools](https://github.com/polygon-io/mcp_polygon)
- [SDK](https://github.com/polygon-io/client-php)
- [SDK](https://pypi.org/project/polygon-api-client/)
- [SDK](https://www.npmjs.com/package/@polygon.io/client-js)
- [SDK](https://central.sonatype.com/artifact/io.polygon.kotlin.sdk/polygon-kotlin-sdk-jvm)
- [SDK](https://pkg.go.dev/github.com/polygon-io/client-go)
- [LinkedIn](https://www.linkedin.com/company/polygon-io)
- [Plans](plans/polygon-plans-pricing.yml)
- [Rate Limits](rate-limits/polygon-rate-limits.yml)
- [Fin Ops](finops/polygon-finops.yml)
- [Spectral Rules](rules/polygon-rules.yml)
- [Vocabulary](vocabulary/polygon-vocabulary.yml)
- [JSON-LD](json-ld/polygon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
