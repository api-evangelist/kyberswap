# KyberSwap

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
