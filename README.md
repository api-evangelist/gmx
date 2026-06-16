# GMX (gmx)

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
