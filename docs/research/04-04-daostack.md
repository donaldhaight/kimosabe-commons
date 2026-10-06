# DAOstack (Alchemy / Arc / DAOstack Hub): evidence-led competitive-intelligence report

**Assessment date:** 2026-10-06  
**Decision context:** lessons for a *new* public-benefit marketing, recruiting, promotion, community-management and governance-operations organization serving the Kimosabe App and Human Blockchain. Kimosabe/Human Blockchain characteristics in the request are treated as **[ASSUMED]** design context, not independently researched facts.

**Claim labels:** **[OBSERVED]** = directly checked in a primary source or API; **[REPORTED]** = a source's historical statement; **[INFERRED]** = a reasoned conclusion from cited evidence; **[UNVERIFIED]** = no adequate public evidence found in the reviewed material.

## Identity, audience, and current status

**[REPORTED]** DAOstack was an Ethereum-based, open-source stack for creating decentralized applications, DAO tools and DAOs. Its published stack separated: **Infra** governance primitives; **Arc** Solidity contracts for a DAO; a JavaScript client and indexed **Subgraph**; and **Alchemy**, an end-user budgeting and resource-allocation application. The project positioned Alchemy for decentralized venture, charitable and innovation funds, budget proposals and open-source feature prioritization—not as a general CRM or marketing platform. [8] [9]

**[REPORTED]** Its intended users were organizations that needed members to propose, prioritize, vote on, and execute decisions about shared resources. The primary governance user was a **Reputation** holder; outside participants could make proposals and use GEN to predict outcomes, but only Reputation holders voted in Alchemy's described workflow. [9] [11]

> **Current-status finding — DORMANT, not formally archived.** **[OBSERVED]** GitHub currently marks the core repositories as `archived: false`, but the Arc default branch's latest commit is 2021-04-08 and the successor `alchemy-monorepo` default branch's latest commit is 2022-05-31. The legacy Alchemy default branch also ends 2022-05-31. The repository API shows later pushes in some repositories/branches (Alchemy 2023-03-01; Arc 2023-01-24), which is not evidence of ongoing product maintenance. [1] [2] [3] [4] [5] [6]
>
> **[OBSERVED]** On 2026-10-06, `daostack.io` pages that once advertised Alchemy instead returned unrelated crypto-casino editorial content. This establishes that the current domain cannot be treated as a trustworthy DAOstack product/documentation channel; it does **not** establish why that occurred or who controls the domain. [17] **[INFERRED]** Together with the multiyear code inactivity, this supports classifying DAOstack as **dormant** rather than maintained. No formal DAOstack archival or shutdown notice was located in the primary sources reviewed, so a claim of formal closure is **[UNVERIFIED]**.

### DAOstack Hub clarification

**[UNVERIFIED]** No primary DAOstack documentation or repository found in this review defines a distinct product named **“DAOstack Hub.”** The live `daostack.io` content is unrelated to DAOstack, so it cannot fill that gap. This report therefore covers the evidenced DAOstack components—Alchemy, Arc, Infra, `arc.js`, Subgraph and Genesis—and does not attribute unverified “Hub” functionality to the project.

## Code, license, and activity signals

**Primary repository for evaluation:** [`https://github.com/daostack/alchemy-monorepo`](https://github.com/daostack/alchemy-monorepo). **[OBSERVED]** The Arc repository itself says Arc development moved to `packages/arc` in that monorepo, making it the closest available canonical combined codebase for the later Alchemy/Arc work. [7]

**License position:** **[OBSERVED]** GitHub identifies the legacy `daostack/alchemy`, `daostack/arc`, `daostack/arc.js`, and `daostack/subgraph` repositories as **GNU GPL v3.0**. The monorepo's GitHub metadata reports `license: null`, and its root listing contains no top-level `LICENSE` file. Thus, it is accurate to call the legacy core packages GPL-3.0; it is **not verified** that the entire later monorepo has a published top-level license. Do not assume that a fork of the monorepo is permissively reusable. [1] [2] [3] [18] [19] [20]


There is **no verified current install count, hosted-DAO count, service-level commitment, or current user count** in the reviewed sources.

## Core capabilities

1. **[REPORTED] Modular on-chain organization account and authority model.** Arc's **Avatar** is the DAO's asset-owning blockchain identity. Its **Controller** registers schemes, sets their permissions and enforces global constraints. [7] [8]
2. **[REPORTED] Reputation-weighted governance.** Arc Reputation is DAO-specific decision power. It is non-transferable and can be granted or removed by DAO decision, unlike a transferable token. [7] [8]
3. **[REPORTED] Proposal-to-execution schemes.** Schemes represent actions the DAO can take. Documented examples include funding/reward proposals, generic calls to contracts, registering schemes or constraints, and upgrading the controller. A successful funding proposal can automatically release funds. [8]
4. **[REPORTED] Holographic Consensus / Genesis Protocol.** Submitted proposals begin queued, may receive GEN staking for/against, move through pre-boosted to boosted if thresholds persist, and then use relative-majority voting. Unboosted proposals use an absolute-majority requirement. The parameters set timing, quorum, bounty, threshold and quiet-ending behavior. [10] [11]
5. **[REPORTED] Alchemy end-user workflow.** A member can make a proposal, predict whether it will pass, and vote. Alchemy also exposed proposal status/metrics, participant activity, DAO holdings and a discussion wall according to The Graph's contemporary account. [9] [12]
6. **[REPORTED] Indexed, queryable activity.** The Subgraph indexed blockchain events into Postgres through Graph Node and exposed GraphQL; `arc.js`/Client was described as a TypeScript layer for proposing, voting, staking, executing and querying DAO data. [8]

## Governance model and incentives

**[REPORTED]** DAOstack's distinctive model separates *decision rights* from *attention prediction*:

- **Reputation holders** vote. Reputation is not transferable and is intended to reflect DAO-specific contribution or stake. [7] [8]
- **Anyone, including a non-member**, could stake GEN to predict an accept/reject outcome. Correct stakers were rewarded, while losing stakes were lost. Staking was intended to focus attention and allow a proposal that met the boosting condition to pass on a relative majority of those voting, instead of needing a majority of all Reputation. [10] [11]
- **[REPORTED]** A DAO selected its own Genesis Protocol configuration—including activation, queued and boosted vote periods, non-boosted quorum, boost threshold, proposer Reputation reward, and quiet-ending extension. This makes policy configurable, but moves significant governance risk into parameter selection. [10]
- **[REPORTED]** Global constraints could stop current or later schemes from violating a system-wide rule, such as a Reputation cap or maximum fund burn rate. [7] [8]

**Third-party evidence.** **[REPORTED]** The academic validation study found markedly stronger prediction accuracy in its larger DAO group (0.93) than in the smaller group (0.67); the authors concluded that the mechanism appeared to serve its intended purpose better in larger DAOs. This supports the *hypothesis* that prediction filtering can help where proposal volume and voter attention are high. It does not prove fairness, resistance to coordinated influence, legal suitability, or performance for U.S.-county stakeholder governance. [13]

**[INFERRED]** The central trade-off is productive but sharp: holographic consensus treats scarce attention as a resource, yet inserts a financially incentivized prediction layer between a proposal and an easier voting threshold. That is less suitable when decisions concern public-benefit legitimacy, real-world persons, or essential rights and must be explainable without economic-game expertise.

## Membership, roles, delegation, and recruiting mechanics

### What the stack documented

**[REPORTED]** The basic roles were **proposer**, **GEN predictor/staker**, **Reputation-holder voter**, and **scheme/controller-authorized actor**. Anyone could propose and predict; only Reputation holders could vote. On launch, a DAO creator chose founder addresses and their initial Reputation/token allocations; the documented creator could bundle founder allocations for up to 100 members in one transaction. [8] [9]

**[REPORTED]** Contribution and recruiting were chiefly economic/governance mechanisms, not a member-success workflow. The `ContributionReward` scheme could distribute funds or Reputation for approved contributions. Genesis 1.0 proposed additional onboarding through monthly auctions: people could lock GEN, receive Reputation in proportion to amount and duration, and thereby become voting participants. It also named builders, growth teams and predictors as contributor groups. This describes a specific Genesis proposal and should not be treated as a universal DAOstack membership rule. [8] [16]

**[REPORTED, historic]** DAOstack's 2018 token-sale post described more than 50 project ambassadors/early adopters, “Pollinators.” That is evidence of a human community initiative, not a software-native recruiting funnel. [14]

**Delegation:** **[UNVERIFIED]** A general, user-facing delegation system was not established in the reviewed official docs. Genesis Protocol has a `voteOnBehalf` parameter name without an explanation in the retrieved documentation, which is insufficient to claim delegation functionality. Do not assume liquid delegation, proxy delegation, identity verification, term limits, territorial representation, background checks, recruitment pipelines, or off-chain role management.

### Operational implication

**[INFERRED]** DAOstack can represent wallet-based voting power and programmed permissions, but it does not itself supply the operating layer a Kimosabe organization would need: candidate relationship management, localized recruiting, orientation, credential validation, consent records, contributor coaching, conflict support, or performance-based staffing. Those must be designed as separate, accountable functions.

## Treasury and fund management

**[REPORTED]** Arc's Avatar may own assets; a funding scheme can turn a passed proposal into an automatic allocation. The Controller and global constraints can limit the schemes that act on assets and set rules such as a maximum burn rate. This is the core of DAOstack's on-chain treasury model. [7] [8]

**[REPORTED]** Alchemy explicitly framed itself as a budgeting and resource-allocation tool. The historical Genesis structure proposed a community-managed fund and funding to DAOstack-related projects. DAOstack's 2018 sale post said most proceeds would be reserved for management by Genesis, where anyone could submit proposals. [9] [14]

**[REPORTED, historic/proposed]** The Genesis 1.0 post described revenue sources as locked GEN, DAI/ETH supplied from DAOstack's token-sale funding, potential locked-GEN sales and potential registry revenue. It said Genesis then received $40,000/month equivalent from DAOstack and targeted $70,000/month by end-Q1 2020. These are dated reported plans, not a current treasury balance, budget, or recurring revenue claim. [16]

**[UNVERIFIED]** Current treasury balances, custody arrangement, fiat banking, audit cadence, grant controls, tax/reporting workflow, multi-signature procedures, and funds remaining after the Genesis halt are not verified by this review. DAOstack should not be assumed to satisfy public-benefit fund stewardship or U.S. compliance requirements.

## Hosting, APIs, and extension surfaces

**[REPORTED]** DAOstack was not only a hosted product. Developers could self-run the components: Alchemy's README offered local development with Docker Compose, Ganache and Graph Node; the Hacker Kit says a developer could run a Graph Node locally or remotely. The original Alchemy README listed hosted URLs, but their present availability is **unverified**, and the primary `daostack.io` web channel is not reliable as of the assessment date. [8] [9] [17]

**[REPORTED]** Extension surfaces included:

- Solidity **schemes** and **global constraints** registered through the Controller;
- alternative **voting machines** / voting-rights management at the Infra level;
- the Arc npm package and `arc.js` client for contract interactions;
- a Graph Protocol **Subgraph** / GraphQL query surface, with custom schema and mappings needed for custom Arc contracts; and
- custom Alchemy/DAO front ends and landing-page content through code changes/PRs. [7] [8] [9]

**[OBSERVED]** The separate `arc.js` and Subgraph repos are public and GPL-3.0 but have old activity signals. [18] [19] **[INFERRED]** A new implementation would need to own the hosting, indexer, dependency upgrades, key management, observability, accessibility, and incident response; no maintained hosted SaaS or support commitment was verified.

## Business model and funding

**[REPORTED]** DAOstack funded its early development through a 2018 GEN utility-token sale. It reported a 5,073 ETH main-sale cap, a 7,000 ETH presale cap, and roughly 32,700 ETH in private-sale advance purchases—about **44,773 ETH in stated accepted/capped sale amounts**, without converting that figure to USD. It reported more than 2,000 participating purchasers across at least 120 countries and 4,940 GEN-holding wallets as of 2018-05-12. [14]

**[REPORTED]** GEN's intended business/economic role was a “collective attention” token used to stake predictions; DAO founders would obtain GEN to incentivize prediction. DAOstack's 2021 update said that requiring GEN had negatively affected the experience of users and projects, and promised a revised GEN model. [11] [15]

**[UNVERIFIED]** No current paid plan, enterprise pricing, support contract, foundation budget, commercial revenue, or active token-economics revision was verified. **[INFERRED]** It is most accurately understood as a historically ICO-funded open-source protocol/application effort, not a currently evidenced recurring-revenue governance-operations vendor.

## Strengths

- **[REPORTED] Attention-aware governance.** Holographic consensus offered an explicit response to proposal overload rather than assuming all members will read all proposals. The empirical study provides some evidence of better prediction performance in larger analyzed DAOs. [10] [13]
- **[REPORTED] Clear separation of organization primitives.** Avatar, Reputation, Controller, schemes and global constraints make authority, asset custody and policy boundaries legible at the smart-contract level. [7] [8]
- **[REPORTED] Non-transferable DAO-specific voting power.** Reputation avoids direct transfer of voting power and can be awarded or removed by the DAO, which is a useful conceptual basis for contribution-linked governance. [7]
- **[REPORTED] Programmable treasury rules.** Funding proposals, automatic execution, constraints and permissioned schemes can make a published allocation rule mechanically enforceable. [8]
- **[REPORTED] Composable data/extension design.** Solidity modules, a JavaScript client, GraphQL indexing and custom dApps provide multiple integration points rather than a single closed interface. [8]
- **[OBSERVED] Public source code and historical evidence.** The accessible repositories and documented historic deployments make DAOstack a useful case study even though it is dormant. [1] [2] [3]

## Gaps and unresolved weaknesses

- **[OBSERVED] Maintenance risk is material.** Core code and docs show multiyear inactivity, and the historical web domain now shows unrelated material. “Not archived” is not a substitute for a maintained release process. [1] [2] [3] [17]
- **[REPORTED] Security maturity was explicitly limited.** Arc's README calls Arc **alpha** and says users should use common sense around real money; it disclaims responsibility for implementation decisions and security problems. That warning is incompatible with treating the code as current production treasury infrastructure without a fresh, independent review. [7]
- **[INFERRED] Complex incentives and parameterization.** Boost thresholds, staking, bounties, quorums, timing and quiet endings create a governance system that operators and ordinary members must understand. Poor configuration can change who gets attention or how easily proposals pass. [10]
- **[REPORTED] The studied benefit is uneven.** The academic analysis found much weaker overall predictive accuracy for its smaller DAO group (0.67) than its larger group (0.93). Holographic filtering should not be presumed beneficial for every county, stakeholder group, or season. [13]
- **[INFERRED] Financialized attention is a poor default for public-benefit decisions.** GEN staking could favor people with capital, specialized knowledge, or coordinated influence; it also makes legitimacy depend partly on a speculative instrument. The reviewed sources do not establish safeguards sufficient for a county-level civic/public-benefit network.
- **[UNVERIFIED] Human governance controls are not documented here.** Identity assurance, anti-Sybil controls, delegation rules, appeals, accessibility, privacy, anti-harassment operations, conflict-of-interest disclosure, geographic eligibility, government/nonprofit compliance and participant safeguards require an independent design.
- **[INFERRED] Community operations are under-scoped.** A proposal wall and on-chain activity dashboard do not replace marketing operations, multilingual communication, recruiting CRM, training, field support or evidence-based contribution evaluation.
- **[OBSERVED] License ambiguity at the later monorepo.** The old component repos are GPL-3.0, while the later monorepo does not expose a top-level license via its API/root listing. This needs legal clarification before any reuse. [1] [2] [3]

## Relevance to a Kimosabe/Human Blockchain marketing, recruiting and management organization

The organization described in the prompt needs accountable human operations across U.S. counties, stakeholder groups, seasonal community credits, a General Ledger, and a claim/conversion loop. DAOstack is **a source of governance patterns, not a deployable operating platform** for that mission.

### ADOPT

1. **[DECIDED] Adopt the architectural separation of identity/authority, decision rights, action modules and non-bypassable constraints.** Use an independently designed, human-readable permission model: territory/role authority; proposal types; budget ceilings; conflict-of-interest checks; and immutable General Ledger audit events. DAOstack's Avatar–Controller–scheme–constraint separation is the useful pattern, not code to copy. [7] [8]
2. **[DECIDED] Adopt a visible proposal lifecycle.** Show each claim, conversion, campaign, recruitment request or allocation moving through draft, review, decision, execution, evidence and reconciliation. Combine it with plain-language reasons, named accountable operators and an appeal state; this preserves DAOstack's legibility while serving public-benefit accountability. **[INFERRED]**
3. **[DECIDED] Adopt contribution-linked credentials as a concept, not transferable financial power.** A seasonal, non-transferable community credential can recognize verified work, analogous to the *concept* of DAO-specific Reputation. Make the credential's issuance, expiry, correction and appeal policies transparent. [7]

### ADAPT

1. **[DECIDED] Adapt attention filtering into a non-financial triage queue.** Where proposal volume becomes too high, use rotating trained reviewers, topic experts and territory representatives to recommend urgency/quality—not open token staking. Publish conflict disclosures, reviewer rationale, error rates and appeal paths. The study supports testing filtering in high-volume contexts, but only as a guarded operational hypothesis. [13]
2. **[DECIDED] Adapt global constraints into policy-as-code plus human sign-off.** Enforce such limits as a county allocation cap, seasonal credit issuance ceiling, dual approval for payouts, required evidence for conversion, and a pause/rollback authority. Real-world exceptions need a logged, authorized process rather than an irreversible automated execution. [7] [8]
3. **[DECIDED] Adapt Arc schemes into independently built, typed workflows.** Make separate, versioned modules for recruiting, campaign grants, stakeholder claims, credit issuance, General Ledger adjustment and territory conversion. Each should have a measurable acceptance criterion, data-retention rule and responsible operator. **[INFERRED]**
4. **[DECIDED] Adapt indexed public reporting.** Maintain a privacy-preserving dashboard of aggregate county activity, campaigns, credit issuance, outcomes and ledger reconciliation. Use an application database/API appropriate to the mission; a GraphQL-like read model can be useful, but do not expose participant data by default. [8]

### REJECT

1. **[DECIDED] Reject direct production reuse of DAOstack/Alchemy/Arc code.** Dormant maintenance, the alpha warning, old dependencies, current hosting uncertainty and GPL/monorepo-license ambiguity make it an unsuitable foundation for a new public-benefit operations service without a separate security, legal and maintenance program. [1] [2] [3] [7] [17]
2. **[DECIDED] Reject GEN-like open financial staking as the default gateway to public attention.** It adds capital-weighted, speculative incentives to civic/community decisions and is poorly aligned with county-level recruiting, participant care and public legitimacy. **[INFERRED]**
3. **[DECIDED] Reject wallet-only membership as the operating identity model.** The new organization needs consent, eligibility, privacy, accessibility and role accountability that the reviewed DAOstack material does not establish. **[INFERRED]**
4. **[DECIDED] Reject a single universal credit/token as the sole measure of contribution, authority and value.** Keep community credit, decision authority, compensation eligibility, reputation and territorial responsibility as separately governed dimensions. **[INFERRED]**

### DEFER

1. **[DECIDED] Defer any on-chain treasury, autonomous payment or tradable-credit deployment.** First run a season using reversible off-chain ledgers, dual controls, reconciliation, participant support, abuse testing and independent legal/accounting review. Move only narrow, low-harm audit proofs on-chain if a concrete benefit is demonstrated.
2. **[DECIDED] Defer prediction-market-style triage until the organization has measured proposal volume, review backlog, error/appeal rates and the effect on underrepresented territories. The cited benefit is historical and context-dependent. [13]**
3. **[DECIDED] Defer delegation design until stakeholder representation, county boundaries, conflicts, term duration, recall and participation accessibility are decided. DAOstack documentation reviewed here does not supply a verified delegation model.**

## Bottom line

**[INFERRED]** DAOstack's enduring lesson is not that a public-benefit network should become a DAO. It is that large contributor networks need an explicit way to make authority, constrained actions, resource allocations and attention queues visible. For Kimosabe/Human Blockchain, independently implement those principles in an accountable operations system centered on people, territories, evidence, privacy and a General Ledger. Treat holographic consensus as a narrow, carefully tested research pattern—not as a production governance default.

## Sources

[1]: https://api.github.com/repos/daostack/alchemy "GitHub API: daostack/alchemy repository metadata" (accessed 2026-10-06)

[2]: https://api.github.com/repos/daostack/arc "GitHub API: daostack/arc repository metadata" (accessed 2026-10-06)

[3]: https://api.github.com/repos/daostack/alchemy-monorepo "GitHub API: daostack/alchemy-monorepo repository metadata" (accessed 2026-10-06)

[4]: https://api.github.com/repos/daostack/alchemy-monorepo/commits/dev "GitHub API: latest commit on alchemy-monorepo dev" (accessed 2026-10-06)

[5]: https://api.github.com/repos/daostack/alchemy/commits/dev "GitHub API: latest commit on Alchemy dev" (accessed 2026-10-06)

[6]: https://api.github.com/repos/daostack/arc/commits/master "GitHub API: latest commit on Arc master" (accessed 2026-10-06)

[7]: https://github.com/daostack/Arc "DAOstack Arc repository README" (accessed 2026-10-06)

[8]: https://raw.githubusercontent.com/daostack/DAOstack-Hackers-Kit/master/README.md "DAOstack Hacker Kit README" (accessed 2026-10-06)

[9]: https://raw.githubusercontent.com/daostack/alchemy/master/README.md "DAOstack Alchemy README" (accessed 2026-10-06)

[10]: https://daostack.github.io/DAOstack-Hackers-Kit/stack/infra/genesisProtocol/ "DAOstack Developer Portal: Genesis Protocol" (accessed 2026-10-06)

[11]: https://medium.com/daostack/on-the-utility-of-the-gen-token-eb4f341d770e "DAOstack: On the Utility of the GEN Token" (accessed 2026-10-06)

[12]: https://thegraph.com/blog/daostack-alchemy/ "The Graph: A Subgraph for 20+ DAOs is Powering DAOstack's Alchemy" (accessed 2026-10-06)

[13]: https://scholarspace.manoa.hawaii.edu/bitstreams/d0686298-aa64-4f41-aa7c-ff4b379d0c87/download "Faqir-Rhazoui, Arroyo & Hassan: A Scalable Voting System—Validation of Holographic Consensus in DAOstack" (accessed 2026-10-06)

[14]: https://medium.com/daostack/daostack-token-sale-successfully-concluded-ec813e7adc6b "DAOstack: Token Sale Successfully Concluded" (accessed 2026-10-06)

[15]: https://medium.com/daostack/daostack-in-2021-2f0ba049e064 "DAOstack in 2021" (accessed 2026-10-06)

[16]: https://medium.com/daostack/genesis-1-0-6184dffbfe8a "Genesis 1.0: Mission, Principles, and Structure" (accessed 2026-10-06)

[17]: https://daostack.io/en/home.html "Current daostack.io page retrieval" (accessed 2026-10-06; returned unrelated crypto-casino content)

[18]: https://api.github.com/repos/daostack/client "GitHub API: daostack/arc.js repository metadata" (accessed 2026-10-06)

[19]: https://api.github.com/repos/daostack/subgraph "GitHub API: daostack/subgraph repository metadata" (accessed 2026-10-06)

[20]: https://api.github.com/repos/daostack/alchemy-monorepo/contents "GitHub API: alchemy-monorepo root contents" (accessed 2026-10-06)

[21]: https://api.github.com/repos/daostack/DAOstack-Hackers-Kit "GitHub API: DAOstack Hacker Kit repository metadata" (accessed 2026-10-06)

[22]: https://cyber.harvard.edu/story/2025-11/rise-and-fall-daostack "Berkman Klein Center: The rise and fall of DAOstack" (accessed 2026-10-06; page identifies a mixed-methods postmortem but the retrieved extract did not provide findings used above)
