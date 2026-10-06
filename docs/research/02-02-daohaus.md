# DAOhaus (Moloch v3 / Baal) — Competitive-Intelligence Brief

## Identity, audience, and code provenance

**OBSERVED.** DAOhaus is an open-source, community-owned toolkit for creating and operating purpose-driven DAOs. Its current site describes the project as a protocol for purpose-driven governance and public goods. The product layer makes the Moloch model usable through an Admin application; its protocol layer is **Baal**, the code name for Moloch v3. Baal is a governance contract layer over a multisignature treasury, using Zodiac to interface with Safe. It is meant for groups that need to pool crypto assets, allocate membership power, vote on actions, and preserve an on-chain exit right. [1] [2] [3]

**OBSERVED.** The stated target is broad but specific in operating model: guilds, venture clubs, and “control panels” are named in the Baal repository. DAOhaus’s own framing is purpose-driven communities rather than consumer social networks, conventional membership associations, or government bodies. [3] [4]

**OBSERVED — primary protocol repository and license.** The appropriate primary protocol repository is [Moloch-Mystics/Baal](https://github.com/Moloch-Mystics/Baal), which labels itself the Moloch v3/Baal template. GitHub’s API reports **GPL-3.0**, 96 stars, 55 forks, and no archive flag as of **2026-10-06**. [4] [5]

**OBSERVED — licensing is split, not unitary.** The historic DAOhaus monorepo is **MIT**-licensed; it contains apps, data libraries, UI components, feature libraries, subgraphs, and infrastructure jobs. The new `HausDAO/daohaus-admin` repository’s GitHub API entry has `license: null`; it is publicly visible, but reuse rights for that repository are therefore **UNVERIFIED** and should not be assumed. This distinction matters: do not treat “DAOhaus is open source” as permission to copy every current frontend asset. [6] [7] [8]

## Adoption and maintenance signals

**REPORTED (historical, not a current count).** In a DAOhaus-authored Optimism governance proposal, the team reported, at the time of that proposal, 100 DAOs, 13,000 proposals, more than 10,000 members, and $416 million of “Total Value Flow.” The post also said DAOhaus had deployed in August 2020. These are self-reported historical metrics, not independently revalidated current usage, and should not be presented as today’s adoption. [9]

**REPORTED (historical third-party).** Decrypt reported the February 2022 Moloch v3/Baal launch, stated the prior Moloch framework had been forked 697 times, and named MetaCartel Ventures, The LAO, Raid Guild, Meta Gamma Delta, and CyberFM as Moloch users. That supports historical lineage and recognition, not live DAOhaus v3 usage. [10]

**OBSERVED (maintenance, access date 2026-10-06).** The project is **not simply archived**: the public `HausDAO/daohaus-admin` repository is not archived, was pushed on **2026-10-01**, and its head commit on `master` is dated **2026-09-03**. The current `moloch-skills` integration repository was last committed **2026-05-11**. The DAOhaus user guide’s head commit was **2026-05-04**. These indicate contemporary maintenance of the interface, documentation, and Base-oriented tooling. [7] [11] [26] [27]

**OBSERVED (core-protocol caution).** Core Baal is much less active: its default branch head is a **2022-09-12** audit-update merge, although the repository had a later `pushed_at` timestamp of **2024-06-11**. The historic monorepo README itself says it has been “packed away in the attic—not actively maintained,” even though GitHub records a `develop`-branch commit on **2026-04-30**. [5] [6] [13]

> **Maintenance verdict — INFERRED:** DAOhaus is **selectively active / maintenance-mode**, not archived overall. The current Admin application and operational tooling show activity, while the canonical Baal contract code looks **mature and dormant rather than actively evolving**. Treat Baal as a stable dependency that requires independent security review and change-control ownership; do not assume a fast upstream patch cadence.

**OBSERVED.** Public popularity signals are modest rather than mass-market: 96 stars/55 forks for Baal, 25 stars/18 forks for the historic monorepo, and 0 stars/1 fork for the 2026 Admin repository at access. No verified current install, active-DAO, treasury-TVl, revenue, or user count was found in the reviewed first-party sources. [5] [6] [7]

## Core capabilities and governance mechanics

**OBSERVED.** Baal separates governance from custody. Baal manages the proposal lifecycle, governance configuration, shaman permission state, and ragequit execution; a Safe holds assets and executes approved multicalls. This allows a DAO either to summon a Safe with the DAO or attach Baal governance to an existing Safe. [1] [2]

**OBSERVED.** The Admin guide exposes signal votes, member/token requests, token swaps, ERC-20 and native-token transfers, governance and token-setting changes, Shaman management, member removal, WalletConnect contract interaction, and an arbitrary multicall proposal builder. A passed multicall can batch contract actions. Thus Baal is an execution-governance primitive, not merely a polling product. [14]

**OBSERVED.** Configuration includes voting and grace periods, quorum, minimum retention, a sponsor threshold, and a proposal offering. The grace period is specifically intended to give dissenters time to ragequit after voting but before execution. Minimum retention auto-fails a proposal if a configured share of the DAO has exited. A member meeting the sponsor threshold auto-sponsors a proposal; a proposal offering can deter spam. [15] [16]

**OBSERVED.** The model splits membership into ERC-20-compatible **Shares** (voting plus exit rights) and **Loot** (exit-only, non-voting economic rights). DAO tokens can be made transferable, although the summon guide recommends starting non-transferable. This permits a useful distinction between decision makers, contributors, grantees, and economic beneficiaries, but it is token-weighted rather than one-person-one-vote. [3] [16]

## Membership, roles, delegation, and recruiting

**OBSERVED.** Admission is proposal-driven. An organizer or candidate files a DAO Token Request containing the prospect’s wallet address and requested voting Shares and/or non-voting Loot. After a successful vote and grace period, the specified tokens transfer to the recipient and make that address a member. Membership data includes join date, power, voting and non-voting balances, and delegation destination. [12] [14]

**OBSERVED.** A holder may delegate voting Shares to another member. Member-management tools also expose a “Guild Kick” flow; the v3 proposal guide defines removal as changing a member’s voting tokens into non-voting tokens. A member may ragequit and withdraw the displayed pro-rata exit amount, but a member with a “Yes” vote on an open proposal cannot exit at that point. [12] [17] [14]

**OBSERVED.** Baal uses three permission categories for **Shamans**—Admin, Manager, and Governor—individually or in combination. Admin can change token transferability; Manager can mint/burn Shares and Loot; Governor can change governance parameters and cancel proposals in the voting period. Shamans are external contracts approved through a DAO proposal. DAOhaus warns that Shamans can make critical changes outside the ordinary proposal process and that a leaked Shaman key can enable damaging administrative actions; it recommends contract-based, not EOA-based, Shamans. [18] [4]

**OBSERVED.** Extension examples show recruiting/onboarding patterns but not a full recruiting system. `OnboarderShaman` can exchange ETH for Shares or Loot; a `ClaimShaman` can allow NFT holders to claim membership tokens; a Community Veto pattern lets Loot holders stake against a proposal during voting. These examples are in repositories described as a playground/experimental configurations, so production readiness is **UNVERIFIED**. [19] [20]

**OBSERVED / REPORTED.** DAOhaus described Yeeter as a trust-minimized public-goods fundraising tool in its Optimism proposal. The currently visible `yeet-haus/contracts` repository describes Yeeter contracts as based on DAOhaus Baal Shaman and Higher Order Summoner contracts and includes `EthYeeter`. This validates the composable crowdfunding pattern. It does **not** verify a currently maintained hosted Yeeter service, campaign adoption, regulatory suitability, or fiat fundraising support. [9] [21]

## Treasury and fund management

**OBSERVED.** One DAO can use one ragequittable main Safe plus multiple non-ragequittable sidecar Safes. The main Safe holds on-chain assets, including native coins, ERC-20, ERC-721, ERC-1155, and veTokens; proposals execute through Safe multicall. The sidecar pattern is the key mechanism for separating an exit-eligible common pool from assets that must not be subject to pro-rata withdrawal. [21]

**INFERRED.** For a Kimosabe operating organization, that split is more valuable than a single undifferentiated treasury: a member-contributed/seasonal-credit reserve can remain separately auditable and subject to narrowly scoped redemption rules, while grant-restricted, payroll, tax, contractual, or legally encumbered funds should not be placed into an automatic ragequit pool. The governing policy, legal ownership, and accounting treatment must be designed independently; Baal does not provide them.

**OBSERVED.** Ragequit protects a dissenting token holder by burning Shares and/or Loot for a pro-rata exit claim before a disputed action executes. The independent Gitcoin mechanism review identifies the trade-off: ragequit can drain a treasury under repeated contentious decisions, proposal/grace periods slow decisions, and wealthier contributors can hold more voting power. Its statement that Moloch lacks delegation applies to original MolochDAO, **not** DAOhaus v3, whose guide documents delegation. [17] [22]

**UNVERIFIED.** “Household” treasury/accounting patterns were not documented in the reviewed official DAOhaus/Baal materials. Do not attribute a household ledger, earmarked family fund, statutory accounting, budget controls, banking, payroll, KYC/AML, tax reporting, or a general ledger to DAOhaus without separate evidence.

## Hosting model, APIs, and extension surfaces

**OBSERVED.** There is a hosted Admin instance at `https://admin.daohaus.club/`, but self-hosting is technically feasible: the new Admin is a Vite/React app that can be installed and run locally. Its documented configuration requires WalletConnect, The Graph, Alchemy, Etherscan, and Gnosis Safe API keys; Sequence is optional. This is a web3 application stack, not a turnkey jurisdictional SaaS. [23] [24]

**OBSERVED.** The integration surface is substantial but developer-oriented: Solidity contracts/ABIs, Safe/Zodiac modules, Shamans, Higher Order Summoners, contract calldata/multicalls, a The Graph subgraph, IPFS/Poster metadata records, and React/data/UI libraries. The historic monorepo states it includes UI apps, data libraries that wrap contracts/subgraphs/data sources, and reusable UI/feature libraries. [13] [19] [23]

**OBSERVED.** Current Base-oriented skills document direct RPC reads/writes and a Graph gateway endpoint for indexed DAO/proposal/member data. They distinguish lag-prone indexed Graph reads from current contract reads, advise re-reading direct state before a write, and explicitly state that the tools do not manage key rotation, spending limits, multisig custody, or simulation for high-value actions. [23]

**INFERRED.** No stable, general-purpose REST API or complete enterprise integration contract was identified in the reviewed sources. The practical “API” is a mix of EVM contracts, GraphQL indexing, provider APIs, wallet signing, and source-level libraries. Kimosabe should therefore put a domain API and event/data warehouse between these primitives and its county-facing application; no critical workflow should depend directly on an unversioned third-party UI or a Graph indexer.

## Business model and funding

**REPORTED (historical).** DAOhaus’s 2021 official HAUS launch post says it had been funded by grants and community contributions. It describes Community Contribution Offerings, Loot used to seed working capital, transmutation into HAUS as funds were spent, and a community treasury allocation. It also describes a core DAO of about 20 remote contributors, value-provided compensation rather than salaries, and functional circles including technical builders, communicators, economic/governance designers, and operational leads. [25]

**REPORTED (historical request, not award confirmation).** In 2022 DAOhaus requested 350,000 OP from Optimism. Its requested allocation earmarked 80% for builder incentives, 13% for marketing/operations/DevRel/support, and 7% for deployment of Moloch v3 contracts. This is credible evidence of a grant-funded public-goods operating strategy and explicit recognition that marketing and community support need resources. It is **not evidence that the grant was awarded**, nor proof of current runway. [9]

**OBSERVED.** The current site calls DAOhaus “free and open,” and the Optimism proposal called the no-code platform open and free to use. No current paid plan, transaction-fee schedule, enterprise contract, recurring revenue disclosure, or current funding ledger was verified in the reviewed sources. [1] [9]

> **Business-model conclusion — INFERRED:** DAOhaus is best read as public-goods/open-source infrastructure historically financed by community capital and grants, not as a proven recurring-revenue operating-services company. A Kimosabe organization should not copy its funding model without a durable operating budget, legal entity, reserves policy, and non-token revenue plan.

## Strengths

- **OBSERVED — credible minority protection.** The grace-period/ragequit combination makes the consequence of a majority decision economically visible and gives dissenters a programmatic exit path. [15] [17]
- **OBSERVED — composable custody/governance split.** Layering Baal governance on Safe/Zodiac avoids rebuilding a treasury wallet and permits an existing Safe to gain DAO governance. [2] [3]
- **OBSERVED — useful participation tiers.** Shares versus Loot, delegation, token transferability controls, and proposal-based admissions support separate voting, contribution, and economic-rights design. [3] [12] [16]
- **OBSERVED — deep execution surface.** Multicall and Shaman/Higher Order Summoner patterns can automate controlled operations beyond simple polling. [14] [19]
- **OBSERVED — operational transparency.** Proposals expose lifecycle state, votes, execution transaction links, and call data; the newer tooling can read indexed history and post IPFS/Poster-linked metadata. [14] [23]
- **REPORTED — public-goods operating lessons.** The historical CCO, contributor-circle, and incentive approach shows DAOhaus recognized the need to finance builders, communications, and operations rather than treating governance software as self-operating. [9] [25]

## Gaps and unresolved weaknesses

- **OBSERVED.** The main Baal branch’s 2022 head commit and the historic monorepo’s own “attic” notice create upstream-maintenance and dependency risk, despite current Admin activity. [5] [13]
- **OBSERVED.** Shaman permissions deliberately bypass the standard proposal path for key actions; poor permission design or signer/contract compromise can undermine governance. [18] [4]
- **OBSERVED / INFERRED.** Arbitrary contract calls and multicalls are powerful but difficult for nontechnical members to review. The current skills warn that gas estimation is not full simulation and that high-value transactions should be simulated separately. [14] [23]
- **OBSERVED / REPORTED.** Ragequit is not a universal fairness control: it can deplete a pooled treasury, makes slow governance more likely, and cannot reverse already executed actions. A `Yes` voter on an open proposal loses the immediate exit option. [17] [22]
- **INFERRED.** Token-weighted governance is a poor direct fit for U.S.-county stakeholder legitimacy where residency, service, role, consent, and territorial accountability may matter more than capital stake. DAOhaus provides no verified identity, residency, credentialing, conflict-of-interest, or geographic-jurisdiction layer.
- **INFERRED.** DAOhaus is not a marketing, CRM, recruiter pipeline, event/promotion, case-management, community-support, analytics, general-ledger, or seasonal-credit platform. Its member list and on-chain profiles are useful audit primitives, not a complete community-operations system.
- **UNVERIFIED.** No reviewed source establishes legal compliance for securities, charitable solicitation, consumer protection, public-benefit governance, payroll, tax, records retention, or the Kimosabe claim/conversion game loop. Professional legal, tax, security, accessibility, and privacy design remains required.
- **OBSERVED.** License posture complicates a direct fork: Baal is GPL-3.0, the old monorepo is MIT, and the active Admin source has no declared license in GitHub’s API. [5] [6] [7]

## Relevance to a Kimosabe/Human Blockchain marketing, recruiting and management organization

### ADOPT

- **ADOPT — proposal lifecycle with a visible grace/review stage [INFERRED].** Use a human-readable lifecycle—draft, sponsored, voting, challenge/review, executed/failed—with immutable action records. This fits promotion budgets, county-program approvals, partner onboarding, and grant disbursements, but it should be implemented in an original Kimosabe interface and policy framework rather than copied UI.
- **ADOPT — separation of voting authority from non-voting contribution recognition [INFERRED].** Baal’s Shares/Loot distinction is a strong design pattern for separating county stakeholder governance from earned seasonal community credit, volunteer recognition, or benefit eligibility. Keep all Kimosabe rules human-legible and subject to legal review; do not assume an ERC-20 implementation is needed.
- **ADOPT — scoped treasury compartments [INFERRED].** Copy the principle of an exit-eligible community pool versus non-exit-eligible restricted operating funds. Map each Kimosabe fund to a General Ledger account, an accountable steward, permitted uses, reserve rule, and audit trail before automating any transfers.
- **ADOPT — proposal-linked documentation and execution evidence [INFERRED].** Require each campaign, recruitment action, territory claim decision, and material spend to link to scope, owner, budget, acceptance evidence, and a public/internal decision record. DAOhaus’s observable execution trail is the useful lesson, not its chain-specific form.

### ADAPT

- **ADAPT — ragequit into a bounded dispute/withdrawal process [INFERRED].** Use a time-boxed objection and exit/appeal policy for voluntary community-credit commitments, but never allow unilateral pro-rata withdrawal from payroll, regulated donations, taxes, restricted grants, or funds owed to third parties. The Kimosabe equivalent needs clear contractual terms, reserve tests, and non-on-chain remedies.
- **ADAPT — Shaman-style automation into revocable service roles [INFERRED].** Create narrowly scoped automation/operations roles—recruiter, county steward, campaign publisher, budget controller—with least privilege, spend limits, dual approval, logs, expiry, and emergency revocation. Do not grant a single general-purpose automation actor broad mint/burn/configuration power.
- **ADAPT — Yeeter/Onboarder into compliant recruitment and campaign intake [INFERRED].** Preserve the idea of a transparent contribution-to-membership conversion flow, but add consent, eligibility, disclosures, fraud controls, CRM consent management, cash/fiat handling, and state-by-state legal review. Treat the reviewed Yeeter artifacts as a pattern, not a launch-ready fundraising product.
- **ADAPT — delegation [INFERRED].** Permit revocable, topic- and territory-limited delegation with disclosure of conflicts and expiry. Avoid permanent wallet-level blanket delegation and capital-proportional delegation for county representation.

### REJECT

- **REJECT — token balance as the primary measure of county legitimacy [INFERRED].** Human Blockchain governance needs territory, stakeholder role, contribution quality, and safeguards against pay-to-control dynamics. Token-weighted Shares can be an optional internal economic instrument, not the default civic representation rule.
- **REJECT — direct dependency on a hosted DAOhaus UI or unmaintained upstream contract as core infrastructure [INFERRED].** The maintenance evidence is uneven and direct dependencies create abandonment, license, provider, and security risk. Own the Kimosabe code, data model, backups, deployment, and incident response.
- **REJECT — unrestricted arbitrary multicall and broad Shaman power for routine operations [INFERRED].** Require allowlists, budgets, simulations, policy checks, clear human approvals, and reconciliation to the General Ledger.
- **REJECT — treating crypto-wallet onboarding as the primary recruiting funnel [INFERRED].** Kimosabe’s county-scale public-benefit audience needs accessible account recovery, phone/email alternatives where lawful, assisted onboarding, and nontechnical participation paths.

### DEFER

- **DEFER — on-chain Baal/Safe deployment [INFERRED].** Revisit only after Kimosabe has validated its off-chain operational model, data governance, legal structure, accounting controls, jurisdictional policy, user-accessibility requirements, and incident response. First validate whether an on-chain settlement benefit exceeds cost and harm.
- **DEFER — transferable credits or tokens [INFERRED].** DAOhaus supports configurable transferability, but seasonal credits should remain non-transferable until economic abuse, tax, securities, consumer-protection, and benefit-program implications are independently resolved.
- **DEFER — autonomous signing agents [INFERRED].** Current DAOhaus skills demonstrate agent-driven action, but their own documentation requires protected managed wallets and notes limitations around key rotation, custody, and simulation. Start with draft-only automation and human approval.

## Bottom line

**INFERRED.** DAOhaus/Baal is a valuable reference for transparent proposal execution, differentiated participation rights, Safe-based treasury separation, and minority-protection design. It is not a complete operating model for a public-benefit, U.S.-county network. The Kimosabe organization should take the **governance and auditability patterns**, then independently build the **identity, territory, recruiting, promotion, community support, compliance, General Ledger, and seasonal-credit controls** that DAOhaus does not supply.

## Sources

All sources below were accessed **2026-10-06**.

[1]: https://daohaus.club/ "DAOhaus home page — accessed 2026-10-06"
[2]: https://docs.daohaus.club/contracts/moloch-v3 "Moloch v3 (Baal) contracts documentation — accessed 2026-10-06"
[3]: https://daohaus.club/moloch "DAOhaus Moloch DAO history and v3 architecture — accessed 2026-10-06"
[4]: https://github.com/Moloch-Mystics/Baal "Moloch-Mystics Baal primary protocol repository — accessed 2026-10-06"
[5]: https://api.github.com/repos/Moloch-Mystics/Baal "GitHub API: Moloch-Mystics/Baal repository metadata — accessed 2026-10-06"
[6]: https://api.github.com/repos/HausDAO/monorepo "GitHub API: HausDAO/monorepo repository metadata — accessed 2026-10-06"
[7]: https://api.github.com/repos/HausDAO/daohaus-admin "GitHub API: HausDAO/daohaus-admin repository metadata — accessed 2026-10-06"
[8]: https://github.com/HausDAO/monorepo "HausDAO monorepo README — accessed 2026-10-06"
[9]: https://gov.optimism.io/t/draft-gf-phase-1-proposal-daohaus/3581 "DAOhaus Optimism Governance Fund proposal — accessed 2026-10-06"
[10]: https://decrypt.co/93196/dao-framework-builder-moloch-launches-v3-at-ethdenver "Decrypt: DAO framework builder Moloch launches v3 at ETHDenver — accessed 2026-10-06"
[11]: https://api.github.com/repos/HausDAO/daohaus-admin/commits/master "GitHub API: DAOhaus Admin master head commit — accessed 2026-10-06"
[12]: https://guide.daohaus.club/quickstart/member "DAOhaus user guide: Add a Member — accessed 2026-10-06"
[13]: https://api.github.com/repos/Moloch-Mystics/Baal/commits/feat/baalZodiac "GitHub API: Baal default-branch head commit — accessed 2026-10-06"
[14]: https://guide.daohaus.club/admin/proposals "DAOhaus user guide: Proposals — accessed 2026-10-06"
[15]: https://guide.daohaus.club/admin/summon "DAOhaus user guide: How to Summon a DAO — accessed 2026-10-06"
[16]: https://guide.daohaus.club/admin/settings "DAOhaus user guide: Settings — accessed 2026-10-06"
[17]: https://guide.daohaus.club/admin/members "DAOhaus user guide: Members — accessed 2026-10-06"
[18]: https://docs.daohaus.club/contracts/shamans "DAOhaus documentation: Shaman contracts — accessed 2026-10-06"
[19]: https://github.com/HausDAO/baal-tokens "HausDAO Baal tokens/Higher Order Summoner examples — accessed 2026-10-06"
[20]: https://github.com/yeet-haus/contracts "Yeet Haus contracts repository — accessed 2026-10-06"
[21]: https://docs.daohaus.club/contracts/treasury "DAOhaus documentation: Treasury (Safe) contracts — accessed 2026-10-06"
[22]: https://gitcoin.co/mechanisms/molochdao "Gitcoin mechanism review: MolochDAO — accessed 2026-10-06"
[23]: https://github.com/HausDAO/moloch-skills "HausDAO Moloch Skills integration repository — accessed 2026-10-06"
[24]: https://github.com/HausDAO/daohaus-admin "HausDAO Admin repository README — accessed 2026-10-06"
[25]: https://medium.com/daohaus-club/haus-launch-bd781bbbf13a "DAOhaus official blog: HAUS Launch — accessed 2026-10-06"
[26]: https://api.github.com/repos/HausDAO/moloch-skills "GitHub API: HausDAO Moloch Skills repository metadata — accessed 2026-10-06"
[27]: https://api.github.com/repos/HausDAO/user-guide "GitHub API: DAOhaus user-guide repository metadata — accessed 2026-10-06"
