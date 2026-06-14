# Zora GraphQL API

The Zora NFT GraphQL API provides a unified interface for querying NFT metadata, on-chain events, sales history, market data, and collection statistics across Ethereum mainnet and supported L2 networks (Zora Network, Base, Optimism). It aggregates data from multiple marketplaces including ZORA, OpenSea (Seaport), LooksRare, Foundation, and others, exposing a single query surface for the entire NFT ecosystem.

The API supports ERC-721 and ERC-1155 token standards and covers every major NFT contract deployed across supported chains. Key capabilities include token and collection metadata retrieval, mint event history, on-chain and offchain market orders, sales volume aggregation, owner analytics, text-based search, and Nouns/NounsBuilder DAO auction data.

**Endpoint:** https://api.zora.co/graphql

**Authentication:** Optional. Unauthenticated access is permitted for up to 120 requests per minute. For higher throughput, include an API key via the `X-API-KEY` request header. Keys are available at https://keys.api.zora.co/

**Networks Supported:**
- Ethereum Mainnet (Chain ID 1)
- Zora Network (Chain ID 7777777)
- Base (Chain ID 8453)
- Optimism (Chain ID 10)
- Goerli, Zora Goerli, Base Goerli, Optimism Goerli (testnets)

**Pagination:** Maximum page size of 500 for standard queries; 50 for search queries.

**Root Query Type:** `RootQuery`

**Top-Level Query Operations:**
- `aggregateStat` — floor price, NFT count, owner count, sales volume, owners by count
- `aggregateAttributes` — trait/attribute distribution across a collection
- `collections` — NFT collection metadata
- `events` — on-chain contract events (mints, transfers, sales, approvals, auction events)
- `market` — single active market (auction, ask, offer)
- `markets` — paginated active market listings across ZORA protocols
- `mints` — historical minting data with optional token and market details
- `nouns` — Nouns Builder DAOs, proposals, governance events, and auctions
- `offchainOrders` — Seaport offchain order book entries
- `sales` — historical sales from ZORA, OpenSea, LooksRare, Foundation, and more
- `tokens` — paginated token list with optional market summary
- `token` — single token with full market history and events
- `search` — text-based search across tokens and collections
- `mintComments` — on-chain comments submitted during minting

**Schema Source:** https://github.com/ourzora/zdk/blob/main/graph-schemas/indexer-graph.graphql

**References:**
- Documentation: https://github.com/ourzora/zora-docs/blob/main/docs/zora-api/intro.mdx
- GettingStarted: https://github.com/ourzora/zora-docs/blob/main/docs/zora-api/zdk.mdx
- SchemaFile: https://github.com/ourzora/zdk/blob/main/graph-schemas/indexer-graph.graphql
- APIKeys: https://keys.api.zora.co/
- ZDK: https://www.npmjs.com/package/@zoralabs/zdk
