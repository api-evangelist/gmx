# GMX (gmx)

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

GMX is a decentralized perpetual and spot exchange deployed on Arbitrum, Avalanche, Botanix, and MegaETH, supporting trades with up to 100x leverage and low-price-impact token swaps powered by oracle-based pricing. The platform exposes four integration surfaces: a GMX REST API (primary, OpenAPI-documented) for account data, orders, analytics, and relayed workflows; an Oracle API (stable) for oracle prices, markets, liquidity snapshots, and APY; a GraphQL API via Subsquid for historical on-chain data; and an MCP server plus TypeScript SDK for AI-agent and programmatic access. Data coverage includes markets, tickers, tokens, positions, orders, rates, APY, performance, wallet balances, GLP/GM/GLV token analytics, OHLCV, buyback stats, and staking power.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gmx/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gmx/refs/heads/main/apis.yml)

## Tags

- DeFi
- Perpetual Exchange
- DEX
- Trading
- Leverage
- Liquidity Pools
- GLP
- GM Tokens
- GLV
- Arbitrum
- Avalanche
- Web3

## Timestamps

- **Created:** 2026-06-14
- **Modified:** 2026-06-14

## APIs

### GMX API

Primary HTTP integration surface for GMX, actively developed and OpenAPI-documented. Covers account data, order information, trading analytics, wallet balances, allowances, staking power, buyback stats, JIT liquidity, subaccounts, and API-relayed order workflows across all supported networks.

- **Human URL:** [https://docs.gmx.io/docs/api/overview/](https://docs.gmx.io/docs/api/overview/)
- **Base URL:** `https://arbitrum.gmxapi.io/v1`

#### Tags

- Trading
- Orders
- Positions
- Analytics
- Accounts

#### Properties

- [Documentation](https://docs.gmx.io/docs/api/overview/)
- [OpenAPI](https://docs.gmx.io/docs/api/overview/) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### GMX Oracle API

Stable, read-only REST API providing oracle prices, market information, liquidity snapshots, APY data, and GM/GLV token info for Arbitrum, Avalanche, Botanix, and MegaETH. Primary endpoints live at {chain}-api.gmxinfra.io with documented fallback hosts for high availability.

- **Human URL:** [https://docs.gmx.io/docs/api/rest/](https://docs.gmx.io/docs/api/rest/)
- **Base URL:** `https://arbitrum-api.gmxinfra.io`

#### Tags

- Oracle
- Prices
- Markets
- Liquidity
- APY

#### Properties

- [Documentation](https://docs.gmx.io/docs/api/rest/)

### GMX GraphQL API

Historical on-chain data for GMX via Subsquid-powered GraphQL endpoints. Enables deep queries over trades, liquidity events, positions, and protocol metrics indexed from Arbitrum and Avalanche chains.

- **Human URL:** [https://docs.gmx.io/docs/api/subsquid/](https://docs.gmx.io/docs/api/subsquid/)
- **Base URL:** `https://gmx.squids.live/gmx-synthetics-arbitrum:prod/api/graphql`

#### Tags

- GraphQL
- Historical Data
- On-Chain
- Subsquid

#### Properties

- [Documentation](https://docs.gmx.io/docs/api/subsquid/)
- [Graph Q L](graphql/gmx-graphql.md)
- [Graph Q L Schema](graphql/gmx-schema.graphql)

### GMX Integration API

CoinGecko-compatible trading pairs API for GMX markets on Arbitrum and Avalanche, returning ticker IDs, base and target currencies, product type (Spot or Perpetual), last price, 24-hour high/low, base and target volumes, and open interest for each market.

- **Human URL:** [https://github.com/gmx-io/gmx-integration-api](https://github.com/gmx-io/gmx-integration-api)
- **Base URL:** `https://gmx-integration-cg.vercel.app/api`

#### Tags

- Trading Pairs
- Tickers
- Market Data
- CoinGecko

#### Properties

- [Documentation](https://github.com/gmx-io/gmx-integration-api)
- [Git Hub](https://github.com/gmx-io/gmx-integration-api)

### GMX TypeScript SDK

Official @gmx-io/sdk package shipping two clients: GmxSdk (SDK v1) for full read/write access via RPC, and GmxApiSdk (SDK v2) for lightweight read-only HTTP access covering markets, tickers, tokens, pairs, rates, APY, performance, positions, orders, OHLCV, buyback stats, and staking power.

- **Human URL:** [https://docs.gmx.io/docs/sdk/](https://docs.gmx.io/docs/sdk/)
- **Base URL:** `https://www.npmjs.com/package/@gmx-io/sdk`

#### Tags

- SDK
- TypeScript
- JavaScript
- RPC

#### Properties

- [Documentation](https://docs.gmx.io/docs/sdk/)
- [Git Hub](https://github.com/gmx-io/gmx-interface)

## Common Properties

- [Website](https://gmx.io)
- [Documentation](https://docs.gmx.io/docs/api/overview/)
- [Git Hub](https://github.com/gmx-io)
- [Twitter](https://x.com/GMX_IO)
- [Discord](https://discord.gg/ymN38YefH9)
- [Blog](https://medium.com/@gmx.io)
- [Changelog](https://docs.gmx.io/docs/ai-agents/overview/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
