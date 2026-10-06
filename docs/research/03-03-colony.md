# Colony — Competitive-intelligence report

**Research access date:** 2026-10-06  
**Claim labels:** **OBSERVED** = directly visible in a primary source at access; **REPORTED** = a source’s claim not independently verified here; **INFERRED** = an evidence-based assessment; **ASSUMED** = a recommendation premise taken from the Kimosabe/Human Blockchain brief.

## What it is, who it serves, and current status

**OBSERVED — Colony is an open-source, EVM-oriented protocol and application for running an organization through smart contracts rather than conventional management paperwork.** Its own documentation describes a colony as contracts for ownership/permissions, reputation, dispute resolution, work/delegation, and financial management. The current commercial-facing site positions the product more narrowly as “DeFi for Teams”: payments, budgets, teams, decision methods, and crypto-to-fiat operations for teams and DAOs. [1] [2]

**OBSERVED — A Colony organization is structured around domains/teams, skills, funding pots, tasks or payments, roles, and reputation.** This makes it aimed at on-chain organizations that need to authorize work and move crypto assets, rather than at civic membership networks, conventional nonprofits, or a marketing CRM. A task can represent a bounty, salary, reimbursement, or incentive. [3] [4]

### Maintenance finding: **DORMANT / low-maintenance in public evidence; not archived**

**OBSERVED — The primary `colonyNetwork` repository is public and not archived, but its latest default-branch commit at access was 2026-03-24 and was a documentation-fix merge.** GitHub reports 446 stars, 117 forks, 53 open issues/PRs, and no archive flag. A pull request was opened on 2026-09-28, which shows at least intermittent external activity but not a merged release. [5] [6] [23] [24]

**OBSERVED — Supporting projects show uneven upkeep.** The current `colonyJS` library was not archived and its latest default-branch commit was a package release on 2025-01-30. The current Dapp repository was not archived; its latest default-branch commit was a README deployment note on 2025-12-10, while API metadata shows a 2026-03-30 push on some branch. The older standalone `colonySDK` repository is explicitly archived and points users to the SDK in `colonyJS`. [7] [8] [9] [25] [26]

**OBSERVED — The most recent GitHub release listed for `colonyNetwork` was published 2020-04-08, although the code repository has later commits and the official website still advertises a live product.** The official blog contains product announcements dated December 2024 in search results; the public pages accessed do not establish releases or production changes after that. [6] [10] [11]

**INFERRED — Classify Colony as dormant/low-maintenance, not as an actively maintained dependency.** The code is not archived and a recent open PR exists, but there is no recent merged substantive default-branch change, recent GitHub release, or current independently measurable user/deployment data in the evidence reviewed. Private development or unobserved production changes remain **unverified**, so this is a public-evidence classification rather than a claim that the network is unavailable.

## License and primary repository

**OBSERVED — Primary repository:** [github.com/JoinColony/colonyNetwork](https://github.com/JoinColony/colonyNetwork). It contains the Colony Network smart contracts, defaults to the `develop` branch, and is licensed **GNU GPL v3.0 (GPL-3.0)**. [5]

**OBSERVED — Related source surfaces:** `JoinColony/colonyJS` is the GPL-3.0 TypeScript monorepo containing `@colony/sdk`, reference libraries, event/types and contract bindings; `JoinColony/colonyCDapp` is the Dapp repository but its GitHub metadata has no detected license. The JoinColony organization reports 102 public repositories. [7] [8] [12]

## Adoption and activity signals

- **OBSERVED:** `colonyNetwork` had **446 GitHub stars, 117 forks, and 53 open issues/PRs** on 2026-10-06; these are developer-interest signals, **not** active-user, treasury-volume, or production-security measures. [5]
- **OBSERVED:** `colonyJS` had **92 stars and 25 forks**; the archived legacy `colonySDK` had **63 stars and 28 forks**; `colonyCDapp` had **7 stars and 13 forks**. [7] [8] [9]
- **REPORTED (by Colony):** ShapeShift has used Colony to pay contributors “for many years.” Colony’s December 2023 V3 post also named Telefonica and ShapeShift as committed users. Neither claim was independently verified in this review, and neither establishes current use in 2026. [11] [13]
- **REPORTED (by Alchemy directory):** Alchemy lists Colony as a no-code DAO toolkit. This provides independent ecosystem visibility but is a directory profile, not an audit or a verified adoption metric. [14]
- **UNVERIFIED:** No authoritative, current public count of active colonies, active members, transaction volume, assets under management, paid customers, or software installs was found in the reviewed primary material. Do not substitute GitHub stars or marketing examples for those measures.

## Core capabilities

### Work, contribution, and payouts

**OBSERVED — Tasks are an on-chain work primitive.** A task includes a brief/specification, deliverable reference, due date, payout(s), domain, and skill tags. It has three task-specific roles: **Manager** (normally task creator/acceptor), **Worker** (does the work), and **Evaluator** (independently assesses work). Important changes need multiple role signatures; workers submit deliverables, then manager/worker ratings use commit-and-reveal. [4]

**OBSERVED — Payments are the lighter-weight primitive.** A payment transfers tokens from a domain pot to an external account without the task’s on-chain work-management workflow. A payout in the colony’s internal token can confer reputation. [4]

**OBSERVED — The public product currently markets batch payments from CSV, streaming salaries, equal/custom/reputation-based splits, staged milestone payments, and crypto-to-fiat payments.** The homepage states a 1% off-ramping fee for the last of these. An official staged-payments post says funds are allocated in smart contracts upfront, with the colony retaining release control by milestone. These are provider claims; the examples and reliability of the workflows were not independently tested. [2] [15]

### Organizational structure, skills, and reputation

**OBSERVED — Domains compartmentalize work and resources like departments; skills classify work independently of a particular domain.** A domain receives an associated funding pot. The protocol’s global skills are curated by Meta Colony; reputation earned in one colony does not transfer as reputation to another. [3] [16]

**OBSERVED — Reputation is designed as non-transferable, contribution-linked influence.** It can be gained or lost through task completion, disputes, or reputation mining and has an approximately 3.5-month half-life. The documentation says task/domain creation, objections/disputes, and collective decisions require both tokens and reputation. [3]

**OBSERVED — Official sources are internally inconsistent on hierarchy.** The current marketing site says Colony has nested teams, while the contract interface documentation says `addDomain` is currently restricted to one level below the root domain. A 2021 roadmap described nested teams as a future feature. **UNVERIFIED:** whether the deployed production configuration now supports the nested hierarchy advertised on the homepage. [2] [9] [17]

## Governance model

**OBSERVED — Meta Colony is the special colony intended to develop, support, and grow the network.** Its members can earn/hold CLNY and Meta Colony reputation. Membership is described as open to all, but network upgrades require a minimum Meta Colony reputation. Meta Colony also has control over global skill tags. [1] [16]

**OBSERVED — Colony’s signature decision pattern is “lazy consensus.”** In the published roadmap, a proposer stakes on a Motion; if no one objects during a security delay, the action executes. An objection triggers a vote. The Safe-control implementation says its motion process uses native-token staking and a reputation-based voting period when objected to. [17] [18]

**OBSERVED — Reputation, not merely capital, is intended to weight participation.** In the task model, work ratings change reputation; in governance, reputation is the stated basis for the vote after an objection. The 2021 roadmap also described token-only and hybrid token/reputation governance as future modules. Treat those roadmap items as **REPORTED plans**, not confirmation of current general availability. [3] [17] [18]

**REPORTED — An independent 2018 legal/organizational case study characterized Colony as a proposed system in which high-quality work yields governance power, potentially useful for globally distributed worker cooperatives.** Because the paper studied the project’s then-design, it supports the conceptual model but does not validate current software maturity, outcomes, or fairness. [19]

## Membership, roles, delegation, and recruiting mechanics

**OBSERVED — Colony has two separate role layers.** Task roles allocate a discrete job among manager, worker, and evaluator. Contract-level roles/permissions allocate authority within domains; the `IColony` interface exposes `setUserRoles` and permission-domain parameters, and its documentation says an extension can call the colony “operating system” functions if the caller has permission. [4] [9]

**OBSERVED — Delegation is bounded by domain and permission rather than by a conventional reporting chart.** Domains create budget/work compartments; task roles delegate delivery and assessment; multi-signature requirements constrain sensitive task changes. This is a practical delegation mechanism for funded work, not a full human-resources system. [3] [4]

**OBSERVED — Meta Colony is open to membership according to its documentation, but there is no documented recruiting funnel in the reviewed protocol materials.** The sources did not establish application forms, referrals, background checks, identity verification, CRM pipelines, geographic eligibility, anti-Sybil controls for civic membership, or candidate communications. Those capabilities are therefore **UNVERIFIED / absent from the reviewed public documentation**, not assumed to exist. [1] [16]

**INFERRED — Colony can make a contributor’s work/payout record legible after onboarding, but it is not a substitute for recruiting, volunteer activation, marketing automation, community moderation, or county-level constituent relationship management.** Wallet and role assignment are not a public-benefit onboarding program.

## Treasury and fund management

**OBSERVED — Colony segregates funds into funding pots.** At minimum it reserves a rewards pot and working-capital pot. Domains and tasks can have associated pots, and contract functions expose pot balances, allocated payouts, movement of funds, and reward payouts. [3] [9]

**OBSERVED — It can govern an attached Safe multisig through a Safe module.** A motion can propose transfers, NFT transfers, contract calls, or raw transactions; it follows lazy consensus and, if unopposed, can execute after the process described by Colony. This is a treasury-control feature, not proof of any particular Safe configuration’s security. [18]

**OBSERVED — Colony’s protocol documentation describes a network-fee model.** Meta Colony collects a small fee when a task payout is claimed. For non-whitelisted tokens, the source says the token goes to an auction contract and is sold for CLNY, which is burned. The organization’s current public pricing also says colonies have no creation/monthly fees but that a small percentage applies to selected transactions. The exact live fee schedule, whitelists, and whether every historical token mechanism remains enabled are **UNVERIFIED**. [2] [16]

**OBSERVED — CLNY is Meta Colony’s token.** The docs state that accounts holding both CLNY and Meta Colony reputation may claim revenue share proportional to combined holdings, and CLNY is used as a stake for reputation mining. This is crypto-economic treasury infrastructure, not a fiduciary public-benefit fund-management model. [16]

## Hosting model, APIs, and extension surfaces

**OBSERVED — The core protocol is public smart contracts intended for direct use by applications.** The developer portal offers direct smart-contract integration, `colonyJS`, and boilerplates; the TypeScript monorepo packages include `@colony/sdk`, `@colony/colony-js`, core types, event parsing, token bindings, and generated contract bindings. [12] [7]

**OBSERVED — The Dapp is not purely clientless in every mode.** Its repository says it supports a fully decentralized mode and a metadata-caching-layer mode. Its local developer setup includes an Amplify/AppSync GraphQL playground and lambda functions. A 2023 V3 post explicitly says Colony moved to a hybrid architecture for performance/stability while retaining a feature-limited fully decentralized option as a security backstop. [8] [11]

**OBSERVED — The public homepage says governance runs Arbitrum-based while the organization can control assets/contracts across most EVM-compatible chains.** The older SDK README uses Gnosis Chain in its example. **UNVERIFIED:** a complete, current production chain/support matrix, cross-chain security assumptions, and an SLA for any hosted layer. [2] [20]

**OBSERVED — Extension architecture exists, but support status needs verification.** The smart-contract architecture documentation names extension factories and lists OldRoles and OneTxPayment as officially supported. However, the latest GitHub release notes available say OldRoles was deprecated. Do not treat either as a current supported plugin commitment without a compatibility test and maintainer confirmation. [21] [6]

**UNVERIFIED — No documented, general-purpose public REST administration API, webhook system, CRM connector catalog, or off-chain governance forum was established by the sources reviewed.** The contract API and TypeScript SDK are the dependable integration surfaces identified here.

## Business model and funding

**OBSERVED — Current listed pricing is freemium/transaction-fee oriented rather than subscription oriented:** free colony creation, no upfront or monthly subscription fee, no stated user/team/transaction caps, gas covered on Arbitrum, selected transaction percentage fees, and a stated 1% crypto-to-fiat off-ramp fee. [2]

**OBSERVED — The network design also contemplated recurring protocol revenue via task-payout fees for Meta Colony.** That design is a distinct incentive layer from the present commercial app pricing and should not be conflated with audited business revenue. [16]

**OBSERVED — In a 2017 official post, Colony said it cancelled its planned token sale before the network was live and would continue funding development privately.** This is historical evidence only. **UNVERIFIED:** current equity/token financing, investors, revenues, operating entity, runway, paid customer count, and whether a later financing/token distribution took place. Do not repeat third-party claims of a 2017 completed Colony token sale: that conflicts with Colony’s contemporaneous primary statement. [22]

## Strengths

- **OBSERVED:** A coherent contribution-to-work-to-payout-to-reputation loop, with explicit task specification, separated evaluator role, commit/reveal ratings, and auditable smart-contract state. [4]
- **OBSERVED:** Fine-grained resource compartmentalization through domains, skills, pots, and role-scoped permissions; this maps naturally to teams with separate budgets. [3] [9]
- **OBSERVED:** Lazy-consensus escalation avoids a vote on every operational action while retaining an objection/vote path for contested actions. [17] [18]
- **OBSERVED:** Multiple payout primitives—batch, stream, split, staged, and Safe-governed transactions—are closer to operations tooling than a bare voting DAO. [2] [15] [18]
- **OBSERVED:** Open-source GPL contracts, direct contract APIs, a TypeScript SDK, and a documented hybrid/decentralized posture provide inspectable integration options rather than a wholly closed SaaS. [5] [7] [11]
- **INFERRED:** The separation of contribution reputation from transferable tokens is a useful governance design pattern when a network wants labor/contribution to matter independently from capital.

## Gaps and unresolved weaknesses

- **OBSERVED:** Public maintenance signals are weak/uneven: the legacy SDK is archived, the TypeScript SDK’s latest default-branch commit is January 2025, the primary repository’s latest default-branch commit is a March 2026 documentation fix, and the latest listed GitHub release is from 2020. This materially raises integration, incident-response, and dependency-risk questions. [5] [6] [7] [8]
- **OBSERVED:** Official sources conflict on at least two operational points—nested-domain availability and OldRoles extension support/deprecation. A network contemplating adoption would need a deployment-level test plan, not reliance on marketing copy. [2] [6] [9] [17] [21]
- **INFERRED:** A 3.5-month reputation half-life can encourage recurring engagement, but it can also disadvantage seasonal, caregiving, rural, or intermittently connected participants unless there are transparent exceptions and appeal rights. [3]
- **INFERRED:** Token staking to object or participate can deter low-resource contributors and converts part of governance access into an economic-capacity question. This is misaligned by default with equal-access public-benefit participation. [3] [17] [18]
- **INFERRED:** Wallet-based, public-chain financial workflows introduce usability, custody, fraud, privacy, tax/accounting, sanctions/AML, consumer-protection, and U.S. legal/compliance work that a public-benefit operator cannot outsource to a smart contract. No legal conclusion is offered here.
- **OBSERVED / INFERRED:** The reviewed sources do not document county residency/eligibility checks, one-person-one-account controls, protected-class safeguards, consent management, participant data portability/deletion, multilingual onboarding, constituent communications, moderation, or formal appeals. These are material missing operational surfaces for a U.S. county-level stakeholder network.
- **UNVERIFIED:** Smart-contract audit status, current audited deployments, bug-bounty status, production availability, customer-support commitments, and current terms/privacy/governance forum practices were not established in the reviewed sources. They require separate due diligence before handling money or consequential governance.

## Relevance to a Kimosabe/Human Blockchain marketing, recruiting and management organization

**ASSUMED — The target organization is a new U.S. public-benefit operator for marketing, recruiting, promotion, community management, and governance operations across county-level stakeholder groups, seasonal community credits, a General Ledger, and a claim/conversion loop.** On that premise, Colony is most useful as a source of **governance and work-accounting patterns**, not as the target organization’s core stack or public-facing membership system.

### ADOPT

1. **ADOPT the domain/team + scoped-budget pattern.** Model county, stakeholder group, program, campaign, or season as a permissions-and-budget scope, with a clear parent-child authorization ledger. This provides accountable local autonomy and makes General Ledger allocations explainable. Do not assume Colony itself supplies the required county hierarchy; its documentation conflicts on nesting. [2] [3] [9]
2. **ADOPT the task brief, deliverable, manager/worker/evaluator separation, and milestone-release pattern.** Use it for promotional campaigns, recruiting cohorts, community-manager assignments, and claims review: define acceptance criteria before work begins; separate the person executing, approving, and independently checking high-risk work; release funds/credits only against documented milestones. [4] [15]
3. **ADOPT transparent earmarked funds and payout-state visibility.** A General Ledger should expose authorized, allocated, released, returned, and disputed balances per program, with access controls appropriate to sensitive data. Colony’s funding-pot concept is a strong conceptual model. [3] [9]

### ADAPT

1. **ADAPT reputation into a non-financial, season-aware contribution record.** Make rules published, evidence-backed, contestable, time-bounded, and separately measured by relevant stakeholder group. Preserve a participant’s historical record even if current-season governance influence changes. Do not copy the 3.5-month decay rule unchanged; test its equity effects first. [3]
2. **ADAPT lazy consensus into a public-notice-and-escalation process.** Routine, low-risk operations can proceed after a visible notice period if there is no qualified objection; spending, rule changes, eligibility decisions, conflicts of interest, and appeals should have explicit human review, records retention, and accessible objection channels. Do not require a crypto stake to be heard. [17] [18]
3. **ADAPT roles as least-privilege operational delegations.** Use separate campaign manager, contributor, verifier/evaluator, fund approver, data steward, and appeals reviewer authorities. Add term limits, disclosures, audit logs, recusal, and revocation workflows beyond Colony’s on-chain permission model. [4] [9]
4. **ADAPT the claim/conversion loop to verifiable operational evidence.** A claim should be a structured record with source/proof, reviewer, decision, appeal date, geographic/stakeholder scope, and ledger impact—not merely a transaction or reputation event.

### REJECT

1. **REJECT adopting CLNY-style transferable-token economics, token-gated objections, revenue sharing, and protocol-fee auctions as the public-benefit organization’s default governance.** They introduce capital-based influence, speculative incentives, and regulatory/financial complexity that do not advance equitable county-level recruiting or community management. [16] [18]
2. **REJECT using Colony as the system of record for identities, recruiting, marketing, moderation, civic eligibility, or sensitive participant data.** The reviewed documentation establishes smart-contract work/treasury primitives and wallets, not consentful U.S. public-benefit CRM, case management, or privacy controls.
3. **REJECT a single opaque reputation score as the determinant of governance weight, access, or rewards.** Contributions across marketing, care, outreach, local knowledge, and governance cannot be safely normalized without transparency, human review, anti-bias controls, and a real appeal route.

### DEFER

1. **DEFER any direct Colony protocol/SDK/Dapp dependency or EVM deployment.** Reconsider only after independent verification of deployed contracts, releases, audits, support commitments, license implications, security posture, and a maintained fork strategy. Current public evidence supports a dormant/low-maintenance classification. [5] [6] [7] [8]
2. **DEFER Safe control, crypto-to-fiat, wallet custody, and any real-money payout path.** Enable only after fiduciary controls, dual authorization, local/state/federal legal review, vendor due diligence, reconciliation, fraud response, tax/accounting treatment, and user-support capacity are in place. [2] [18]
3. **DEFER importing Meta Colony’s network-fee/reward design.** First demonstrate that the Kimosabe network’s seasonal credits, General Ledger, and claim conversion rules are understandable, non-extractive, and auditable without creating a tradeable asset or requiring economic staking. [16]

**Decision:** **Use Colony as a pattern library, not as a foundation dependency.** Its strongest transferable ideas are scoped work/budgets, evaluated contribution records, staged allocations, and proportionate escalation. Its crypto-economic, identity-light, and low-maintenance characteristics make it a poor direct platform for the proposed public-benefit organization.

## Source-quality and verification notes

**OBSERVED:** Primary sources dominate factual claims: Colony documentation, official blog, current website, and live GitHub API/repositories. The 2018 independent academic case study is used only for historical/conceptual corroboration, because it explicitly studies Colony’s then-proposed design. [19]

**OBSERVED:** Alchemy’s directory is a credible ecosystem listing but not a due-diligence report. A separate commercial comparison page reviewed during research stated that Colony completed a 2017 token sale; this conflicts with Colony’s contemporaneous announcement that it cancelled that sale, so it was not relied on for funding or chronology. [14] [22]

**UNVERIFIED:** This report did not independently execute contracts, create a colony, inspect on-chain deployment state, validate user testimonials, or audit code. It does not establish present availability, security, legal compliance, or financial performance.

## Sources

[1]: https://docs.colony.io/next/colonynetwork/ "Colony Network official documentation (accessed 2026-10-06)"

[2]: https://colony.io/ "Colony official homepage and pricing/features (accessed 2026-10-06)"

[3]: https://docs.colony.io/next/develop/dev-learning/feature-overview/ "Colony official feature overview (accessed 2026-10-06)"

[4]: https://docs.colony.io/colonynetwork/tldr/tasks "Colony official tasks and payments documentation (accessed 2026-10-06)"

[5]: https://api.github.com/repos/JoinColony/colonyNetwork "GitHub API — JoinColony/colonyNetwork metadata (accessed 2026-10-06)"

[6]: https://api.github.com/repos/JoinColony/colonyNetwork/releases?per_page=10 "GitHub API — colonyNetwork releases (accessed 2026-10-06)"

[7]: https://api.github.com/repos/JoinColony/colonyJS "GitHub API — JoinColony/colonyJS metadata (accessed 2026-10-06)"

[8]: https://api.github.com/repos/JoinColony/colonyCDapp "GitHub API — JoinColony/colonyCDapp metadata (accessed 2026-10-06)"

[9]: https://docs.colony.io/next/colonynetwork/interfaces/icolony/ "Colony IColony interface documentation (accessed 2026-10-06)"

[10]: https://blog.colony.io/ "Colony official blog index (accessed 2026-10-06)"

[11]: https://blog.colony.io/upcoming-colony-v3/ "Colony V3 beta official announcement (accessed 2026-10-06)"

[12]: https://github.com/JoinColony "JoinColony GitHub organization page (accessed 2026-10-06)"

[13]: https://blog.colony.io/how-shapeshift-uses-colony/ "Colony official ShapeShift use-case post (accessed 2026-10-06)"

[14]: https://www.alchemy.com/dapps/colony "Alchemy third-party Colony directory profile (accessed 2026-10-06)"

[15]: https://blog.colony.io/staged-payments/ "Colony official staged-payments announcement (accessed 2026-10-06)"

[16]: https://joincolony.github.io/colonynetwork/whitepaper-tldr-the-meta-colony-and-clny/ "Colony official Meta Colony and CLNY documentation (accessed 2026-10-06)"

[17]: https://blog.colony.io/roadmap "Colony official 2021 roadmap and governance description (accessed 2026-10-06)"

[18]: https://blog.colony.io/new-feature-fully-control-a-multi-sig-safe-with-a-dao/ "Colony official Safe-control governance announcement (accessed 2026-10-06)"

[19]: https://papers.ssrn.com/sol3/Delivery.cfm/SSRN_ID3356774_code1344173.pdf?abstractid=3356774&mirid=1 "Morshed Mannan, Fostering Worker Cooperatives with Blockchain Technology: Lessons from the Colony Project, Erasmus Law Review (2018) (accessed 2026-10-06)"

[20]: https://github.com/JoinColony/colonySDK "JoinColony legacy SDK repository README (accessed 2026-10-06)"

[21]: https://joincolony.github.io/colonynetwork/docs-overview/ "Colony Network smart-contract architecture documentation (accessed 2026-10-06)"

[22]: https://blog.colony.io/the-colony-token-sale-7ac14c845bc0 "Colony official 2017 token-sale cancellation post (accessed 2026-10-06)"

[23]: https://api.github.com/repos/JoinColony/colonyNetwork/commits/develop "GitHub API — latest colonyNetwork develop commit (accessed 2026-10-06)"

[24]: https://api.github.com/repos/JoinColony/colonyNetwork/issues?state=open&per_page=1 "GitHub API — latest visible open colonyNetwork pull request (accessed 2026-10-06)"

[25]: https://api.github.com/repos/JoinColony/colonyJS/commits/main "GitHub API — latest colonyJS main commit (accessed 2026-10-06)"

[26]: https://api.github.com/repos/JoinColony/colonyCDapp/commits/master "GitHub API — latest colonyCDapp master commit (accessed 2026-10-06)"
