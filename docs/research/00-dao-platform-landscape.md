# Open-Source DAO Management Platforms: Competitive-Intelligence Synthesis

**Decision context.** This synthesis ranks platforms by their usefulness as *component inspirations or bounded integrations* for a new public-benefit marketing, recruiting, promotion, and management organization—not by token-market adoption, total value locked, or general developer popularity. It is based solely on the supplied per-platform findings and their cited sources, accessed by the research agents **2026-10-06**. Numerical adoption, pricing, support, and hosted-service continuity claims that were not verified in those findings are intentionally left as **not verified**.

> **Evidence convention:** Observed repository/product facts, provider-reported claims, and inferences are distinguished in the underlying item reports. A dash in the capability matrix means **not evidenced in the supplied findings**, not that a capability is technically impossible. “Reusable” means an independently implemented operating pattern—not permission to copy code, UI, documentation, brand, or protected expression.

## 1. Ranked comparison

### Ranking method

The rank weights: (1) fit for real-world, public-benefit operations; (2) active and controllable deployment; (3) participation, accountability, and financial-operating maturity; and (4) the absence of default token/custody dependency. **No platform is a complete system of record** for the intended organization. The top ranks therefore identify the best *layers to learn from or integrate around*, not a winner-take-all procurement recommendation.

| Rank | Platform | License | Governance model | Treasury | Membership model | Hosting | Activity status |
|---:|---|---|---|---|---|---|---|
| **1** | **Decidim** | **AGPL-3.0** | Participatory processes, assemblies, initiatives, proposals, endorsements, meetings, voting, results and accountability; governed as a public commons through Decidim/MetaDecidim. | Participatory-budgeting and accountability workflows; **not** custody, payout, accounting, or a General Ledger. | Visitor, registered, and verified participation tiers; groups/verification capability requires release- and deployment-specific validation. | Modular, self-hosted application; per-instance GraphQL, OAuth, and protected machine credentials. | **Active** in the supplied evidence; repository unarchived and latest commit reported 2026-10-06. |
| **2** | **Open Collective** | **MIT** for the public frontend/API | Separates Collective admins from a legal **Fiscal Host**; platform stewardship through member-governed OFiCo. | The strongest reviewed real-money stewardship pattern: hosts hold funds and manage compliance, accounting, payments, expenses/receipts, and policy controls. It remains **not** the organization’s General Ledger. | Contributors and admins; public engagement rather than a recruiting CRM or verified territory graph. | Hosted GraphQL, OAuth, and webhooks; production self-host support for the complete financial stack is **not verified**. | **Active** in the supplied evidence; continuity/host diligence remains material following the 2024 organizational transition. |
| **3** | **Loomio** | **AGPL-3.0** | Asynchronous, process-flexible discussion and advice/consent/consensus decisions; company is a worker co-op using consent/dynamic hierarchies. | No native treasury or payout layer; its durable decision record is a useful control input to a separately governed ledger/treasury. | Group membership and participation, with email/chat-enabled engagement; no verified territory, identity, or recruiting graph. | US/EU/Australia cloud, private hosting, and self-hosting; API, exports, SSO, and chat integrations. | **Active** in the supplied evidence; repository unarchived and latest commit reported 2026-10-06. |
| **4** | **Snapshot** *(including the former Tally/Cactus Governor-service pattern)* | **MIT** for Snapshot `sx-monorepo` and legacy `snapshot-v1`; full former Tally/current Cactus hosted-service license **not verified**. | Each Space defines eligibility and voting strategy. Legacy Spaces are gasless off-chain signaling; Snapshot X and configured Governor/timelock flows can be binding on-chain. | Legacy Snapshot has no custody. Snapshot X/Governor can execute configured contract calls, but neither is a fiduciary, accounting system, custodian, or General Ledger. | Wallet/address membership, optional delegation, scores, proposal restrictions, and token/NFT/custom strategies; not civic identity or county eligibility. | MIT components include frontend, GraphQL API, hub, indexer, relayer, SDK, and MCP; self-hosting entails database/infrastructure/key operations. | **Snapshot active** in supplied evidence. Former **Tally** announced wind-down in March 2026 and was reported as taken over/rebranded to **Cactus** in June 2026; continuity, SLA, export, API, and security terms are **not verified**. |
| **5** | **Aragon OSx / Aragon App** | **AGPL-3.0** for OSx; Aragon App public-repository license **not verified**. | Configurable organization-level plugins and function-scoped permissions: token voting, multisig, address-list voting, staged/optimistic flows, timelocks, and councils. | DAO accounts hold assets and execute permitted actions; it is execution control, **not** accounting, payroll, tax, procurement, compliance, or a General Ledger. | ERC20Votes holdings/delegation, named multisig approvers, or one-address/one-vote lists; no CRM, territory, verified eligibility, or real-world identity layer. | Hosted no-code App plus SDK, ABI/artifacts, UI Kit/App Template, custom plugins, and self-hostable custom applications. | **Active** in the supplied evidence (OSx latest default-branch commit reported 2026-09-04; App reported 2026-10-05). Governance/stewardship continuity needs review after the 2023 association dissolution. |
| **6** | **Colony** | **GPL-3.0** | Scoped domains/teams, roles, reputation, lazy-consensus motions with objection/escalation, and Safe-module control. | Funding pots, task/reward allocations, staged/batch/stream payments, and Safe-enabled transfers; still not a full General Ledger or compliance/payroll system. | Wallet/permission-based membership; task manager-worker-evaluator roles and domain-scoped permissions. No CRM, eligibility, consent, anti-Sybil, or county workflow. | Direct contracts plus TypeScript SDK; Dapp has decentralized and hybrid modes, with unresolved chain/support/API details. | **Dormant/low-maintenance** in public evidence, not archived. Latest reported `develop` commit was 2026-03-24; an open PR was dated 2026-09-28. |
| **7** | **DAOhaus / Moloch v3 (Baal)** | **GPL-3.0** for Baal; historic HausDAO monorepo MIT; current DAOhaus Admin has **no declared license** in the supplied GitHub evidence. | Token-weighted proposal governance with voting/grace periods, Share/Loot rights, delegation, ragequit, and Safe/Zodiac execution. | Safe custody separates the ragequittable main pool from optional non-ragequittable sidecars; approved multicalls can execute passed actions. | Token Request proposals create Shares and/or Loot; delegation and Guild Kick exist, but no recruiting CRM, verified identity, or territorial eligibility. | Hosted Admin and a self-hostable Vite/React Admin; EVM contracts/ABIs, Safe/Zodiac, Shamans, The Graph/GraphQL, IPFS/Poster and RPC/provider surfaces. | **Selectively active/uneven:** Admin/tooling is current in supplied evidence, while Baal’s default-branch head was reported 2022-09-12. |
| **8** | **DAOstack (Alchemy / Arc)** | **GPL-3.0** verified for legacy Alchemy, Arc, arc.js, and Subgraph; later `alchemy-monorepo` top-level license **not verified**. | Reputation holders vote; GEN prediction/staking may boost proposals; Avatar holds assets; Controller authorizes schemes; global constraints restrict actions. | Avatar-held assets and approved funding/reward schemes can execute within Controller/global constraints; current custody, audit, fiat, and compliance controls are **not verified**. | Wallet-based founders receive Reputation/tokens; contribution reward may issue Reputation or funds. No verified CRM, general delegation, identity, accessibility, appeals, or territory model. | Historically self-hostable Solidity/Docker/Graph Node/Postgres/GraphQL stack; current hosted availability is **not verified**. | **Dormant**: supplied findings report material core default-branch work ending in 2021–2022, even though repositories are not formally archived. |

**Interpretation.** **Decidim** is first for public participation lifecycle and accountability, **Open Collective** for financial stewardship boundaries, and **Loomio** for low-friction human deliberation. **Snapshot** and **Aragon** are useful optional governance/execution adapters—not sources of civic legitimacy. **Colony**, **DAOhaus**, and especially **DAOstack** offer valuable patterns but demand increasing maintenance, custody, licensing, and security caution.

## 2. Capability matrix

**Legend:** **● Mark** = documented, native/core capability; **◐ Mark-partial** = limited, integration-dependent, historical, incomplete, or not an end-to-end fit; **— Mark-absent** = not documented in the supplied findings. This is a suitability matrix, not a substitute for release-specific testing.

| Platform | No-code DAO creation | Token / credit issuance | Off-chain voting | On-chain execution | Delegation | Roles & permissions | Membership onboarding | Treasury / multisig | Contribution tracking & payouts | Grants / crowdfunding | Public API / webhooks | Self-hosting | Mobile experience | Analytics & reporting | Community / forum layer |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| **Decidim** | ◐ | — | ● | — | — | ● | ● | ◐ | ◐ | ◐ | ◐ | ● | — | ● | ● |
| **Open Collective** | ● | — | — | — | — | ◐ | ◐ | ● | ● | ● | ● | ◐ | — | ● | ◐ |
| **Loomio** | ● | — | ● | — | — | ◐ | ● | — | — | — | ◐ | ● | — | ◐ | ● |
| **Snapshot** | ● | — | ● | ◐ | ● | ◐ | ◐ | ◐ | — | — | ● | ● | — | ● | ◐ |
| **Aragon OSx / App** | ● | ◐ | — | ● | ● | ● | ◐ | ● | — | — | ◐ | ◐ | — | — | — |
| **Colony** | ◐ | ● | — | ● | ◐ | ● | ◐ | ● | ● | ◐ | ◐ | ◐ | — | ◐ | — |
| **DAOhaus / Baal** | ● | ● | — | ● | ● | ● | ◐ | ● | ◐ | ● | ◐ | ● | ◐ | ◐ | — |
| **DAOstack** | ◐ | ● | — | ● | — | ● | ◐ | ● | ◐ | ◐ | ◐ | ◐ | — | ◐ | — |

### Matrix annotations that prevent false equivalence

- **Decidim** earns marks for participatory lifecycle, verified tiers, processes, public results, and accountability. Its partial treasury/grants marks mean participatory budgeting and allocation process—not custody, fiscal compliance, accounting, payroll, or cash disbursement.
- **Open Collective** earns its treasury, payout, crowdfunding, reporting, and API/webhook marks because **Fiscal Hosts** operationalize real-money controls. It earns only partial onboarding/roles because contributor/admin engagement is not a full recruiting, verification, or territory system; complete production self-hosting of the financial stack was not verified.
- **Loomio** is a strong off-chain human-decision and decision-record layer, not a finance, identity, campaign, or CRM layer. Its API/webhook cell is partial because API/SSO/exports are documented but a webhook catalog was not established in the supplied findings.
- **Snapshot** has two distinct modes that must not be conflated: gasless **off-chain Spaces** and configured **Snapshot X/Governor** binding execution. Its delegation and reporting strengths remain wallet/token centric; “self-hosting” requires operational control of infrastructure, databases, and keys.
- **Aragon** provides no-code deployment and deeply composable permissioned execution. Its token/credit cell is partial because voting-token integration is not a verified end-to-end civic-credit issuance/ledger system; its lack of a documented mobile/community/CRM layer is deliberate scope, not necessarily a defect.
- **Colony** is the clearest reviewed work-to-verification-to-payout pattern. Its delegation, self-hosting, grant, and API cells remain partial due to the supplied limitations and low-maintenance posture, not because its contracts lack expressive power.
- **DAOhaus** has a practical Safe/multisig and proposal/crowdfunding pattern, but shares/loot and Yeeter-style onboarding do not solve public-benefit eligibility, recruitment, or civic representation. Its mobile partial reflects WalletConnect support, not a verified full mobile product.
- **DAOstack** has a historically rich architecture and contribution-reward concept. All positive cells require the maintenance-risk qualifier: it is not a current production baseline without fresh security, licensing, deployment, and operations validation.

## 3. Five strongest reusable patterns to adopt

The following are **adopt-the-principle, independently design-the-implementation** recommendations. They are selected for transferability into a public-benefit operating organization, not for direct code reuse.

| Reusable pattern | Primary source platform(s) | Why it transfers | Independent implementation guardrail |
|---|---|---|---|
| **Dual approval and legal/operational separation for real-money actions** | **Open Collective** | Open Collective’s separation of a Collective from its Fiscal Host is the most directly applicable model for separating program intent, payment approval, custody, compliance, and receipt evidence. It limits the risk that a community vote silently becomes a payment instruction. | Maintain an independently designed, double-entry General Ledger, approval policy, receipt archive, and role matrix. Use Fiscal Host or custodian relationships only after jurisdiction, insurance, security, privacy, export, and service-continuity diligence. |
| **Participation lifecycle with public accountability** | **Decidim** | Decidim shows how proposals, meetings, endorsements, voting, results, and accountability can form a continuous public process rather than an isolated poll. That lifecycle maps well to transparent campaign, county, or stakeholder initiatives. | Build an original process model with locally appropriate accessibility, moderation, retention, appeal, and U.S. legal controls. Do not reproduce Decidim interface copy or assume its verification module proves a particular identity attribute. |
| **Task → independent verification → staged release → contribution record** | **Colony** | Colony’s manager-worker-evaluator separation, task specification/deliverables, staged payments, scoped teams, and visible allocation states are a useful accountability loop. The key transfer is separation of doing, checking, and releasing value. | Use non-transferable, explainable seasonal contribution records rather than speculative tokens. Make evaluations appealable; include recusal, accessibility accommodations, and human review; do not make a crypto wallet a prerequisite for work or recognition. |
| **Least-privilege, function-scoped authority and constrained execution** | **Aragon OSx** | Aragon’s function-scoped ACL, conditional permissions, plugin boundaries, timelocks, councils, and auditable execution highlight how high-consequence actions can be narrowly authorized. This is appropriate for promotions, disbursements, data export, role changes, and policy exceptions. | Implement policy-as-code only behind human-readable policy, change control, audit logs, dual control, emergency suspension, and independent security review. Do not default to public-chain storage of people, campaigns, applications, or sensitive operational data. |
| **Separate signal, delegation, and binding action—with transparent lifecycle notices** | **Snapshot** *(and the former Tally/Governor workflow pattern)* | Snapshot demonstrates low-friction, gasless signal collection, configurable voting strategies, delegate visibility, lifecycle notifications, GraphQL/webhooks, and a distinct path to binding Governor/timelock execution. It enables broad input without misrepresenting every poll as legal authority. | Define in advance which decisions are advisory, delegated, administrative, or binding. Representation must be based on verified stakeholder/territory mandates, capped and reviewable credits, notice/appeal rights, and a General-Ledger receipt—not raw token balance or wallet ownership. |

**Patterns considered but not adopted as defaults.** **DAOhaus** contributes the useful idea of separated pools/sidecars and minority-protection windows, but ragequit and arbitrary multicall/Shaman authority are poor defaults for shared public-benefit funds. **DAOstack** contributes Avatar/Controller/constraint separation and non-transferable Reputation, but its GEN-staked triage and dormant codebase should be treated as historical design input, not implementation substrate.

## 4. Five critical operating gaps none of the platforms fill

These are the decisive white spaces for a marketing, recruiting, promotion, and management organization. The platforms cover fragments of the answer, but **none supplies the complete system**.

| Gap | What is missing across the landscape | Why it matters for the new organization | Design implication |
|---|---|---|---|
| **1. End-to-end recruiting CRM and talent/member funnel** | **Aragon**, **DAOhaus**, **Colony**, **DAOstack**, and **Snapshot** are wallet/role/proposal systems; **Open Collective** has contributor/admin engagement; **Loomio** has groups; **Decidim** has registered/verified participants. None provides a full pipeline from prospect and referral through consent, application, screening, interview, training, placement, retention, reactivation, and offboarding. | Growth depends on trusted human relationships, not simply granting an address a voting or payment right. | Build a consent-based CRM with source/referral history, recruitment stages, communications preferences, training/compliance milestones, human-owner queues, and export/deletion workflows. |
| **2. Campaign and promotion operations** | **Decidim** can run participatory processes and **Loomio** can host deliberation, but no reviewed platform runs integrated campaign calendars, creative approvals, audience segments, canvassing/field activity, event execution, content distribution, partner promotions, or experimentation. | Marketing/recruiting performance requires repeatable operating playbooks and coordinated execution, not merely governance. | Create a campaign workspace with objectives, audiences, territory, budget envelopes, content/version approvals, channel checklists, events, volunteer tasks, consent, risk review, and post-campaign learning. |
| **3. Privacy-preserving attribution and conversion measurement** | **Snapshot**, **Aragon**, **DAOhaus**, **Colony**, and **DAOstack** center public wallet/event records; **Open Collective** centers transparent financial reporting; **Loomio** and **Decidim** report decisions/processes. None is a privacy-safe attribution system connecting outreach source → consented lead → onboarding → training → contribution → durable outcome. | Without attribution, the organization cannot responsibly learn which recruitment/promotion investments work—or defend allocation decisions. | Use a first-party event and attribution model with consent, minimization, retention limits, access scopes, aggregate reporting, correction/appeal paths, and separation of public accountability from private person-level data. |
| **4. Seasonal operating cycles and non-speculative community-credit administration** | **Colony** and **DAOstack** offer reputation/contribution concepts; **Snapshot**, **Aragon**, and **DAOhaus** offer token/strategy mechanics; none manages seasonal rules, credits, eligibility snapshots, expiration/rollover, disputes, reconciliation, conversion constraints, and reporting as an end-to-end civic operating cycle. | Seasonal campaigns and contribution programs need predictable timing, explainable value recognition, and auditable closeout—not permanently transferable token power. | Establish an explicit seasonal ledger: published rules, eligibility snapshot, capped formula, evidence links, provisional/verified/appealed states, close calendar, authorized conversion, reversal, and audit report. Keep it distinct from cash and from political/representation rights. |
| **5. Verified real-world identity, stakeholder designation, and territory representation** | **Decidim** offers verification tiers, but release-specific assurance is unresolved; every DAO stack reviewed is primarily wallet/address/token based. **Open Collective**, **Loomio**, and **Decidim** do not provide the required county stakeholder graph, anti-Sybil program, mandate/delegation controls, or jurisdictional appeals. | A public-benefit organization cannot infer residency, employer/community role, legitimacy, or representation from a wallet balance, email, or generic account. | Operate an independent identity/eligibility and territory service with minimal disclosure, credential provenance, consent, duplicate/abuse review, recertification, delegation bounds, conflict/recusal handling, and human appeal. Do not expose sensitive records on a public chain. |

**Cross-cutting sixth gap (non-negotiable even though not counted above):** none is a complete **General Ledger** for the intended organization. **Open Collective** is the closest reviewed financial-stewardship layer; **Colony**, **Aragon**, **DAOhaus**, **DAOstack**, and configured **Snapshot** flows can represent or execute allocations; **Loomio** and **Decidim** can record decisions. A canonical chart of accounts, reconciliation, audit trail, tax/compliance controls, receivables/payables, program/fund accounting, and controlled data exports must remain independently governed.

## 5. Differentiation thesis: a public-benefit operating system, not another token DAO

> **Thesis:** Build a **consent-first, territory-aware public-benefit operating system** that connects verified people and stakeholder mandates to recruiting funnels, campaign execution, seasonal contribution recognition, transparent decisions, and a true General Ledger—while using governance or blockchain tools only as optional, narrowly scoped adapters.

This is differentiated from the reviewed landscape in six concrete ways:

1. **Human legitimacy before wallet legitimacy.** Where **Snapshot**, **Aragon**, **DAOhaus**, **Colony**, and **DAOstack** begin from addresses, balances, reputation, or delegated wallet power, the new organization begins with consented, minimally disclosed real-world eligibility, stakeholder designation, territory, training, and appealable mandate.
2. **Operating funnel before proposal feed.** Where **Decidim** provides a rich public-process lifecycle and **Loomio** provides deliberation, the new system adds the missing private-to-permissioned flow: outreach → consent → lead → application → verification → training → placement → contribution → retention/re-engagement. Public transparency is derived from approved aggregates and decisions rather than exposure of personal operational data.
3. **Campaign-to-outcome closed loop.** Where no reviewed platform supplies campaign operations or attribution, the new design makes objectives, sources, content, events, tasks, conversion milestones, budget envelopes, outcomes, and lessons traceable under privacy controls.
4. **Seasonal credits as accountable records, not speculative governance tokens.** The system adapts **Colony** and **DAOstack** contribution-recognition ideas but uses a bounded, non-transferable, explainable, season-aware record with evidence, independent verification, dispute handling, and explicit limits on what it may influence. Credits neither substitute for cash nor automatically determine representation.
5. **Three separate planes of authority.** (a) a canonical private identity/territory/CRM plane; (b) an operating and decision-record plane informed by **Decidim**, **Loomio**, and **Snapshot**; and (c) a financial/settlement plane with **Open Collective**-style separation of responsibility and an independent General Ledger. Optional **Aragon**-style permissions or **Snapshot/Governor** execution can be attached only for well-defined, auditable actions.
6. **Original, interoperable implementation.** The organization should create its own data model, original interaction design, terminology, workflows, policies, and accessibility treatment. It may interoperate through documented APIs, exports, and smart-contract/SDK interfaces after review; it should not copy proprietary branding, UI, text, or protected expression. Direct reuse of AGPL/GPL code demands license-specific legal and engineering review; a clean independent implementation avoids treating competitor designs as a template to clone.

### Practical architecture hypothesis

| Plane | Canonical responsibilities | Optional informed-by integrations | Non-negotiable controls |
|---|---|---|---|
| **Identity, territory, and relationship plane** | Consent, verified eligibility, stakeholder roles, territory mandate, CRM funnel, communications preferences, case history, appeals, and recertification. | SSO/OAuth with **Decidim**, **Loomio**, **Open Collective**, or a governance adapter where appropriate. | Data minimization, encryption, access logging, deletion/export, anti-Sybil review, human escalation, accessibility, and no public-chain PII. |
| **Campaign and community-operations plane** | Campaign brief, audience, channels, content approvals, event/field operations, referrals, task coordination, contribution evidence, seasonal cycles, and attribution. | **Decidim**-style participatory processes; **Loomio**-style deliberation; **Colony**-inspired task/evaluator/release separation. | Consent-aware analytics, versioned approvals, recusal, supervision, moderation, outcomes measurement, and reviewable automation. |
| **Decision and representation plane** | Decision classification, notice, deliberation, stakeholder/territory eligibility, delegation limits, vote/signal capture, decision record, and appeal. | **Snapshot** signal votes/delegate visibility; **Loomio** consensus; **Decidim** processes; narrowly scoped **Aragon** authorization. | Advisory-versus-binding label, quorum/representation safeguards, audit trail, accessibility, appeal, and no one-token-one-vote civic default. |
| **Financial and settlement plane** | Chart of accounts, fund restrictions, budgets, commitments, invoices, approval matrices, payment evidence, reconciliation, close, and public aggregate reporting. | **Open Collective**-style fiscal-host separation; controlled **Safe/Aragon/Snapshot Governor** settlement only where justified. | Dual control, fiduciary/legal review, least privilege, ledger reconciliation, receipt retention, independent auditability, rollback/hold, and no automated payout by unreviewed poll. |

This thesis is a **hypothesis**, not a claim that any listed platform is unsuitable. It should be validated through a limited county/territory pilot with defined success measures: verified-onboarding completion, time-to-training, campaign conversion, cost per qualified recruit, contribution-evidence completion, decision participation across accessibility needs, reconciliation time, dispute/appeal resolution time, and privacy/security incidents.

## 6. Maintenance, dependency, and procurement risk

### Highest concern: dormant or uneven core projects

| Platform | Risk finding | What to do before any production reliance |
|---|---|---|
| **DAOstack (Alchemy / Arc)** | **High maintenance risk.** The supplied findings classify it as **DORMANT**, with material core default-branch work ending in 2021–2022. Arc documentation labels code alpha; hosted availability, audits, custody, support, and current governance practice are unverified. | Treat as an architectural case study only. Do not deploy/reuse for funds or authority absent an independent code/license/security audit, reproducible deployment, operating owner, incident response, and migration plan. Prefer independent reimplementation of concepts over direct dependency. |
| **Colony** | **Medium-high maintenance risk.** The supplied public evidence is dormant/low-maintenance rather than archived. Contract/SDK dependency, incident response, chain/support matrix, extension support, and some documentation claims remain unresolved. | Use the task/evaluator/staged-release pattern, not a direct default dependency. Require validated contracts, supported deployment target, audit evidence, security owner, SLA/response commitments, and exit/data-export plan before integration. |
| **DAOhaus / Baal** | **Medium maintenance and authority risk.** Current Admin activity does not erase a Baal core default-branch head reported in 2022. GPL/mixed licensing, absence of an Admin declared license, Shamans, arbitrary multicalls, signer/key management, and ragequit pool drainage are material. | If exploring, make every execution role revocable and least-privileged; prohibit unrestricted multicalls; use a controlled Safe policy; validate licenses and all upstream contracts; stage on non-production funds; preserve an independent ledger. |

### Material continuity or scope risks in active projects

- **Aragon OSx / App:** supplied evidence supports current code activity, but the 2023 association dissolution, legacy product migration, and current council/on-chain control configuration create stewardship/continuity questions. Use it, if at all, as optional authorization/execution infrastructure with independent key governance, audit, and export/migration capability.
- **Snapshot / former Tally/Cactus:** Snapshot’s MIT/public-code position and current activity are favorable. However, former **Tally** wind-down and subsequent **Cactus** takeover/rebrand mean no hosted service should be procured without written confirmation of operator, security posture, source/license scope, API terms, data export, business continuity, incident response, and SLA. Keep signal voting separate from binding authority.
- **Open Collective:** active maintenance and strong fiscal-host pattern do not remove the need to diligence a particular Fiscal Host, privacy segmentation, policy controls, transition continuity, and data/export requirements. Public-ledger defaults may conflict with sensitive operations.
- **Loomio and Decidim:** both show active maintenance in supplied evidence. Their primary risks are operational rather than dormancy: national-scale deployment, retention/deletion, moderation, accessibility, release-specific verification/group features, pricing/performance, security operations, and jurisdiction-specific legal design require a pilot and due diligence.

### Licensing note

**MIT** components (notably **Snapshot** and the reviewed **Open Collective** frontend/API) may be easier to reuse, but attribution/notice and dependency obligations still apply. **AGPL-3.0/GPL-3.0** components (**Aragon OSx**, **Loomio**, **Decidim**, **Colony**, **Baal**, and legacy **DAOstack**) carry copyleft obligations that require qualified legal review before modification, hosting, distribution, or incorporation. License status is explicitly **unverified** for Aragon App, DAOhaus Admin, DAOstack’s later monorepo, and the full former Tally/current Cactus hosted service; do not assume reuse rights.

## 7. Source list carried forward from the item reports

The links below are the source set supplied by the research agents. All were reported as accessed **2026-10-06** unless otherwise stated in the item report. Provider adoption and business claims remain provider-reported unless the underlying report labels them observed or independently corroborated.

### Aragon OSx / Aragon App

- [Aragon documentation](https://docs.aragon.org/)
- [Aragon OSx repository](https://github.com/aragon/osx) and [GitHub API metadata](https://api.github.com/repos/aragon/osx)
- [Aragon App repository](https://github.com/aragon/app)
- [“A new chapter for the Aragon project”](https://blog.aragon.org/a-new-chapter-for-the-aragon-project/)
- [Legacy product update](https://blog.aragon.org/legacy-product-update/)
- [Aragon Foundation: Advancing the Aragon mission](https://www.aragonfoundation.org/announcement/advancing-the-aragon-mission)
- [Ethereum developer tool listing](https://ethereum.org/developers/tools/aragon-osx/)
- [QuickNode Aragon guide](https://www.quicknode.com/builders-guide/tools/aragon-dao-by-aragon-association)
- [The Block: Aragon Association dissolution / ANT redemption reporting](https://www.theblock.co/news/ecosystems/2023-11-02-aragon-association-to-dissolve-itself-provide-liquidity-for-ant-redemption-261179)

### DAOhaus / Moloch v3 (Baal)

- [DAOhaus](https://daohaus.club/)
- [DAOhaus Moloch v3 contract documentation](https://docs.daohaus.club/contracts/moloch-v3)
- [Baal repository](https://github.com/Moloch-Mystics/Baal) and [GitHub API metadata](https://api.github.com/repos/Moloch-Mystics/Baal)
- [DAOhaus Admin repository](https://github.com/HausDAO/daohaus-admin)
- [DAOhaus Optimism grant proposal](https://gov.optimism.io/t/draft-gf-phase-1-proposal-daohaus/3581)
- [Haus launch post](https://medium.com/daohaus-club/haus-launch-bd781bbbf13a)
- [Decrypt: Moloch v3 launch coverage](https://decrypt.co/93196/dao-framework-builder-moloch-launches-v3-at-ethdenver)

### Colony

- [Colony Network documentation](https://docs.colony.io/next/colonynetwork/)
- [Colony site](https://colony.io/)
- [colonyNetwork GitHub API metadata](https://api.github.com/repos/JoinColony/colonyNetwork), [develop commits](https://api.github.com/repos/JoinColony/colonyNetwork/commits/develop), and [releases](https://api.github.com/repos/JoinColony/colonyNetwork/releases?per_page=10)
- [colonyJS repository](https://github.com/JoinColony/colonyJS) and [colonyCDapp repository](https://github.com/JoinColony/colonyCDapp)
- [Meta Colony / CLNY whitepaper TLDR](https://joincolony.github.io/colonynetwork/whitepaper-tldr-the-meta-colony-and-clny/)
- [Colony roadmap](https://blog.colony.io/roadmap)
- [SSRN research paper](https://papers.ssrn.com/sol3/Delivery.cfm/SSRN_ID3356774_code1344173.pdf?abstractid=3356774&mirid=1)

### DAOstack (Alchemy / Arc)

- [DAOstack alchemy-monorepo GitHub API metadata](https://api.github.com/repos/daostack/alchemy-monorepo)
- [Alchemy `dev` commits](https://api.github.com/repos/daostack/alchemy/commits/dev) and [Arc `master` commits](https://api.github.com/repos/daostack/arc/commits/master)
- [DAOstack Hackers Kit README](https://raw.githubusercontent.com/daostack/DAOstack-Hackers-Kit/master/README.md)
- [Genesis Protocol documentation](https://daostack.github.io/DAOstack-Hackers-Kit/stack/infra/genesisProtocol/)
- [DAOstack in 2021 post](https://medium.com/daostack/daostack-in-2021-2f0ba049e064)
- [The Graph: DAOstack Alchemy](https://thegraph.com/blog/daostack-alchemy/)
- [Hawaii scholarly paper](https://scholarspace.manoa.hawaii.edu/bitstreams/d0686298-aa64-4f41-aa7c-ff4b379d0c87/download)
- [DAOstack site observed in research](https://daostack.io/en/home.html)

### Snapshot and Tally/Cactus

- [Snapshot documentation](https://docs.snapshot.box/) and [Snapshot X protocol overview](https://docs.snapshot.box/snapshot-x/protocol/overview)
- [Snapshot `sx-monorepo`](https://github.com/snapshot-labs/sx-monorepo) and [GitHub API metadata](https://api.github.com/repos/snapshot-labs/sx-monorepo)
- [Snapshot: home for Governor DAOs](https://blog.snapshot.box/snapshot-is-now-home-for-governor-daos.md)
- [Starknet: Snapshot X on-chain voting](https://www.starknet.io/blog/snapshot-x-onchain-voting/)
- [Anchorage: Snapshot voting](https://www.anchorage.com/insights/announcing-snapshot-voting-with-anchorage-digital)
- [Tally OpenZeppelin Governor guide](https://docs.tally.xyz/user-guides/governance-frameworks/openzeppelin-governor/) and [OpenZeppelin governance documentation](https://docs.openzeppelin.com/contracts/5.x/governance)
- [Business Wire: Tally Series A announcement](https://www.businesswire.com/news/home/20250422345730/en/Tally-Raises-%248-Million-Series-A-to-Help-Protocol-Tokens-Accrue-Value)
- [Compound forum: Tally governance-service proposal](https://www.comp.xyz/t/proposal-tally-as-a-dedicated-governance-service-provider-to-the-compound-dao/6789)
- [Tally Zero repository](https://github.com/withtally/tally-zero)
- [Scopelift: Tally is now Cactus](https://scopelift.co/blog/tally-is-now-cactus)

### Open Collective, Loomio, and Decidim

- [Open Collective: how it works](https://opencollective.com/how-it-works), [Fiscal Host documentation](https://documentation.opencollective.com/fiscal-hosts/fiscal-hosts), and [frontend GitHub API metadata](https://api.github.com/repos/opencollective/opencollective-frontend)
- [Loomio: collaborative decision-making](https://www.loomio.com/collaborative-decision-making/), [Loomio GitHub API metadata](https://api.github.com/repos/loomio/loomio), and [Loomio cooperative coordination](https://www.loomio.coop/coordination.html)
- [Decidim features](https://decidim.org/features/), [Decidim GitHub API metadata](https://api.github.com/repos/decidim/decidim), [Decidim API authentication documentation](https://docs.decidim.org/en/develop/develop/api/authentication.html), and [Decidim about page](https://decidim.org/about/)
- [Open Source Observatory: Decidim](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/decidim)
- [Academic background paper](https://arxiv.org/abs/1707.06526)

## 8. Bottom line

The market does **not** offer a turnkey “DAO management platform” that safely unifies marketing, recruiting, promotion, public participation, identity/territory, contribution records, and financial management. A defensible strategy is to use **Decidim** for participation-process lessons, **Open Collective** for fiscal-separation lessons, **Loomio** for deliberation lessons, **Colony** for accountable work/payout lessons, and **Aragon/Snapshot** only as optional execution or signaling patterns—while making an independently controlled CRM, identity/territory service, campaign system, seasonal ledger, and General Ledger the canonical core. The choice should be validated with a small, measured pilot before high-authority automation, public-chain settlement, tokenized credits, or national-scale deployment.

**Research failures to note:** none were supplied.
