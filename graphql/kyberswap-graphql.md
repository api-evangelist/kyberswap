# KyberSwap GraphQL API

## Description

KyberSwap Elastic exposes on-chain liquidity data through The Graph Protocol subgraph. The subgraph indexes all events from the KyberSwap Elastic (concentrated liquidity) smart contracts on Ethereum mainnet, including pool creation, swaps, mints, burns, fee collections, flash loans, and liquidity farming. It provides time-series analytics at day and hour granularity for pools, tokens, and ticks, as well as real-time position and farming pool data.

## Endpoint

- **Mainnet:** `https://api.thegraph.com/subgraphs/name/kybernetwork/kyberswap-elastic-mainnet`
- **Protocol:** GraphQL over HTTP POST
- **Authentication:** None required for hosted service queries

## Schema Source

The schema is sourced from the official KyberNetwork elastic-subgraph repository:
- https://github.com/KyberNetwork/elastic-subgraph/blob/main/schema.graphql

## Key Entity Types

| Type | Description |
|------|-------------|
| Factory | Global protocol stats — pool count, total volume, TVL, fees |
| Bundle | ETH/USD price oracle used for USD conversions |
| Token | ERC-20 token metadata, volume, TVL, and price data |
| Pool | Concentrated liquidity pool state, tick, price, volume, and TVL |
| Tick | Individual tick within a pool — liquidity, price bounds, fee growth |
| Position | NFT liquidity position (lower/upper tick, liquidity, fee growth) |
| PositionSnapshot | Point-in-time snapshot of a position at a specific block |
| Transaction | On-chain transaction with gas metadata |
| Mint | Liquidity add event within a pool |
| Burn | Liquidity removal event within a pool |
| Swap | Token swap event with amounts, sender, recipient, and price |
| Collect | Fee collection event from a position |
| Flash | Flash loan event |
| KyberSwapDayData | Protocol-wide daily aggregate stats |
| PoolDayData | Per-pool daily OHLC, volume, fees, TVL |
| PoolHourData | Per-pool hourly OHLC, volume, fees, TVL |
| TickDayData | Per-tick daily volume and liquidity |
| TickHourData | Per-tick hourly volume and liquidity |
| TokenDayData | Per-token daily OHLC, volume, TVL |
| TokenHourData | Per-token hourly OHLC, volume, TVL |
| Farm | Liquidity mining farm contract |
| FarmingPool | Individual farming pool with reward schedule |
| RewardToken | Reward token configuration for a farming pool |
| DepositedPosition | NFT position deposited into a farm |
| JoinedPosition | Position joined to a specific farming pool |

## Example Queries

### Get top pools by TVL
```graphql
{
  pools(first: 10, orderBy: totalValueLockedUSD, orderDirection: desc) {
    id
    token0 { symbol }
    token1 { symbol }
    feeTier
    totalValueLockedUSD
    volumeUSD
    txCount
  }
}
```

### Get recent swaps for a pool
```graphql
{
  swaps(
    first: 20
    orderBy: timestamp
    orderDirection: desc
    where: { pool: "0x<pool_address>" }
  ) {
    timestamp
    amount0
    amount1
    amountUSD
    sender
    recipient
  }
}
```

### Get token day data
```graphql
{
  tokenDayDatas(
    first: 30
    orderBy: date
    orderDirection: desc
    where: { token: "0x<token_address>" }
  ) {
    date
    priceUSD
    volumeUSD
    totalValueLockedUSD
    open
    high
    low
    close
  }
}
```

## Documentation

- KyberSwap Docs: https://docs.kyberswap.com
- KyberSwap Elastic: https://docs.kyberswap.com/liquidity-solutions/kyberswap-elastic
- The Graph Hosted Service: https://thegraph.com/hosted-service/subgraph/kybernetwork/kyberswap-elastic-mainnet
- GitHub (elastic-subgraph): https://github.com/KyberNetwork/elastic-subgraph
