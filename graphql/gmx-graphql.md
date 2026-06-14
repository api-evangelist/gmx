# GMX GraphQL API

GMX exposes historical on-chain data through a Subsquid-powered GraphQL API. The primary endpoint indexes the GMX Synthetics protocol on Arbitrum and provides deep query capabilities over trades, positions, liquidity events, fees, referrals, funding rates, and protocol-level metrics. A legacy The Graph subgraph also covers GMX v1 stats on Arbitrum and Avalanche.

## Endpoints

### Subsquid — GMX Synthetics (v2, primary)

| Network | Endpoint |
|---------|----------|
| Arbitrum | `https://gmx.squids.live/gmx-synthetics-arbitrum:prod/api/graphql` |
| Avalanche | `https://gmx.squids.live/gmx-synthetics-avalanche:prod/api/graphql` |

### The Graph — GMX Stats (v1, legacy)

| Network | Endpoint |
|---------|----------|
| Arbitrum | `https://api.thegraph.com/subgraphs/name/gmx-io/gmx-stats` |
| Arbitrum (raw) | `https://api.thegraph.com/subgraphs/name/gmx-io/gmx-arbitrum-raw` |
| Avalanche | `https://api.thegraph.com/subgraphs/name/gmx-io/gmx-avalanche-stats` |
| Referrals | `https://api.thegraph.com/subgraphs/name/gmx-io/gmx-referrals` |

Documentation: https://docs.gmx.io/docs/api/subsquid/

Source repository: https://github.com/gmx-io/gmx-subgraph

## Authentication

Both Subsquid and The Graph endpoints are publicly accessible with no API key required. Standard GraphQL POST requests with `Content-Type: application/json` are supported.

## Schema Overview (Subsquid / Synthetics v2)

The live schema (introspected June 2026) covers the following major entity groups:

### Protocol Metrics
- `PlatformStats` — aggregate deposited users, traded users, and total volume
- `VolumeInfo` / `SwapVolumeInfo` / `PositionVolumeInfo` — trading volume broken down by period and type
- `ProcessorStatus` — indexer processing state

### Markets
- `Market` — market identity (index token, long token, short token)
- `MarketInfo` — full market configuration including pool amounts, open interest caps, impact factors, borrowing factors, funding parameters, and pool values
- `OnChainSetting` — protocol-level configuration parameters stored on-chain

### Positions
- `Position` — live position snapshot per account/market including size, collateral, PnL, fees, and leverage
- `PositionChange` — event-level record of every position open, increase, decrease, and close with full fee breakdown
- `AccountStat` — per-account aggregate statistics (wins, losses, realized PnL, volume, capital utilization)

### Orders
- `Order` — individual order records with status lifecycle (Created, Executed, Cancelled, Frozen)
- `TradeAction` — unified trade event log covering all action types

### Fees
- `CollectedFeesInfo` — pool-level fee collection snapshots (position fees, borrowing fees) by period
- `SwapFeesInfo` / `SwapFeesInfoWithPeriod` — swap fee events and period aggregates
- `PositionFeesEntity` / `PositionFeesInfoWithPeriod` — position fee events and period aggregates

### Funding & Borrowing Rates
- `FundingRateSnapshot` — point-in-time funding rate snapshots per market
- `BorrowingRateSnapshot` — borrowing rate snapshots per market/side
- `MarketInfo.fundingFactorPerSecond`, `borrowingFactorPerSecondForLongs/Shorts` — live rate fields

### Liquidity (GM / GLV Tokens)
- `CumulativePoolValue` — historical pool value tracking
- `Glv` — GLV vault entity (multi-market liquidity vault)
- `AprSnapshot` / `PnlAprSnapshot` — APR snapshots for GM and GLV tokens

### Prices
- `Price` — oracle price records (min/max) per token with snapshot support

### Referrals
- `ReferralCodeOwner` — referral code to owner mapping
- `TraderReferral` — trader-to-referral-code association
- `AffiliateReferralTradeStatsByHour` — affiliate-side referral trading stats
- `TraderReferralTradeStatsByHour` — trader-side referral stats
- `AffiliateTraderStatsByHour` — affiliate's trader counts and volume

### Claimable Amounts
- `ClaimableCollateral` / `ClaimableCollateralGroup` — claimable collateral tracking after price impact
- `ClaimableFundingFeeInfo` — unclaimed funding fee amounts
- `ClaimRef` — claim reference records
- `ClaimAction` — on-chain claim event log
- `ClaimableAmount` — token-level claimable amount per account
- `Distribution` — token distribution records

### Staking
- `StakingPower` — per-account staking power snapshots
- `NetworkStakingPower` — network-wide staking power aggregates

### Multichain Funding (Cross-Chain)
- `MultichainFundingSendEvent` — cross-chain funding send events
- `MultichainFundingReceiveEvent` — cross-chain funding receive events
- `MultichainSamechainFundingEvent` — same-chain multichain funding events

### PnL / Performance
- `CumulativePnl` — cumulative PnL tracking per account or market
- `AprSnapshot` / `PnlAprSnapshot` — APR and PnL-APR snapshots

## Schema Overview (The Graph / GMX v1)

The legacy v1 subgraph covers original GMX vault-based architecture:

- `TokenStat` — per-token pool amounts, USDG amounts, reserve amounts by period
- `TradingStat` — profit/loss, open interest, liquidation stats by period
- `GlpStat` — GLP token supply, AUM, distributed ETH/esGMX rewards
- `FundingRate` — funding rate history per token
- `LiquidatedPosition` — liquidation event records
- `Order` / `OrderStat` — v1 order lifecycle and aggregate counts
- `Swap` — individual swap records with fee basis points
- `VolumeStat` — volume by type (margin, swap, liquidation, mint, burn) by period
- `UserStat` — unique user counts and action counts by period
- `ChainlinkPrice` / `UniswapPrice` / `FastPrice` — multi-source price records

## Example Queries

### Query recent trade actions (Subsquid)
```graphql
query RecentTrades {
  tradeActions(
    orderBy: timestamp_DESC
    limit: 10
  ) {
    id
    account
    market
    isLong
    sizeDeltaUsd
    collateralDeltaAmount
    executionPrice
    priceImpactUsd
    timestamp
  }
}
```

### Query market info (Subsquid)
```graphql
query MarketDetails {
  marketInfos(limit: 20) {
    id
    marketTokenAddress
    indexTokenAddress
    longTokenAddress
    shortTokenAddress
    longOpenInterestUsd
    shortOpenInterestUsd
    poolValueMax
    fundingFactorPerSecond
    borrowingFactorPerSecondForLongs
    borrowingFactorPerSecondForShorts
  }
}
```

### Query account positions (Subsquid)
```graphql
query AccountPositions($account: String!) {
  positions(
    where: { account_eq: $account }
    orderBy: sizeInUsd_DESC
  ) {
    id
    market
    collateralToken
    isLong
    sizeInUsd
    collateralAmount
    realizedPnl
    unrealizedPnl
    leverage
    entryPrice
    openedAt
  }
}
```

### Query GLP stats (The Graph v1)
```graphql
query GlpHistory {
  glpStats(
    first: 30
    orderBy: timestamp
    orderDirection: desc
    where: { period: "daily" }
  ) {
    id
    glpSupply
    aumInUsdg
    distributedEth
    distributedUsd
    timestamp
  }
}
```

## Pagination

Subsquid uses cursor-based pagination via the `Connection` pattern:

```graphql
query PaginatedPositions {
  positionsConnection(
    orderBy: sizeInUsd_DESC
    first: 50
    after: "cursor_value"
  ) {
    edges {
      node {
        id
        account
        sizeInUsd
      }
      cursor
    }
    pageInfo {
      hasNextPage
      endCursor
    }
    totalCount
  }
}
```

The Graph v1 subgraph uses offset-based `first` / `skip` pagination.

## Notes

- All monetary values are `BigInt` in raw token/USD units with 30 decimal precision (1e30 = 1 USD) in the Subsquid schema
- The Subsquid endpoint supports both list queries (with `where`, `orderBy`, `limit`, `offset`) and connection queries (cursor-paginated)
- Squid status can be checked via the `squidStatus` query which returns the current head block
- The v1 The Graph subgraph is considered legacy; new integrations should use the Subsquid v2 endpoint
