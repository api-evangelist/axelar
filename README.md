# Axelar (axelar)

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

Axelar is a decentralized cross-chain communication network that enables secure interoperability across 80+ blockchains including EVM chains, Cosmos, Solana, Sui, Stellar, and XRPL. The network provides General Message Passing (GMP) for arbitrary cross-chain contract calls, the Interchain Token Service (ITS) for deploying and bridging tokens across chains, and the Axelarscan API suite for querying network state, validator metrics, token transfer status, and GMP transaction data. Developer tooling includes the AxelarJS SDK, the Mobius Development Stack (MDS), and Axelar Virtual Machine (AVM).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/axelar/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/axelar/refs/heads/main/apis.yml)

## Tags

- Blockchain
- Cross-Chain
- Interoperability
- Web3
- General Message Passing
- Token Bridge
- Cosmos
- EVM

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### Axelarscan API

Retrieves information about the Axelar network and the AXL token. Provides access to metrics such as circulating supply, total supply, inflation, total value locked (TVL) across 80+ chains and 30+ assets, network proposals, and overall chain health. Backed by OpenSearch-cached data for sub-second responses on mainnet.

- **Human URL:** [https://docs.axelarscan.io/axelarscan](https://docs.axelarscan.io/axelarscan)
- **Base URL:** `https://api.axelarscan.io/api`

#### Tags

- Network Stats
- TVL
- AXL Token
- Analytics

#### Properties

- [Documentation](https://docs.axelarscan.io/axelarscan)

### Axelar Validator API

Exposes metrics for validators operating on the Axelar network, including heartbeat status, uptime percentages, proposed block counts, voting participation, and quadratic voting scores. Useful for delegators evaluating validator performance and for monitoring infrastructure reliability across the 75+ active validators.

- **Human URL:** [https://docs.axelarscan.io/validator](https://docs.axelarscan.io/validator)
- **Base URL:** `https://api.axelarscan.io/api`

#### Tags

- Validators
- Staking
- Network Health
- Metrics

#### Properties

- [Documentation](https://docs.axelarscan.io/validator)

### Axelar Token Transfer API

Provides insights into cross-chain token transfers executed through the Axelar network. Returns transfer status, source and destination chain details, asset denomination, amounts, confirmation counts, and historical transfer statistics. Supports both gateway token transfers and Interchain Token Service (ITS) transfers.

- **Human URL:** [https://docs.axelarscan.io/token-transfer](https://docs.axelarscan.io/token-transfer)
- **Base URL:** `https://api.axelarscan.io/api`

#### Tags

- Token Transfer
- Cross-Chain
- ITS
- Bridge

#### Properties

- [Documentation](https://docs.axelarscan.io/token-transfer)

### Axelar GMP API

Returns information about General Message Passing (GMP) calls routed through the Axelar network. Provides transaction status, source and destination chain data, contract call payloads, gas payment status, gas estimation, and recovery details for stuck or underfunded cross-chain transactions. Complements the AxelarJS SDK GMP recovery methods.

- **Human URL:** [https://docs.axelarscan.io/gmp](https://docs.axelarscan.io/gmp)
- **Base URL:** `https://api.axelarscan.io/api`

#### Tags

- GMP
- General Message Passing
- Cross-Chain Calls
- Gas Estimation

#### Properties

- [Documentation](https://docs.axelarscan.io/gmp)

### Axelar Amplifier GMP API

The Amplifier GMP API is the HTTP REST integration layer exposed by the Axelar Amplifier relayer service. External chain integrators and relayer operators use it to publish on-chain events (CALL, MESSAGE_EXECUTED, SIGNERS_ROTATED, ITS transfer events, etc.) and to poll pending transaction tasks (EXECUTE, APPROVE_MESSAGES, ROTATE_SIGNERS) that must be submitted to destination chains. Also supports CosmWasm contract broadcast and query, and large payload pre-storage.

- **Human URL:** [https://github.com/axelarnetwork/amplifier-relayer-api](https://github.com/axelarnetwork/amplifier-relayer-api)
- **Base URL:** `https://amplifier.axelar.dev`

#### Tags

- Amplifier
- GMP
- General Message Passing
- Cross-Chain
- Relayer
- CosmWasm

#### Properties

- [Documentation](https://github.com/axelarnetwork/amplifier-relayer-api)
- [Repository](https://github.com/axelarnetwork/amplifier-relayer-api)
- [OpenAPI](openapi/amplifier-gmp-api.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### AxelarJS SDK

JavaScript/TypeScript SDK wrapping common cross-chain operations on the Axelar network. Key classes include AxelarAssetTransfer (generates deposit addresses for token transfers), AxelarQueryAPI (fee estimation, denom lookups, transfer status), and AxelarGMPRecoveryAPI (query GMP transaction status, manual relay, execute destination contract, add gas). Supports both MAINNET and TESTNET environments.

- **Human URL:** [https://docs.axelar.dev/dev/axelarjs-sdk/intro/](https://docs.axelar.dev/dev/axelarjs-sdk/intro/)
- **Base URL:** `https://github.com/axelarnetwork/axelarjs-sdk`

#### Tags

- SDK
- JavaScript
- TypeScript
- NPM
- Token Transfer
- GMP Recovery

#### Properties

- [Documentation](https://docs.axelar.dev/dev/axelarjs-sdk/intro/)
- [Repository](https://github.com/axelarnetwork/axelarjs-sdk)

## Common Properties

- [Website](https://axelar.network/)
- [Documentation](https://docs.axelar.dev/)
- [Git Hub](https://github.com/axelarnetwork)
- [Explorer](https://axelarscan.io/)
- [A P I Documentation](https://docs.axelarscan.io/)
- [Discord](https://discord.com/invite/aRZ3Ra6f7D)
- [Twitter](https://twitter.com/axelar)
- [Blog](https://axelar.network/blog)
- [Plans](plans/axelar-plans-pricing.yml)
- [Rate Limits](rate-limits/axelar-rate-limits.yml)
- [Fin Ops](finops/axelar-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
