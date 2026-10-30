# GMX

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
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

**Areas:** DeFi · Perpetual Exchange · Decentralized Exchange · Trading · Leverage · Liquidity Pools · GLP · GM Tokens · GLV · Arbitrum · Avalanche · Web3

## GMX on APIs.io

Everything profiled for GMX is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/gmx/](https://apis.io/providers/gmx/)** — or go straight to one of the APIs or properties below.

### APIs (22)

- [GMX Oracle API](https://apis.io/apis/gmx/oracle-api/) — Stable, read-only REST API providing oracle prices, market information, liquidity snapshots, APY data, and GM/GLV token info for Arbitrum, Avalanche,…
- [GMX GraphQL API](https://apis.io/apis/gmx/graphql-api/) — Historical on-chain data for GMX via Subsquid-powered GraphQL endpoints. Enables deep queries over trades, liquidity events, positions, and protocol metrics…
- [GMX Integration API](https://apis.io/apis/gmx/integration-api/) — CoinGecko-compatible trading pairs API for GMX markets on Arbitrum and Avalanche, returning ticker IDs, base and target currencies, product type (Spot or…
- [GMX TypeScript SDK](https://apis.io/apis/gmx/typescript-sdk/) — Official @gmx-io/sdk package shipping two clients: GmxSdk (SDK v1) for full read/write access via RPC, and GmxApiSdk (SDK v2) for lightweight read-only HTTP…
- [GMX Allowances API](https://apis.io/apis/gmx/gmx-allowances-api/) — The Allowances API from GMX — 1 operation(s) for allowances.
- [GMX APY API](https://apis.io/apis/gmx/gmx-apy-api/) — The APY API from GMX — 1 operation(s) for apy.
- [GMX Balances API](https://apis.io/apis/gmx/gmx-balances-api/) — The Balances API from GMX — 1 operation(s) for balances.
- [GMX Account API](https://apis.io/apis/gmx/gmx-gmx-account-api/) — The GMX Account API from GMX — 4 operation(s) for gmx account.
- [GMX JIT API](https://apis.io/apis/gmx/gmx-jit-api/) — The JIT API from GMX — 2 operation(s) for jit.
- [GMX Markets API](https://apis.io/apis/gmx/gmx-markets-api/) — The Markets API from GMX — 5 operation(s) for markets.
- [GMX Order Transactions API](https://apis.io/apis/gmx/gmx-order-transactions-api/) — The Order Transactions API from GMX — 6 operation(s) for order transactions.
- [GMX Orders API](https://apis.io/apis/gmx/gmx-orders-api/) — The Orders API from GMX — 2 operation(s) for orders.
- [GMX Pairs API](https://apis.io/apis/gmx/gmx-pairs-api/) — The Pairs API from GMX — 1 operation(s) for pairs.
- [GMX Performance API](https://apis.io/apis/gmx/gmx-performance-api/) — The Performance API from GMX — 2 operation(s) for performance.
- [GMX Positions API](https://apis.io/apis/gmx/gmx-positions-api/) — The Positions API from GMX — 2 operation(s) for positions.
- [GMX Prices API](https://apis.io/apis/gmx/gmx-prices-api/) — The Prices API from GMX — 1 operation(s) for prices.
- [GMX Rates API](https://apis.io/apis/gmx/gmx-rates-api/) — The Rates API from GMX — 1 operation(s) for rates.
- [GMX Staking API](https://apis.io/apis/gmx/gmx-staking-api/) — The Staking API from GMX — 1 operation(s) for staking.
- [GMX Subaccounts API](https://apis.io/apis/gmx/gmx-subaccounts-api/) — The Subaccounts API from GMX — 2 operation(s) for subaccounts.
- [GMX Tokens API](https://apis.io/apis/gmx/gmx-tokens-api/) — The Tokens API from GMX — 2 operation(s) for tokens.
- [GMX Trades API](https://apis.io/apis/gmx/gmx-trades-api/) — The Trades API from GMX — 2 operation(s) for trades.
- [GMX Buy Back API](https://apis.io/apis/gmx/gmx-buy-back-api/) — The Buy Back API from GMX — 1 operation(s) for buy back.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [GMX GraphQL API](https://apis.io/graphqls/gmx/gmx-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Gmx Agentic Access](https://apis.io/agentic-access/gmx/gmx-agentic-access/)

#### JSON Schema (72)

The data models the API reads and writes.

- [ApiParameterPeriod](https://apis.io/schemas/gmx/ApiParameterPeriod/)
- [ApprovalPrepareRequest](https://apis.io/schemas/gmx/ApprovalPrepareRequest/)
- [ApprovalPrepareResponse](https://apis.io/schemas/gmx/ApprovalPrepareResponse/)
- [ApyEntry](https://apis.io/schemas/gmx/ApyEntry/)
- [ApyResponse](https://apis.io/schemas/gmx/ApyResponse/)
- [BigIntToString_BuybackWeeklyStatsData_](https://apis.io/schemas/gmx/BigIntToString_BuybackWeeklyStatsData_/)
- [BigIntToString_StakingPowerData_](https://apis.io/schemas/gmx/BigIntToString_StakingPowerData_/)
- [BridgeOutParamsDto](https://apis.io/schemas/gmx/BridgeOutParamsDto/)
- [BuybackWeeklyStatsResponse](https://apis.io/schemas/gmx/BuybackWeeklyStatsResponse/)
- [CancelPrepareRequest](https://apis.io/schemas/gmx/CancelPrepareRequest/)
- [CollateralOperation](https://apis.io/schemas/gmx/CollateralOperation/)
- [CollateralPrepareRequest](https://apis.io/schemas/gmx/CollateralPrepareRequest/)
- [CrossChainDepositPrepareRequest](https://apis.io/schemas/gmx/CrossChainDepositPrepareRequest/)
- [CrossChainDepositPrepareResponse](https://apis.io/schemas/gmx/CrossChainDepositPrepareResponse/)
- [CrossChainWithdrawPrepareRequest](https://apis.io/schemas/gmx/CrossChainWithdrawPrepareRequest/)
- [CrossChainWithdrawPrepareResponse](https://apis.io/schemas/gmx/CrossChainWithdrawPrepareResponse/)
- [CrossChainWithdrawSubmitRequest](https://apis.io/schemas/gmx/CrossChainWithdrawSubmitRequest/)
- [CrossChainWithdrawSubmitResponse](https://apis.io/schemas/gmx/CrossChainWithdrawSubmitResponse/)
- [EditPrepareRequest](https://apis.io/schemas/gmx/EditPrepareRequest/)
- [GasPaymentParamsDto](https://apis.io/schemas/gmx/GasPaymentParamsDto/)
- [GlvShiftParamsResponse](https://apis.io/schemas/gmx/GlvShiftParamsResponse/)
- [GmxAccountStatusRequest](https://apis.io/schemas/gmx/GmxAccountStatusRequest/)
- [GmxAccountStatusResponse](https://apis.io/schemas/gmx/GmxAccountStatusResponse/)
- [JitLiquidityHistoryPeriod](https://apis.io/schemas/gmx/JitLiquidityHistoryPeriod/)
- [JitLiquidityHistoryResponse](https://apis.io/schemas/gmx/JitLiquidityHistoryResponse/)
- …and 47 more published on APIs.io

#### JSON-LD (2)

Linked-data contexts for the provider's vocabulary.

- [Api Context](https://apis.io/jsonld/gmx/api/)
- [context Context](https://apis.io/jsonld/gmx/context/)

#### Examples (37)

Example requests and responses.

- [Cancelprepare](https://apis.io/examples/gmx/CancelPrepare/)
- [Collateralprepare](https://apis.io/examples/gmx/CollateralPrepare/)
- [Editprepare](https://apis.io/examples/gmx/EditPrepare/)
- [Fetchstatus](https://apis.io/examples/gmx/FetchStatus/)
- [Getallowances](https://apis.io/examples/gmx/GetAllowances/)
- [Getannualized](https://apis.io/examples/gmx/GetAnnualized/)
- [Getapy](https://apis.io/examples/gmx/GetApy/)
- [Getliquidityhistory](https://apis.io/examples/gmx/GetLiquidityHistory/)
- [Getliquidityinfo](https://apis.io/examples/gmx/GetLiquidityInfo/)
- [Getmarkets](https://apis.io/examples/gmx/GetMarkets/)
- [Getmarketsconfig](https://apis.io/examples/gmx/GetMarketsConfig/)
- [Getmarketsinfo](https://apis.io/examples/gmx/GetMarketsInfo/)
- [Getmarketstickers](https://apis.io/examples/gmx/GetMarketsTickers/)
- [Getmarketsvalues](https://apis.io/examples/gmx/GetMarketsValues/)
- [Getohlcv](https://apis.io/examples/gmx/GetOhlcv/)
- [Getorderbykey](https://apis.io/examples/gmx/GetOrderByKey/)
- [Getordersbyaddress](https://apis.io/examples/gmx/GetOrdersByAddress/)
- [Getpairs](https://apis.io/examples/gmx/GetPairs/)
- [Getpositionbykey](https://apis.io/examples/gmx/GetPositionByKey/)
- [Getpositionsinfo](https://apis.io/examples/gmx/GetPositionsInfo/)
- [Getrates](https://apis.io/examples/gmx/GetRates/)
- [Getsnapshots](https://apis.io/examples/gmx/GetSnapshots/)
- [Getstakingpower](https://apis.io/examples/gmx/GetStakingPower/)
- [Gettokens](https://apis.io/examples/gmx/GetTokens/)
- [Gettokensinfo](https://apis.io/examples/gmx/GetTokensInfo/)
- …and 12 more published on APIs.io

#### Collections (18)

Postman and Open Collection request collections.

- [@gmx-io/gmx-public-api Allowances API](https://apis.io/collections/gmx/open-gmx-allowances-api/)
- [@gmx-io/gmx-public-api Allowances APY API](https://apis.io/collections/gmx/open-gmx-apy-api/)
- [@gmx-io/gmx-public-api Allowances Balances API](https://apis.io/collections/gmx/open-gmx-balances-api/)
- [@gmx-io/gmx-public-api Allowances Buyback API](https://apis.io/collections/gmx/open-gmx-buyback-api/)
- [@gmx-io/gmx-public-api Allowances GMX Account API](https://apis.io/collections/gmx/open-gmx-gmx-account-api/)
- [@gmx-io/gmx-public-api Allowances JIT API](https://apis.io/collections/gmx/open-gmx-jit-api/)
- [@gmx-io/gmx-public-api Allowances Markets API](https://apis.io/collections/gmx/open-gmx-markets-api/)
- [@gmx-io/gmx-public-api Allowances Order Transactions API](https://apis.io/collections/gmx/open-gmx-order-transactions-api/)
- [@gmx-io/gmx-public-api Allowances Orders API](https://apis.io/collections/gmx/open-gmx-orders-api/)
- [@gmx-io/gmx-public-api Allowances Pairs API](https://apis.io/collections/gmx/open-gmx-pairs-api/)
- [@gmx-io/gmx-public-api Allowances Performance API](https://apis.io/collections/gmx/open-gmx-performance-api/)
- [@gmx-io/gmx-public-api Allowances Positions API](https://apis.io/collections/gmx/open-gmx-positions-api/)
- [@gmx-io/gmx-public-api Allowances Prices API](https://apis.io/collections/gmx/open-gmx-prices-api/)
- [@gmx-io/gmx-public-api Allowances Rates API](https://apis.io/collections/gmx/open-gmx-rates-api/)
- [@gmx-io/gmx-public-api Allowances Staking API](https://apis.io/collections/gmx/open-gmx-staking-api/)
- [@gmx-io/gmx-public-api Allowances Subaccounts API](https://apis.io/collections/gmx/open-gmx-subaccounts-api/)
- [@gmx-io/gmx-public-api Allowances Tokens API](https://apis.io/collections/gmx/open-gmx-tokens-api/)
- [@gmx-io/gmx-public-api Allowances Trades API](https://apis.io/collections/gmx/open-gmx-trades-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [GMX — jsonschema rules](https://apis.io/rules/gmx/gmx-jsonschema-spectral-rules/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Gmx Domain Security](https://apis.io/security/gmx/gmx-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Gmx Plans Pricing](https://apis.io/plans/gmx/gmx-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Gmx Rate Limits](https://apis.io/rate-limits/gmx/gmx-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Gmx Finops](https://apis.io/finops/gmx/gmx-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://gmx.io)
- [Documentation](https://docs.gmx.io/docs/api/overview/)
- [Changelog](https://docs.gmx.io/docs/ai-agents/overview/)
- [Blog](https://medium.com/@gmx.io)

## API Evangelist rating

**Kin Score 26.1** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 46.4 |
| Contract governance | 9.8 |
| Operational transparency | 28.9 |
| Developer ergonomics | 16.7 |
| Access clarity | 5.3 |

**Agent readiness 17.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/gmx/](https://apis.io/providers/gmx/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for GMX: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/gmx/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
