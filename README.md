# KyberSwap

KyberSwap is a multi-chain DEX aggregator and liquidity protocol. It aggregates liquidity from 420+ sources across 17+ EVM chains to find optimal swap routes, and provides additional DeFi primitives including gasless limit orders, concentrated liquidity Zap-in/out, and on-chain token pricing.

All KyberSwap APIs are publicly accessible and require no API key or subscription. Protocol fees are charged at the smart-contract layer for certain transaction types, not on API access.

## APIs

| API | Base URL | Purpose |
|-----|----------|---------|
| Aggregator API | `https://aggregator-api.kyberswap.com` | Best-rate swap routing across 420+ liquidity sources |
| Limit Order API | `https://limit-order.kyberswap.com` | Gasless limit order creation and fulfillment |
| ZaaS API | `https://zap-api.kyberswap.com` | Zap-In/Out/Migrate for concentrated liquidity positions |
| OnChain Price Service | `https://price.kyberswap.com` | Real on-chain token prices per network |

## Supported Chains

Ethereum, BNB Chain, Arbitrum, Polygon PoS, Optimism, Avalanche, Base, Linea, Mantle, Sonic, Berachain, Ronin, Unichain, HyperEVM, Plasma, Etherlink, Monad, MegaETH.

## Documentation

- Developer docs: https://docs.kyberswap.com
- Aggregator API spec: https://docs.kyberswap.com/kyberswap-solutions/kyberswap-aggregator/aggregator-api-specification/evm-swaps
- Limit Order API spec: https://docs.kyberswap.com/kyberswap-solutions/limit-order/limit-order-api-specification
- ZaaS HTTP API: https://docs.kyberswap.com/kyberswap-solutions/kyberswap-zap-as-a-service/kyberswap-zap-as-a-service-zaas-api/zaas-http-api

## Contact

Business Development: bd@kyber.network
