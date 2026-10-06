# Snapshot and Tally (now Cactus): governance infrastructure assessment

**Access date:** 2026-10-06  
**Decision context:** This assessment informs a **new public-benefit marketing, recruiting, promotion, community-management, and governance-operations organization** for the Kimosabe App and Human Blockchain. It assesses only Snapshot and its historically relevant on-chain execution partner, Tally.

## Current identity and maintenance status

**OBSERVED — Snapshot is an actively maintained governance stack, not merely a legacy off-chain poll site.** Its current public `sx-monorepo` contains the Vue frontend, GraphQL API, off-chain hub, multi-chain Snapshot X indexer, gas relayer, MCP server, and TypeScript SDK. The repository is MIT-licensed, marked non-archived, had **55 GitHub stars**, and its `pushed_at` timestamp was **2026-10-01** when checked on 2026-10-06. The historical `snapshot-v1` interface repository remains non-archived with **9,079 stars** and was pushed on **2026-09-14**. Those are activity signals, not a security or availability guarantee. [4] [6] [7]

**OBSERVED — Several older Snapshot repositories are explicitly superseded or archived.** `snapshot-hub` is archived and directs users to `sx-monorepo`; `snapshot-strategies` is also archived/deprecated in favor of newer architecture. Do not build a new deployment around those legacy repositories merely because their older star counts are larger. [11] [28]

**OBSERVED/REPORTED — “Tally” is no longer the current product brand.** A March 19, 2026 Snapshot post states that Tally announced a shutdown and that its app would begin winding down at the end of that month. A credible third-party report attributed the wind-down to an unsustainable DAO-tooling business model. Later, a June 17, 2026 post by Scopelift says it had “taken over Tally,” retired the Tally brand, and rebranded the platform as **Cactus**, initially still hosted on `tally.xyz`; the current site’s metadata and banner likewise say “Tally is now Cactus. New name, same platform.” [5] [23] [24] [15]

> **Lifecycle judgment:** **Snapshot: actively maintained.** **Tally brand: retired/dormant as a standalone vendor identity.** **Cactus successor platform: apparently active, but continuity is only reported by the successor and observed on its web presence; its ownership terms, enterprise support continuity, and long-term operating model were not independently verified.** Tally’s publicly visible `tally-zero` repository is MIT and non-archived but its latest commit was 2025-12-11, before the reported wind-down; that does **not** establish that the former hosted Tally product remains publicly maintained. [22] [26]

## What it is and who it serves

**OBSERVED — Snapshot is governance infrastructure for DAOs, DeFi protocols, and NFT communities.** Its core legacy service enables configurable, **gasless off-chain signed voting** through organization-specific “Spaces,” strategies, vote types, and proposal rules. The official overview describes the platform as off-chain and open source. [1]

**OBSERVED — Snapshot now spans three related modes.**

- **Snapshot (legacy/off-chain):** signed messages; voting power is computed at a defined blockchain snapshot; no voter gas is required. It is well suited to sentiment checks, ratification processes, and coordination whose real-world enforcement is handled elsewhere. [1] [13]
- **Snapshot X:** modular, on-chain voting and execution on Starknet. A deployed Space combines authenticators, voting strategies, a proposal-validation strategy, and execution strategies. Anyone may permissionlessly execute an approved proposal through its configured execution strategy. [3]
- **Governor interface:** since March 2026, Snapshot says it supports OpenZeppelin Governor and Governor Bravo DAOs from temperature check through on-chain voting and execution in one interface. This is a user interface and integration layer over the DAO’s existing Governor/timelock contracts, not a replacement for those contracts. [5] [17]

**REPORTED — Snapshot’s historical adoption is substantial, but the figures are dated.** Starknet’s September 2024 launch announcement reported that Snapshot served 96% of DAOs and 500,000 monthly active users, while Anchorage reported that by April 2023 it saw more than 1,600 Spaces with at least one proposal, more than 5,500 proposals, and more than 600 proposals with over 100 distinct votes. These figures should be treated as historical partner-reported indicators, **not current market share**. [12] [13]

**OBSERVED — Tally was a hosted governance interface and services business for on-chain organizations; Cactus presents itself as its successor.** The historical Tally product served token holders, delegates, proposers, DAOs, foundations, and service providers with dashboards for proposals, voting, delegation, and execution. Its 2025 funding announcement described a broader suite for launch, governance/operations, and staking-based growth. The present `tally.xyz` page is branded Cactus and advertises on-chain proposal creation/voting, autonomous execution, voting-power management, signaling votes, custodian integration, an API, staking, token launch, and distribution capabilities. [18] [15]

## License and primary repositories

**OBSERVED — Snapshot’s current primary public codebase is [`snapshot-labs/sx-monorepo`](https://github.com/snapshot-labs/sx-monorepo), under the MIT License.** It is the appropriate technical reference for the present front-end/API/relayer/SDK stack. `snapshot-labs/snapshot-v1` is also MIT and remains the important historical repository with 9,079 stars, but its own description calls it the “V1 interface.” [4] [6] [7]

**OBSERVED — Tally/Cactus’s complete hosted product source and its license could not be verified as public.** The public [`withtally/tally-zero`](https://github.com/withtally/tally-zero) fallback voter client is MIT-licensed and is designed for React/IPFS deployment. The separate `gov-deployer` helper is MIT. Neither is evidence that the full former Tally hosted dashboard, indexer, API, or successor Cactus service is open source. **Do not describe Tally/Cactus as an open-source platform without a written license confirmation for the specific component.** [22] [26]

## Core capabilities

### Snapshot

**OBSERVED — Flexible eligibility and voting power.** A Snapshot Space can use configurable voting strategies. The legacy model supports token, NFT, delegation, and custom calculations; the latter can ask an external API for address scores. Snapshot X turns its strategy logic into contracts and permits arbitrary logic for voting power, including token, NFT, quadratic, badge, or custom state-variable-based designs. This flexibility is useful but changes the trust boundary: an external score API or a custom strategy requires its own integrity controls and audit. [3] [8]

**OBSERVED — Proposal and vote configuration.** Spaces may define members, a minimum proposal score, an “only members” proposal switch, voting strategies, voting systems, and proposal-validation rules. Snapshot X separately configures eligible proposers, authenticators, voting strategies, and execution strategies. In both cases, governance is configured **per Space**, rather than supplied as a universal membership constitution. [3] [8]

**OBSERVED — Gasless participation is implemented differently by mode.** Legacy Snapshot votes are signed off-chain messages, therefore no chain transaction/gas fee is needed. Snapshot X can sponsor on-chain proposal/vote submission through the Mana meta-transaction relayer. Snapshot’s Governor integration says an operator can top up a relayer account to sponsor voter gas. Sponsorship moves cost from voters to the organization; it should be rate-limited and separately budgeted. [1] [4] [5]

**OBSERVED — Execution tools now include transaction construction and simulation.** Snapshot’s Governor offering includes an execution builder for token/NFT transfers and contract calls, ABI autodetection through Sourcify, Tenderly simulation, treasury display, WalletConnect handoff, and a Governor/Snapshot combined view. Snapshot X’s execution strategy can authorize or directly execute the encoded transaction bundle after the vote. [3] [5]

**OBSERVED — The stack is extensible.** The current monorepo includes a GraphQL API, multi-chain indexer, transaction relayer, TypeScript `sx.js` SDK, MCP server, and off-chain sequencer. The legacy documentation also describes a Hub GraphQL API and webhook notifications for proposal creation/start/end events. [4] [9] [10]

### Tally / Cactus

**OBSERVED — The original Tally model was a dashboard and service layer over on-chain governance, particularly OpenZeppelin Governor and Compound Governor-style systems.** The Tally OpenZeppelin guide describes token delegation/self-delegation, proposer thresholds, voting delays/periods, quorum, timelock queuing, cancellation conditions, and execution. The contract—not the hosted UI—governs the authority to vote and execute. [16] [17]

**REPORTED — Its advanced operations offering included automated execution, relayer-based gasless voting, custom domains, delegate reputation display, forum synchronization, notifications, Safe homepages, analytics, and treasury analytics.** These capabilities appear in Tally’s 2025 service proposal to Compound. They are best treated as scoped/vendor-delivered capabilities, not universally available product guarantees, because the document is a proposal and several items are future deliverables. [19]

**OBSERVED — An API integration existed.** Tally’s public quickstart instructs users to generate an API key, use the GraphQL playground, and query governors/proposals. It explicitly warns that only the Governors and Proposals queries are stable while other queries/mutations may be changed or deprecated. [21]

**OBSERVED — Tally Zero provides a narrow resilience pattern.** It is an open-source, IPFS-oriented, read-only/on-chain voting frontend designed to allow direct interaction with Governor contracts without the hosted Tally service. It is useful as a contingency interface, not a complete governance-operations or community-management product. [19] [22]

## Governance model

**OBSERVED — Snapshot itself does not impose a single constitution or elect a cross-platform governing body for each community.** Each Space’s administrator/ENS owner and settings determine proposal eligibility, strategy, voting configuration, members, and off-chain enforcement. Consequently, a Space can model a wide range of policies, but policy legitimacy and appeals do not arrive “out of the box.” [8]

**OBSERVED — Legacy Snapshot is principally a decision-record and signaling system, not trustless execution.** Anchorage describes the key trade-off: gasless votes are off-chain and decisions are typically enforced by a protocol-team multisig. That can be adequate for real-world coordination or temperature checks but creates a gap between result and action unless the organization publishes who must act, by when, and under which safeguards. [13]

**OBSERVED — Snapshot X and Governor governance can bind actions only through the configured smart-contract authority.** Snapshot X can execute passed payloads permissionlessly through its execution strategy. OpenZeppelin Governor supports modular voting/quorum/counting rules and, where configured, a timelock controller. The familiar lifecycle is proposal → delay → vote → quorum/majority → queue → timelocked execution; particular settings vary by DAO. [3] [17]

**INFERRED — A Kimosabe public-benefit organization should separate three decisions that these tools otherwise conflate:** (1) community sentiment and seasonal-credit signaling; (2) verified county/stakeholder membership and role legitimacy; and (3) binding authority over ledger changes, funds, or production systems. Snapshot can improve transparency in (1) and parts of (3), but cannot establish civil identity, public-benefit accountability, or fair territorial representation by itself.

## Membership, roles, delegation, contribution, and recruiting mechanics

**OBSERVED — Snapshot’s basic membership is wallet/address and Space configuration, not personhood or an HR/community CRM record.** The legacy Space guide calls “members” the addresses allowed to create official “Core” proposals; it permits a minimum token score and an only-members-proposals filter. The Space derives its identity from an ENS domain and its owner sets/edits settings. This is appropriate for wallet-native communities, but it does not verify a U.S. county relationship, stakeholder designation, age, eligibility, contribution, or consent. [8]

**OBSERVED — Snapshot supports delegate discovery and delegation, but delegation is address-based.** Users can delegate through a Space-specific delegate registry, Snapshot’s delegation page, or direct smart-contract interaction. Delegations can apply globally or to one Space, and a `with-delegation` voting strategy must be added for delegated votes to count. The current Governor interface adds ranked delegate discovery, statements, direct delegation, and vote history. [2] [5]

**OBSERVED — Tally/OpenZeppelin delegation is also token/address based.** A voter must delegate tokens to a third party or self-delegate before token votes count in the Governor workflow. Proposal rights depend on the protocol’s threshold; the governance contract sets voting period, quorum, and timelock. [16] [17]

**REPORTED — Tally’s service proposals use delegate reputation and operational communications to improve participation.** The Compound proposal describes Karma delegate scores, a Discourse forum bot, notification channels, monthly office hours, and DAO health reporting. Those are promising governance-operations patterns, but are vendor services and not a substitute for locally designed recruiting, training, conflict-of-interest, or safeguarding processes. [19]

**INFERRED — Neither product natively runs the Kimosabe recruiting funnel.** There is no verified evidence that Snapshot or Tally/Cactus provides county-based lead assignment, volunteer onboarding, contribution credentialing, seasonally expiring community credits, referral attribution, campaign segmentation, opt-in outreach consent, or staff/community-manager role workflows. Any claim otherwise should be treated as **unverified**.

## Treasury and fund management

**OBSERVED — Snapshot legacy is not a treasury custodian or fund manager.** It can record a vote about spending, but off-chain results need a separately authorized multisig/administrator to carry out action. That separation is explicitly noted by Anchorage. [13]

**OBSERVED — Snapshot’s newer stacks can prepare and execute on-chain actions when the DAO has delegated that authority.** Snapshot X execution strategies can execute approved transactions; Snapshot’s Governor UI can construct/simulate transactions, show treasuries, and connect through WalletConnect. This is governance-controlled execution, **not** custody, accounting, bookkeeping, grant due diligence, banking, or fiduciary fund management. [3] [5]

**REPORTED — Tally proposed treasury analytics and Safe visibility, while operating through the DAO’s underlying governance contracts.** Its Compound proposal describes token holdings, flows, runway projections, historical changes, and Safe pages; the 2025 company announcement says its operating suite supports treasury management. These claims do not prove a general-ledger, accounting, or regulated-custody function. [18] [19]

**INFERRED — For Human Blockchain, use an external, auditable General Ledger as the authoritative record.** A governance platform should submit signed approvals, references, and execution receipts to that ledger; it should never be the sole record of county credits, public-benefit allocations, claims, or legal obligations.

## Hosting model, APIs, and extension surfaces

**OBSERVED — Snapshot is unusually self-hostable for the governance field.** Its MIT monorepo is a practical starting point for independent operation: front end, API, hub, indexer, relayer, SDK, and MCP server are all named components. Its earlier hub deployment instructions require a MySQL database, environment configuration, and a private relayer key, illustrating that self-hosting shifts operational and key-management responsibility to the operator. [4] [11]

**OBSERVED — Snapshot integration surfaces include GraphQL, webhooks, and SDKs.** The Hub documentation describes GraphQL data queries and a 60-requests-per-minute limit unless an API key is obtained. Webhooks send proposal lifecycle events to a configured endpoint. The current product announcement says `api.snapshot.box` unifies Governor and Snapshot X data and that an indexer can be run independently. [9] [10] [5]

**OBSERVED — Tally historically offered a hosted GraphQL API, but the successor migration is a material dependency.** The quickstart requires a Tally API key. The Cactus rebrand post asks API users to contact the successor for migration as domains change. Do not embed old `tally.xyz`/`api.withtally.com` endpoints into a production workflow without a written migration and data-export commitment. [21] [23]

**OBSERVED — Tally Zero can be independently hosted on IPFS/Fleek or other hosting, but it is only a client.** It is a reasonable “break glass” example, not proof of self-hosting parity with a complete Cactus/Tally service. [22]

## Business model and funding

**OBSERVED — Snapshot is open-source infrastructure with a visible paid support/product tier.** Its March 2026 Governor post offers six months of free migration support, then lists **Snapshot Pro at $6,000/year** for standard OpenZeppelin Governor/Governor Bravo integrations, explicitly excluding execution fees and noting that some functions are not included. This is the most concrete current pricing evidence found. [5]

**REPORTED — A 2021 news report said Snapshot Labs raised a $4 million seed round, but a primary financing announcement was not located in the sources reviewed.** Treat that amount and investor composition as **unverified for decision-making** until Snapshot Labs or lead investors confirm it in a primary record. It should not be used to infer present runway or support capacity.

**OBSERVED — Tally announced an $8 million Series A on 2025-04-22.** The company’s Business Wire release names AppWorks, Blockchain Capital, and 1kx as leads and CyberFund, Placeholder, BitGo, and Bloccelerate as participants. It claimed hundreds of thousands of launch-tool users and over $1 billion moved using Tally infrastructure; those traction figures are **company-reported**. [18]

**REPORTED — Tally’s former enterprise/service model included a self-serve offering with a proposal fee and custom support/development.** In a Compound proposal, Tally priced a 12-month dedicated service engagement at $150,000 (stated discounted from $250,000) plus separate future work. An ENS proposal outlined $180,000 year-one work and $60,000 recurring enterprise support. These were proposals, not verified executed contracts or universal price cards. [19] [20]

**INFERRED — The former Tally outcome illustrates a material commercial risk.** High usage and a major Series A did not prevent the reported wind-down; a public-benefit organization should avoid an operating model whose critical governance, community history, and notification channels depend on a venture-funded portal without exit, export, and continuity rights. [18] [24]

## Strengths

- **OBSERVED — Low-friction participation:** Snapshot’s signed off-chain votes and relayer-sponsored on-chain options remove voter gas as a participation barrier. [1] [4] [5]
- **OBSERVED — Highly configurable governance:** Snapshot X supports custom authenticators, voting-power strategies, proposal validation, and execution strategies; it can reflect more than a single ERC-20 balance. [3]
- **OBSERVED — Strong public-code and integration posture:** Snapshot’s current MIT monorepo packages front end, APIs, indexers, relayers, SDK, and MCP components; that creates credible exit/self-hosting options. [4] [6]
- **OBSERVED — Clear on-chain execution pattern:** OpenZeppelin Governor plus timelock gives a familiar, auditable proposal lifecycle, while the new Snapshot Governor UI adds simulation and execution construction. [5] [17]
- **REPORTED — Mature delegate/operations patterns:** Tally service proposals demonstrate useful practices—delegate profiles, reputation signals, notifications, forum synchronization, proposal simulations, service metrics, and resilience UI. [19] [20]
- **OBSERVED — Governance-resilience precedent:** Tally Zero’s IPFS client and Snapshot’s self-hostable components demonstrate that the public interface need not be a single point of failure. [4] [22]

## Gaps and unresolved weaknesses

- **OBSERVED — Wallet/token voting is not civic membership:** Neither platform demonstrates verified county residency, stakeholder-class eligibility, one-person safeguards, consent management, conflict checks, or public-benefit accountability. [2] [16]
- **OBSERVED — Off-chain Snapshot decisions need an accountable enforcement path:** the result can be ignored or selectively implemented by the responsible multisig/administrator unless the organization supplies binding rules and audit trails. [13]
- **OBSERVED — Flexible strategies create new trust and audit obligations:** custom off-chain score APIs, privileged space administrators, relayers, custom contracts, bridges/storage proofs, and execution strategies can each alter outcomes or create attack paths. [3] [8]
- **OBSERVED — Delegation can reproduce concentration:** an address-based delegate directory does not solve voter apathy, delegate capture, token concentration, or unequal regional representation. This is a design risk rather than a product defect. [2] [16]
- **OBSERVED — Tally/Cactus continuity is unsettled for a new dependency:** the public evidence includes a shutdown announcement, then a takeover/rebrand. Its full code license, API/deprecation policy after migration, ownership terms, audit posture, commercial SLAs, and data-retention/export guarantees were not verified. [5] [21] [23]
- **REPORTED — Several valuable Tally functions were proposed rather than proven generally available:** auto-execution, analytics, treasury views, custom domains, webhooks, integrations, and SLA response targets must be contracted and acceptance-tested; proposal language is not a product guarantee. [19] [20]
- **INFERRED — Neither tool is a General Ledger, CRM, field-organizing system, marketing automation suite, safeguarding workflow, or dispute-resolution system.** Building any of those functions requires an independent data model, permissions model, and human operations process.

## Relevance to a Kimosabe/Human Blockchain marketing, recruiting and management organization

### ADOPT

- **ADOPT the two-stage governance pattern:** run low-friction, public, signed **signal/temperature checks** before any binding ledger, treasury, or protocol change. Snapshot’s gasless model is a strong precedent for reducing participation friction. **Reason:** seasonal community credits and campaign decisions need broad input without forcing every stakeholder to pay gas. Bind only the final, clearly scoped actions through an authoritative workflow. [1] [13]
- **ADOPT a public delegate directory, statements, voting history, and proposal lifecycle notifications.** **Reason:** these features make local representatives visible and enable recruiting/retention through recognition and accountability. Use county, stakeholder group, term, conflict disclosures, and activity status as first-class fields—beyond a wallet address. [5] [19]
- **ADOPT GraphQL/webhook/event patterns for an independent operations console.** **Reason:** proposal-created, voting-started, quorum/reached, vote-ended, and execution-receipt events can trigger opt-in communications, community-manager work queues, dashboards, and archival to the General Ledger. [9] [10] [19]
- **ADOPT a resilience requirement:** any public governance interface must have exportable data, a static/IPFS-style contingency viewer, and an independently operable read path. **Reason:** the Tally transition demonstrates why governance cannot depend on a single hosted UI. [22] [23]

### ADAPT

- **ADAPT Snapshot Spaces into county-and-stakeholder “jurisdictions,” not generic token communities.** Replace ENS/wallet-only admission with a Kimosabe-issued, privacy-preserving eligibility credential tied to county, stakeholder group/designation, season, and consent. **Reason:** territory and public-benefit legitimacy cannot be inferred from token ownership. This is an independent design requirement; Snapshot merely supplies configurable authorization precedents. [3] [8]
- **ADAPT voting power into a transparent, capped, auditable community-credit formula.** Use time-bounded non-transferable credentials, contribution receipts, anti-Sybil review, and representation caps; publish plain-language explanations and an appeal process. **Reason:** arbitrary strategy flexibility is useful, but “custom API score” alone is too weak for consequential outcomes. [3] [8]
- **ADAPT delegation with duty-of-care controls:** delegate applications, term limits, county/stakeholder coverage, disclosure, recall, participation minimums, and auditable vote rationales. **Reason:** address delegation alone enables concentration and does not recruit or prepare responsible human representatives. [2] [16]
- **ADAPT the execution builder into a preflight workflow:** human-readable action summaries, simulation, independent review, a minimum notice period, and an immutable General Ledger reference before/after execution. **Reason:** it preserves the useful Governor/Snapshot X execution discipline while acknowledging that ledger updates and community-credit conversions have social/legal effects beyond a contract call. [3] [5]
- **ADAPT enterprise-service ideas as an internal operating playbook, not a vendor promise:** notification SLAs, forum sync, analytics, office hours, and proposal support are valuable; measure them by county and stakeholder group. **Reason:** Kimosabe’s management organization must own outreach and community health even if it uses external governance tooling. [19] [20]

### REJECT

- **REJECT one-token-one-vote as the primary Kimosabe membership rule.** **Reason:** wealth-weighted, transferable holdings conflict with the stated county-level stakeholder network and public-benefit mission. Token balances may be a disclosed supplemental input only if independently justified.
- **REJECT using off-chain Snapshot results as automatic authorization for money, legal commitments, credit conversion, or personal-data changes.** **Reason:** legacy Snapshot has no intrinsic enforcement; binding actions need predefined authorization, review, and auditable execution. [13]
- **REJECT treating Snapshot, Tally, or Cactus as the General Ledger, CRM, recruiting system, or treasury custodian.** **Reason:** none supplies the comprehensive records, privacy controls, human operations, or fiduciary controls required by this use case. [5] [18] [19]
- **REJECT a new hard dependency on the retired Tally brand or undocumented successor endpoints.** **Reason:** transition risk is material and the core hosted platform license/continuity is not verified. [5] [23]

### DEFER

- **DEFER production use of Cactus/Tally successor services** until due diligence obtains a signed statement of product ownership, service continuation, pricing, SLA, API migration/deprecation policy, export format, data-retention/deletion, incident handling, security/audit evidence, and termination assistance. **Reason:** public rebrand messaging is insufficient for public-benefit critical infrastructure. [21] [23]
- **DEFER Snapshot X for binding multi-treasury/community-credit execution** until a threat model, contract/strategy audits, relayer-budget controls, L1/L2 proof assumptions, rollback/guardian policy, and a county-representation test are completed. **Reason:** its flexibility and cross-chain design increase the analysis surface. [3] [12]
- **DEFER conclusions about Snapshot Labs’ current financing/runway and Cactus’s long-term commercial solvency.** **Reason:** available funding and traction statements are historical/company-reported, not current audited financial evidence. [18]

## Key decision facts

- **OBSERVED:** Snapshot is best understood as an actively maintained, MIT-licensed governance toolkit with a mature gasless off-chain mode, a modular on-chain Snapshot X mode, and newer Governor UI support. [1] [3] [4]
- **OBSERVED:** Tally should be treated as a historical execution/UI reference and continuity risk case study; the present successor is Cactus, not a newly verifiable Tally service. [5] [23]
- **INFERRED:** The best fit is to use Snapshot-inspired interfaces and event patterns around a Kimosabe-controlled eligibility, ledger, outreach, and human-accountability layer—not to outsource those layers to a DAO voting portal.

## Sources

[1]: https://docs.snapshot.box/ "Snapshot documentation overview" (accessed 2026-10-06)

[2]: https://docs.snapshot.box/user-guides/delegation "Snapshot documentation: Delegation" (accessed 2026-10-06)

[3]: https://docs.snapshot.box/snapshot-x/protocol/overview "Snapshot X protocol overview" (accessed 2026-10-06)

[4]: https://github.com/snapshot-labs/sx-monorepo "Snapshot `sx-monorepo` repository" (accessed 2026-10-06)

[5]: https://blog.snapshot.box/snapshot-is-now-home-for-governor-daos.md "Snapshot: Governor DAO support and note on Tally" (published 2026-03-19; accessed 2026-10-06)

[6]: https://api.github.com/repos/snapshot-labs/sx-monorepo "GitHub REST metadata: `snapshot-labs/sx-monorepo`" (accessed 2026-10-06)

[7]: https://api.github.com/repos/snapshot-labs/snapshot-v1 "GitHub REST metadata: `snapshot-labs/snapshot-v1`" (accessed 2026-10-06)

[8]: https://github.com/snapshot-labs/snapshot-docs/blob/master/guides/create-a-space.md "Snapshot documentation source: create a Space" (accessed 2026-10-06)

[9]: https://github.com/snapshot-labs/snapshot-docs/blob/master/graphql-api/README.md "Snapshot documentation source: GraphQL API" (accessed 2026-10-06)

[10]: https://github.com/snapshot-labs/snapshot-docs/blob/master/tools/webhooks.md "Snapshot documentation source: webhooks" (accessed 2026-10-06)

[11]: https://github.com/snapshot-labs/snapshot-hub "Snapshot Hub repository" (accessed 2026-10-06)

[12]: https://www.starknet.io/blog/snapshot-x-onchain-voting/ "Starknet: Snapshot X on-chain voting launch" (published 2024-09-09; accessed 2026-10-06)

[13]: https://www.anchorage.com/insights/announcing-snapshot-voting-with-anchorage-digital "Anchorage Digital: Snapshot voting integration" (accessed 2026-10-06)

[14]: https://ethereum.org/developers/tools/snapshot/ "Ethereum.org tool listing: Snapshot" (accessed 2026-10-06)

[15]: https://www.tally.xyz/ "Cactus / Tally current public site" (accessed 2026-10-06)

[16]: https://docs.tally.xyz/user-guides/governance-frameworks/openzeppelin-governor/ "Tally documentation: OpenZeppelin Governor" (accessed 2026-10-06)

[17]: https://docs.openzeppelin.com/contracts/5.x/governance "OpenZeppelin Contracts documentation: governance" (accessed 2026-10-06)

[18]: https://www.businesswire.com/news/home/20250422345730/en/Tally-Raises-%248-Million-Series-A-to-Help-Protocol-Tokens-Accrue-Value "Tally Series A announcement" (published 2025-04-22; accessed 2026-10-06)

[19]: https://www.comp.xyz/t/proposal-tally-as-a-dedicated-governance-service-provider-to-the-compound-dao/6789 "Compound governance forum: proposed Tally governance services" (published 2025-05-22; accessed 2026-10-06)

[20]: https://discuss.ens.domains/t/should-the-dao-have-tally-as-a-dedicated-governance-service-provider/20937 "ENS governance forum: proposed Tally governance services" (published 2025-06-17; accessed 2026-10-06)

[21]: https://github.com/withtally/tally-api-quickstart "Tally API Quickstart repository" (accessed 2026-10-06)

[22]: https://github.com/withtally/tally-zero "Tally Zero repository" (accessed 2026-10-06)

[23]: https://scopelift.co/blog/tally-is-now-cactus "Scopelift: Goodbye Tally, Hello Cactus" (published 2026-06-17; accessed 2026-10-06)

[24]: https://www.tradingview.com/news/cointelegraph:9421935de094b:0-tally-winds-down-citing-lack-of-viable-market-for-dao-tooling/ "Cointelegraph report syndicated by TradingView: Tally wind-down" (accessed 2026-10-06)

[25]: https://api.github.com/orgs/withtally "GitHub REST metadata: `withtally` organization" (accessed 2026-10-06)

[26]: https://api.github.com/repos/withtally/tally-zero "GitHub REST metadata: `withtally/tally-zero`" (accessed 2026-10-06)

[27]: https://api.github.com/repos/snapshot-labs/snapshot-hub "GitHub REST metadata: `snapshot-labs/snapshot-hub`" (accessed 2026-10-06)

[28]: https://api.github.com/repos/snapshot-labs/snapshot-strategies "GitHub REST metadata: `snapshot-labs/snapshot-strategies`" (accessed 2026-10-06)
