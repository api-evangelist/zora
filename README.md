# Zora

Zora is an NFT protocol and marketplace that enables creators to mint, sell, and manage digital collectibles across Ethereum mainnet and Layer 2 networks including the Zora Network (an OP Stack L2), Base, and Optimism. The platform exposes a GraphQL NFT API for querying collections, token metadata, mint events, on-chain sales, and creator royalty data; a Coins SDK REST API for exploring and trading Zora Coins (creator monetization tokens); and a Protocol SDK for contract-level interactions covering ERC-721 and ERC-1155 minting workflows.

## APIs

| API | Base URL | Description |
|-----|----------|-------------|
| Zora NFT GraphQL API | `https://api.zora.co/graphql` | Query NFT metadata, sales, mints, collections, and token data |
| Zora Coins SDK REST API | `https://api-sdk.zora.engineering/api` | Coins market data, profiles, and discovery lists |
| Zora Protocol SDK | TypeScript package | Creator and Collector clients for minting ERC-721 and ERC-1155 tokens |
| Zora Network RPC | `https://rpc.zora.energy` | JSON-RPC access to the Zora Network L2 chain |

## Authentication

API key registration is available at https://zora.co/settings/developer. Without a key, the NFT GraphQL API and Coins SDK REST API allow up to 120 requests per minute. An API key significantly increases this limit and is required for production applications.

- NFT GraphQL API: `X-API-KEY: <key>` header
- Coins SDK REST API: `api-key: <key>` header

## Resources

- Website: https://zora.co
- Developer Docs: https://docs.zora.co
- NFT API Docs: https://github.com/ourzora/zora-docs/blob/main/docs/zora-api/intro.mdx
- Coins SDK REST API: https://docs.zora.co/coins/sdk/public-rest-api
- Interactive OpenAPI: https://api-sdk.zora.engineering/docs
- Protocol SDK: https://nft-docs.zora.co/protocol-sdk/introduction
- GitHub: https://github.com/ourzora
- X: https://x.com/zoradevs

## Repository Contents

- `apis.yml` — APIs.json 0.19 provider profile
- `plans/zora-plans-pricing.yml` — API access tiers and pricing
- `rate-limits/zora-rate-limits.yml` — Rate limit policies
- `finops/zora-finops.yml` — FinOps Framework FOCUS-aligned cost model
