# Zora

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
