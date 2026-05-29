# Polygon (polygon)

Polygon (Polygon.io, rebranded as Massive in early 2026) provides real-time and historical market data APIs across US stocks, options, indices, forex, cryptocurrencies, and futures. Coverage is delivered through REST endpoints and WebSocket streams under a single api.polygon.io surface plus an S3 flat files product, with tiered subscription plans for retail developers and Business contracts for redistribution and exchange-licensed data.

**APIs.yml:** [apis.yml](apis.yml)

## Type
- **x-type:** company
- **x-tier:** 2 (pipeline-enriched)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Finance

## Tags
Finance, Fintech, Market Data, Stocks, Options, Forex, Crypto, Indices, Futures, WebSockets, Real-time, Historical, Public APIs

## APIs (`https://api.polygon.io` / `wss://socket.polygon.io`)
- **Polygon Stocks API** — [Documentation](https://polygon.io/docs/stocks)
  - OpenAPI: [openapi/polygon-stocks-openapi.yml](openapi/polygon-stocks-openapi.yml)
  - JSON Schema: [json-schema/polygon-aggregate-bar-schema.json](json-schema/polygon-aggregate-bar-schema.json)
  - Example: [examples/polygon-stocks-aggregate-bars-example.json](examples/polygon-stocks-aggregate-bars-example.json)
  - Naftiko Capabilities: [stocks-aggregates](capabilities/stocks-aggregates.yaml), [stocks-dailybars](capabilities/stocks-dailybars.yaml)
- **Polygon Options API** — [Documentation](https://polygon.io/docs/options)
  - OpenAPI: [openapi/polygon-options-openapi.yml](openapi/polygon-options-openapi.yml)
  - JSON Schema: [json-schema/polygon-options-contract-schema.json](json-schema/polygon-options-contract-schema.json)
  - Example: [examples/polygon-options-chain-snapshot-example.json](examples/polygon-options-chain-snapshot-example.json)
  - Naftiko Capabilities: [options-aggregates](capabilities/options-aggregates.yaml), [options-contracts](capabilities/options-contracts.yaml), [options-snapshots](capabilities/options-snapshots.yaml)
- **Polygon Indices API** — [Documentation](https://polygon.io/docs/indices)
  - OpenAPI: [openapi/polygon-indices-openapi.yml](openapi/polygon-indices-openapi.yml)
  - Naftiko Capabilities: [indices-aggregates](capabilities/indices-aggregates.yaml), [indices-snapshots](capabilities/indices-snapshots.yaml)
- **Polygon Forex API** — [Documentation](https://polygon.io/docs/forex)
  - OpenAPI: [openapi/polygon-forex-openapi.yml](openapi/polygon-forex-openapi.yml)
  - Example: [examples/polygon-forex-conversion-example.json](examples/polygon-forex-conversion-example.json)
  - Naftiko Capabilities: [forex-aggregates](capabilities/forex-aggregates.yaml), [forex-conversion](capabilities/forex-conversion.yaml), [forex-quotes](capabilities/forex-quotes.yaml)
- **Polygon Crypto API** — [Documentation](https://polygon.io/docs/crypto)
  - OpenAPI: [openapi/polygon-crypto-openapi.yml](openapi/polygon-crypto-openapi.yml)
  - Naftiko Capabilities: [crypto-aggregates](capabilities/crypto-aggregates.yaml), [crypto-dailybars](capabilities/crypto-dailybars.yaml), [crypto-snapshots](capabilities/crypto-snapshots.yaml), [crypto-books](capabilities/crypto-books.yaml)
- **Polygon Reference API** — [Documentation](https://polygon.io/docs/stocks/get_v3_reference_tickers)
  - OpenAPI: [openapi/polygon-reference-openapi.yml](openapi/polygon-reference-openapi.yml)
  - JSON Schema: [json-schema/polygon-ticker-schema.json](json-schema/polygon-ticker-schema.json)
  - Example: [examples/polygon-reference-tickers-example.json](examples/polygon-reference-tickers-example.json)
  - Naftiko Capabilities: [reference-tickers](capabilities/reference-tickers.yaml), [reference-markets](capabilities/reference-markets.yaml), [reference-corporateactions](capabilities/reference-corporateactions.yaml), [reference-news](capabilities/reference-news.yaml)
- **Polygon WebSocket API** — [Documentation](https://polygon.io/docs/stocks/ws_getting-started)
  - AsyncAPI: [asyncapi/polygon-websocket-asyncapi.yml](asyncapi/polygon-websocket-asyncapi.yml)
  - JSON Schemas: [trade](json-schema/polygon-trade-schema.json), [quote](json-schema/polygon-quote-schema.json)
  - Example: [examples/polygon-websocket-subscribe-example.json](examples/polygon-websocket-subscribe-example.json)

## Cross-cutting Workflow Capability
- [market-data-research.yaml](capabilities/market-data-research.yaml) — cross-asset research composition (tickers + stocks aggregates + indices snapshot)

## Common Properties
- [Portal](https://polygon.io/)
- [Documentation](https://polygon.io/docs)
- [Pricing](https://polygon.io/pricing)
- [Status](https://status.polygon.io/)
- [Blog](https://polygon.io/blog)
- [GitHub org](https://github.com/polygon-io)
- [Official MCP Server (mcp_polygon → mcp_massive)](https://github.com/polygon-io/mcp_polygon)
- SDKs: [PHP](https://github.com/polygon-io/client-php) (official), [Python](https://pypi.org/project/polygon-api-client/), [JavaScript/TypeScript](https://www.npmjs.com/package/@polygon.io/client-js), [Kotlin/JVM](https://central.sonatype.com/artifact/io.polygon.kotlin.sdk/polygon-kotlin-sdk-jvm), [Go](https://pkg.go.dev/github.com/polygon-io/client-go)
- [Plans](plans/polygon-plans-pricing.yml)
- [RateLimits](rate-limits/polygon-rate-limits.yml)
- [FinOps](finops/polygon-finops.yml) — FOCUS-aligned
- [Spectral Rules](rules/polygon-rules.yml)
- [Vocabulary](vocabulary/polygon-vocabulary.yml)
- [JSON-LD Context](json-ld/polygon-context.jsonld)

## Artifact Counts
| Artifact | Count |
|---|---|
| OpenAPI specs | 6 |
| AsyncAPI specs | 1 |
| JSON Schema | 5 |
| JSON Structure | 3 |
| JSON-LD contexts | 1 |
| Examples | 5 |
| Spectral rulesets | 1 |
| Naftiko capabilities | 19 (18 per-tag + 1 workflow) |
| Vocabulary | 1 |
| Plans / Rate Limits / FinOps | 1 each |

## Notes on the Polygon → Massive Rebrand
Polygon.io rebranded to Massive in early 2026. The `polygon.io` domain, the
`api.polygon.io` REST host, and the `socket.polygon.io` WebSocket clusters
all remain operational at the time of this profile. Pricing and marketing
pages may redirect to `massive.com`. The official MCP server was renamed
from `mcp_polygon` to `mcp_massive` on the polygon-io GitHub org.

## Timestamps
- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## Maintainers
- **Kin Lane** — kin@apievangelist.com
