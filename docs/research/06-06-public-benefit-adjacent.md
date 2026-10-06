# Public-benefit and civic governance platforms: Open Collective, Loomio, and Decidim

**Research access date:** 2026-10-06  
**Decision context:** This comparison informs a **new public-benefit organization** responsible for marketing, recruiting, promotion, community management, and governance operations for the Kimosabe App / Human Blockchain ecosystem. The ecosystem is described in the assignment as a U.S.-county-level stakeholder network with seasonal community credits, a General Ledger, territory-based stakeholder groups, and a claim/conversion loop.

## Evidence labels

- **OBSERVED** — directly documented in the cited product, documentation, repository, or policy source.
- **REPORTED** — stated by an operator, user, vendor, or third party; not independently audited here.
- **INFERRED** — analytical conclusion drawn from observed evidence.
- **ASSUMED** — context supplied in the assignment or an unverified design premise.

> **Scope note — ASSUMED:** “Community credits,” claim/conversion rules, county stakeholder designations, and the Human Blockchain General Ledger are product concepts supplied by the brief. None of the three platforms was verified as implementing those specific concepts.

## Open Collective

### What it is and who it serves

**OBSERVED:** Open Collective is a financial-operations platform for a group (“Collective”) to receive contributions and manage expenses with a visible budget. Its core proposition combines contribution collection, expense workflows, community updates and fiscal hosting so a group can raise and spend money without separately incorporating or opening its own bank account.[1]

**OBSERVED:** A Fiscal Host is the legal entity holding funds, issuing receipts/invoices, handling tax, accounting, compliance, financial administration, and payment of Collective-approved expenses. Hosts set their own acceptance policies and fees; Collectives that receive or pay money need a host unless they convert to an Organization with their own legal/financial setup.[2]

**REPORTED:** The platform’s public transition announcement says a group of fiscal hosts representing **thousands of Collectives** formed the Open Finance Consortium (OFiCo) to take over the then-current platform branch from Open Collective Inc. The announcement also records disruption risk: Open Collective Foundation, then one of the largest hosts, had ceased operations earlier in 2024.[8]

### License, primary repositories, adoption, and maintenance

**OBSERVED:** The primary public application repository selected for this comparison is [`opencollective/opencollective-frontend`](https://github.com/opencollective/opencollective-frontend), a Next.js/React frontend under the **MIT License**. On 2026-10-06 it had **893 GitHub stars**, **453 forks**, was **not archived**, and its most recent commit was **2026-10-06 09:19:28 UTC**.[5] [6]

**OBSERVED:** The companion backend is [`opencollective/opencollective-api`](https://github.com/opencollective/opencollective-api), described as a TypeScript GraphQL API using Sequelize/PostgreSQL. It was **MIT-licensed**, **not archived**, had **471 stars** and was pushed on **2026-10-06 08:42:03 UTC**.[7] The GitHub-org repository named `opencollective/opencollective` is an MIT-licensed issue/RFC/document tracker rather than the deployable application; it had 2,281 stars on the same access date (not used here as product-source adoption).[30]

**INFERRED — activity status: actively maintained:** Same-day commits/pushes in the frontend and API, plus public 2025 development-cycle updates visible on OFiCo’s public Collective page, are strong current maintenance signals. This does **not** by itself validate financial control quality, organizational durability, or the stability of the post-2024 governance transition.

### Core capabilities

**OBSERVED:** The documented platform workflow includes public budget display; contribution tiers/goals and credit card, bank-transfer, and PayPal payment options; submitted receipts/invoices that admins approve or reject; automatically updated balances after payment; updates and conversation forums; contributor leaderboards; monthly activity/expense reports; event-ticket revenue; project-specific budgets; embeddable contribution components; optional 2FA; and limited-host beta virtual cards.[1]

**OBSERVED:** Hosts can configure contribution information thresholds, expense-type policies (invoice, receipt, grant), minimum Collective-admin counts, self-approval limits, non-team expense-submission rules, expense categories, accepted expense types, vendor rules, contributor-category exclusions, and a 30-day contribution-refund policy.[3]

**REPORTED (third-party operator evidence):** The Social Change Agency/The Social Change Nest describes its Open Collective fiscal-hosting offering as useful for quick setup, receiving grants, paying out money, transparent records, collaborative admin rotation, and a network of 300+ groups. This is a service provider’s implementation testimony, **not** an independent audit of Open Collective’s platform controls.[9]

### Governance model; membership, roles, delegation, and recruiting

**OBSERVED:** At platform level, OFiCo says it owns the platform and is governed by member organizations that depend on it; certified fiscal hosts participate in governance and receive a trust indicator.[2] The October 2024 transition post says the nonprofit would run the platform for members and the larger community.[8]

**OBSERVED:** At operational level, the model separates **Collective admins/core contributors** from **Fiscal Host admins**. Collective approval and host review/payment can be made distinct; host policy can mandate multiple admins and block self-approval at the Collective level.[2] [3]

**INFERRED:** This is a **delegated financial-governance** model rather than a generalized deliberative-democracy system. It is strong at explicit financial authority boundaries but the reviewed material does not evidence constituent representation, county-level delegation chains, consent governance, or participant-led policy formation.

**OBSERVED:** Recruiting mechanics center on collecting contributors, displaying contributors/leaderboards, publishing updates, hosting events, and embedding contribution widgets. The sources reviewed do not document a native candidate pipeline, stakeholder credentialing, territory assignment, or structured volunteer/member onboarding. Those capabilities are **unverified**, not absent from all possible custom integrations.[1]

### Treasury and fund management

**OBSERVED:** This is the strongest platform in the set for real-money operations. Funds are legally held by the Fiscal Host; the platform provides budget/expense tracking, reporting, and bookkeeping automation. The host, not the Collective alone, bears legal and compliance responsibility.[2]

**REPORTED:** The 2024 platform-transfer announcement says platform fees and platform tips on the current branch would go to the community-managed nonprofit, while each Fiscal Host sets its own fees.[2] [8] **UNVERIFIED:** Current OFiCo funding mix, reserves, and audited accounts were not established from the reviewed public sources.

**INFERRED:** Public transaction transparency improves accountability but can conflict with privacy-sensitive payments, sensitive stakeholder incentives, or county-level claims. A Kimosabe design must explicitly separate what is public, member-visible, host-visible, and confidential.

### Hosting, APIs, and extension surfaces

**OBSERVED:** Open Collective provides a public GraphQL endpoint and OAuth 2.0 Authorization Code flow with PKCE. OAuth scopes cover account, expenses, orders, transactions, virtual cards, updates, conversations, webhooks, and Fiscal Host administration; scopes constrain access and do not add privileges beyond the authorizing user’s role.[4]

**OBSERVED:** The frontend and API code are public under MIT.[5] [7] **INFERRED:** This gives a capable integration boundary for a custom marketing/recruiting portal. **UNVERIFIED:** The reviewed documentation did not establish a supported, production-ready self-hosting program for the complete financial stack; source availability must not be treated as a low-risk substitute for qualified fiscal operations.

### Business model and funding

**OBSERVED:** Fiscal Hosts independently choose fees, while platform-level documentation identifies platform fees/tips as a revenue source for the OFiCo-managed branch.[2] [8]

**INFERRED:** This creates an aligned but potentially complex multi-party economics: the public-benefit operator, the fiscal host, and the software steward may each need sustainable revenue. The reviewed sources do not disclose current platform pricing, fee schedules, or audited financials, so unit economics are **unverified**.

### Strengths

- **OBSERVED:** Deepest documented combination of transparent budgets, contribution intake, expense review, receipts, reports, and host compliance workflow in this three-platform set.[1] [2]
- **OBSERVED:** Fine-grained policy controls can enforce multi-admin and anti-self-approval safeguards before a Collective is accepted or expenses are paid.[3]
- **OBSERVED:** OAuth, GraphQL, webhooks, and embeddable contribution surfaces support a separate branded acquisition and community layer.[1] [4]
- **INFERRED:** The legally accountable host/Collective split is a useful structural pattern for a public-benefit organization that wants visible financial stewardship without making every local group a corporation.

### Gaps and unresolved weaknesses

- **REPORTED:** The 2024 closure of a major host and transfer to a new community-governed nonprofit show material ecosystem/continuity risk. Due diligence should cover host solvency, offboarding, data export, fee changes, and operational escalation paths before relying on it for a national program.[8]
- **INFERRED:** It does not evidence a native, territory-aware stakeholder CRM, recruiting journey, referral/claim logic, decision delegation, or seasonal-credit engine.
- **INFERRED:** Public budget defaults need a designed privacy policy for beneficiary payments, donor restrictions, staff compensation, and potentially regulated financial information.
- **UNVERIFIED:** No reviewed source proves that the full production financial stack is readily self-hosted, that the platform supports U.S.-county partitioning at required scale, or that it can represent non-cash community credits safely.

## Loomio

### What it is and who it serves

**OBSERVED:** Loomio is open-source collaboration software for groups to create a focused decision record: groups contain discussions, discussions contain context/replies, and polls/proposals collect preferences, advice, and decisions. It is positioned for membership organizations, self-managing teams, boards/councils, distributed networks, and residential/cooperative communities.[10]

**OBSERVED:** Its decision templates support advice, consent, consensus, and polls/proposals; product materials also list show-of-thumbs, multiple-choice, score, ranked-choice, dot-voting, and time polls. Participants can reply by email, and notifications/outcomes can be sent to Slack, Microsoft Teams, Discord, Matrix, or Mattermost.[11] [12]

### License, primary repository, adoption, and maintenance

**OBSERVED:** The primary repository is [`loomio/loomio`](https://github.com/loomio/loomio), licensed **GNU AGPL v3.0**. On 2026-10-06 it had **2,612 GitHub stars**, **705 forks**, was **not archived**, and was last committed at **2026-10-06 09:09:27 UTC**.[14] [15]

**REPORTED:** Loomio describes itself as an Aotearoa New Zealand worker-owned cooperative. It names World Resources Institute, OpenSSL, NYC DSA, and Raise Recruiting among users; its terms say “thousands of people” use Loomio products daily. These are vendor statements, not independently audited active-user figures.[13] [16]

**REPORTED (third party):** TechSoup offers eligible nonprofits a 50% discount for Loomio Pro and describes its use for asynchronous web/email/mobile discussions, scheduling, document approval, budget decisions, and polling. This is credible nonprofit-sector distribution evidence, but it is not an independent technical/security evaluation.[17]

**INFERRED — activity status: actively maintained:** The core source repository had a same-day functional commit and is not archived. The observed commit repaired notification behavior, which is evidence of ongoing maintenance rather than only documentation churn.[15]

### Governance model; membership, roles, delegation, and recruiting

**OBSERVED:** Loomio’s *product* governance model is process-flexible: an organization can expose advice, consent, consensus, or polling rules and preserve discussion, decision, and rationale together. The platform does not assert that one process is universally correct.[11]

**OBSERVED:** Loomio the *organization* is a worker-owned cooperative. Its handbook describes “dynamic hierarchies by consent”: roles hold defined mandates, are reviewed at least quarterly, coordinators are appointed by co-op members with worker input, and authority ultimately traces to co-op membership. At least two coordinators are required; they can delegate work but are accountable for coordination, financial operations, membership processes, and executing board decisions.[16]

**OBSERVED:** Product groups hold members, discussions, polls, and files; membership organizations can involve members in general-assembly voting. The platform supports automated threads, polls, and memberships through an API, plus email participation and integrations.[10] [12]

**INFERRED:** Loomio is a sound **deliberation and decision-record layer** for county stakeholder groups, but not a full recruiting/CRM system. The reviewed sources do not establish native territory hierarchy, electoral delegation, referral attribution, claim conversion, or structured credential verification beyond account/group management.

### Treasury and fund management

**OBSERVED:** Loomio supports discussion, polls, decisions, and documented “budget decisions,” but reviewed sources do not document a native ledger, payment rail, expense approval, grant disbursement, fiscal sponsorship, or custody function.[11] [17]

**INFERRED:** Treat Loomio decisions as a possible **authorization/audit trail** for a separate General Ledger or treasury system, not as the treasury itself. A decision outcome must not automatically trigger fund movements without role checks, legal policy, and reconciled ledger controls.

### Hosting, APIs, and extension surfaces

**OBSERVED:** Loomio offers cloud hosting in the U.S., EU, and Australia/NZ; a private-host offer with a dedicated server/database, SAML or OAuth SSO, branding/domain options, and regional data-center choices; and self-hosting. It supports CSV, HTML, or JSON history export; an API for threads/polls/memberships; and integrations with several chat tools.[12]

**OBSERVED:** Loomio’s core code is AGPL v3.0 and its repository directs operators to self-host/deployment documentation. The pricing FAQ says Loomio can support self-hosted deployments, but discusses them as a service engagement.[13] [14]

**INFERRED:** For the new organization, a branded private host or self-hosted deployment could give useful decision-record control. AGPL obligations and operational ownership require legal and engineering review before modifying/deploying it as a tightly integrated proprietary service.

### Business model and funding

**OBSERVED:** Loomio Limited sells annual/monthly subscriptions and a private-host offering, while offering 25–50% nonprofit/member-funded discounts. At access date, public nonprofit-oriented pricing listed Starter at $299/year (up to 30 members), Pro at $499/year (up to 300, plus paid member increments), and Private Host at $4,999/year; list prices are higher on the same page.[12] [13]

**OBSERVED:** Terms say subscription fees are prepaid and renew automatically unless canceled. They also say a canceled cloud group cannot start threads/invite members and its active-system content is deleted after 30 days.[13]

**UNVERIFIED:** Current revenue, margins, financial backing, and the precise relationship between commercial subscription proceeds and the worker-cooperative’s governance were not found in the reviewed sources.

### Strengths

- **OBSERVED:** Clear asynchronous path from context to proposal/poll to recorded outcome; it directly supports advice, consent, consensus, and several ballot types.[10] [11]
- **OBSERVED:** Practical low-friction access—email participation, notifications, chat integrations, exports, regional hosting, and multiple languages—supports distributed recruiting and community-management operations.[12]
- **OBSERVED:** The cooperative’s published role/delegation model provides a concrete governance practice to study, rather than a vague “community-led” claim.[16]
- **INFERRED:** Its focused scope reduces the risk of conflating political/social deliberation with actual money custody.

### Gaps and unresolved weaknesses

- **OBSERVED:** No reviewed source establishes native financial custody, transparent budget ledger, expense controls, or fiscal-host workflow.[11] [17]
- **INFERRED:** No evidence of a ready-made county/territory/delegation graph, stakeholder designation taxonomy, seasonal-credit accounting, or claim/conversion mechanics.
- **OBSERVED:** Cloud cancellation/deletion timing requires deliberate export/retention policy; this is especially important for governance records and public-benefit accountability.[13]
- **INFERRED:** The public tier’s member limits and additional-member pricing may be unsuitable for a national stakeholder network without a separate scale/cost assessment.
- **UNVERIFIED:** No load/performance, accessibility, moderation-abuse, or secure-voting assurance at the proposed national scale was established from reviewed sources.

## Decidim

### What it is and who it serves

**OBSERVED:** Decidim is a free/libre, open-source participatory-democracy framework for public or private organizations, including cities, associations, universities, NGOs, trade unions, neighborhood associations, and cooperatives. It organizes participation through spaces—processes, assemblies, votings, and initiatives—and modular components such as proposals, comments, meetings, surveys, results, accountability, participatory text, newsletters, and sortition.[18]

**REPORTED:** The Decidim Association says the project began with Barcelona’s 2016 participation platform, was constituted as an association in 2019, and has been embraced by **over 450 cities and organizations globally**. This is an official project claim, not a separately audited deployment census.[24]

**REPORTED (independent institutional and academic context):** The EU Open Source Observatory describes Decidim as a collaboratively built, free-software public-commons infrastructure for civic participation in public/private organizations with hundreds or thousands of participants.[27] An academic case study of Decidim Barcelona found that negatively aligned comments were more likely to generate discussion cascades, supporting deliberation in that studied interface.[28]

### License, primary repository, adoption, and maintenance

**OBSERVED:** The primary repository is [`decidim/decidim`](https://github.com/decidim/decidim), a Ruby on Rails framework under **GNU AGPL v3.0**. On 2026-10-06 it had **1,829 GitHub stars**, **487 forks**, was **not archived**, and its latest commit was **2026-10-06 04:43:54 UTC**.[22] [23]

**INFERRED — activity status: actively maintained:** Same-day repository activity, current installation guidance through v0.29, and a named nonprofit responsible for source-code maintenance support an active classification.[21] [23] **Caveat — OBSERVED:** The latest sampled commit was a dependency update by Dependabot, so it alone is not evidence of active feature work; a future technical due-diligence pass should review release cadence, unresolved security issues, and human-maintainer throughput.[23]

### Core capabilities

**OBSERVED:** Participatory Processes are phased workflows that can combine components for strategic planning, participatory budgeting, elections, regulation writing, public-policy design, and other initiatives. Assemblies document recurring bodies/working groups, composition, agendas, meetings, and decisions. Initiatives let participants define goals, gather endorsements, and promote/discuss them.[18]

**OBSERVED:** Proposal workflows can include creation wizards, comparison, attached documents/images, geolocation, collaborative incubation, filtering, comments, and support/voting rules. Voting can be unlimited, threshold-limited, weighted, or cost-based. Results can receive official acceptance/rejection responses, and Accountability tracks project/result progress.[18]

**OBSERVED:** Decidim’s module catalog describes optional engines including a GraphQL API, accountability, assemblies, blogs, comments, conferences, consultations, debates, initiatives, meetings, processes, proposals, and sortition. The core user/organization engine is required; other modules are optional.[29]

### Governance model; membership, roles, delegation, and recruiting

**OBSERVED:** The Decidim Free Software Association is a nonprofit responsible for maintaining source code and fostering the community. The project’s social-contract framing commits partners to free/open code, transparent/traceable/integral participation content, equal opportunity and accessibility, privacy with verification, and accountable institutional responses. The white paper describes MetaDecidim as the platform community used to organize the project itself.[24] [25]

**OBSERVED:** A Decidim instance distinguishes visitors, registered participants, and verified participants. Registered participants can propose/comment, attend meetings, endorse, follow, receive notifications and private messages; verified participants can make decisions. Administrators can selectively set permissions for registered vs. verified users, and Decidim documents a public register of administrative activity for auditability.[19]

**OBSERVED:** Participants can join verified user groups/collectives and act in their own or a group name. Documentation says groups can manage permissions/administration roles, private debate spaces, and shared group information—but labels parts of that group feature **“currently missing.”** Therefore, current production completeness of that group-management capability is **unverified** and must be tested against the targeted release.[19]

**INFERRED:** Decidim provides the strongest native structure for public recruitment-to-participation: open visitor awareness, registered onboarding, verification-gated rights, initiative promotion/endorsement, notifications, meetings, newsletters, and a documented public accountability loop. It still requires an organization-specific operating model for recruiter assignments, eligibility, outreach attribution, and jurisdictional verification.

### Treasury and fund management

**OBSERVED:** Decidim supports participatory budgeting as a **deliberation/allocation process**, cost-based voting, accepted-result tracking, and accountability progress—not a native financial-custody/expense-payment system in the reviewed sources.[18] [25]

**INFERRED:** It can govern “what should be funded” and publish progress, but it should not be adopted as a General Ledger, payout processor, grant administrator, or community-credit ledger without an integrated treasury subsystem.

### Hosting, APIs, and extension surfaces

**OBSERVED:** Decidim is self-deployable. Its manual install guidance identifies PostgreSQL, Ruby, Node.js, ImageMagick, and browser/driver requirements; production deployment additionally needs web serving, backups, monitoring, server administration, and security operations.[21]

**OBSERVED:** Its per-instance GraphQL API is public/read-only by default. Writes/mutations require authenticated API users via OAuth (for participant-facing apps) or protected API credentials (for machine-to-machine automation); documentation warns that machine credentials are highly sensitive and should be rotated.[20]

**OBSERVED:** Decidim is explicitly modular, with optional engines and custom modules. Its API can vary by instance/version, and the default API rate limit is documented as 100 requests/minute/IP, though an instance may change it.[20] [29]

**INFERRED:** Decidim offers the broadest extension surface for independently designed territory, season, claim, and campaign modules. That flexibility comes with a significant implementation/operations burden and should not be confused with a ready-to-run national service.

### Business model and funding

**OBSERVED:** Decidim is a nonprofit-governed FLOSS/public-commons project rather than a single hosted SaaS offer in the reviewed sources. The Association says it maintains code, fosters the community, and collaborates on participatory design, installation, research, governance-of-commons, and related work.[24]

**REPORTED (official governance forum, current date on post not verified):** A MetaDecidim economic-sustainability discussion says the Association was highly dependent on public funding, citing €100k from Barcelona City Council and €50k from Generalitat de Catalunya, while identifying loss of funding/changes in government as risk and calling for diversification. Treat those amounts as historical forum assertions—not current financial statements.[26]

**UNVERIFIED:** Current audited finances, current public grants, service-provider revenue, donation income, and the Association’s current sustainability plan were not established in this review.

### Strengths

- **OBSERVED:** Richest civic-participation toolkit: phased processes, assemblies, initiatives, verified participation, proposals, endorsement, multiple voting approaches, meetings, newsletters, and accountability.[18] [19]
- **OBSERVED:** Social-contract norms make traceability, public response, accessibility, privacy, and verification explicit design commitments rather than incidental features.[25]
- **OBSERVED:** AGPL source, self-host deployment, OAuth/machine-to-machine GraphQL, and optional modules support independently designed extensions.[20] [21] [29]
- **REPORTED:** It has credible civic adoption signals: the project reports 450+ organizations/cities, and the EU Open Source Observatory characterizes it as an active community-maintained public-commons infrastructure.[24] [27]

### Gaps and unresolved weaknesses

- **OBSERVED:** It is not a payment, fiscal-hosting, expense-approval, or custody system in the reviewed materials.[18] [25]
- **OBSERVED:** Production self-hosting needs competent infrastructure/security operations beyond local installation; this raises cost and delivery risk.[21]
- **REPORTED:** The Association’s own sustainability forum describes dependency on a limited public-funding base as risk; current exposure is unverified.[26]
- **OBSERVED/UNVERIFIED:** One participant/group documentation page contains dated-looking planned/missing-feature statements. Do not assume gamification or user-group administration is current without release-specific acceptance testing.[19]
- **INFERRED:** Generic civic participation and electoral/voting components require careful U.S. legal, accessibility, identity, anti-coercion, and moderation analysis before use in any benefits, credits, claims, or binding allocation program.

## Relevance to a Kimosabe/Human Blockchain marketing, recruiting and management organization

### ADOPT

- **ADOPT — transparent public-benefit financial reporting, not a wholesale platform:** **OBSERVED** Open Collective’s visible budget/receipt/report pattern and host-reviewed expense workflow are the best precedent for a public-facing General Ledger view.[1] [2] **INFERRED:** Publish aggregated revenue, approved programs, season budgets, commitments, and execution status; protect private beneficiary/staff/payment data by default.
- **ADOPT — dual authority for real money:** **OBSERVED** Open Collective can enforce multiple admins and restrict self-approval while separating Collective and Host review.[3] **INFERRED:** Require at least two authorized approvers for material disbursements and a separate compliance/finance authority from local campaign operators.
- **ADOPT — a durable decision record:** **OBSERVED** Loomio keeps proposal, context, input, vote, outcome, and reasoning in one record and accommodates consent/advice/consensus rather than forcing one ballot style.[11] **INFERRED:** Give every county/territory governance action a linked decision record and clearly show whether it is advisory, delegated, or binding.
- **ADOPT — lifecycle-based participation and accountability:** **OBSERVED** Decidim connects proposals, results, official responses, and execution progress in configured participatory spaces.[18] **INFERRED:** Map campaign and community work to transparent states: discover → recruit → verify → claim/propose → deliberate → authorize → execute → reconcile → report.
- **ADOPT — graduated participation rights:** **OBSERVED** Decidim distinguishes visitor, registered, and verified participation and can restrict action by verification status.[19] **INFERRED:** Use public audiences for marketing, registered members for local discussion, and verified/credentialed stakeholders for sensitive claims, governance, or benefits.

### ADAPT

- **ADAPT — fiscal-host concept into a U.S. public-benefit operating model:** **OBSERVED** Open Collective separates a legal host’s compliance obligation from a Collective’s community activity.[2] **INFERRED:** The new organization can act as an operating steward and recruiting/community-services provider, while qualified legal entities and written agreements govern actual funds. **Do not assume** that becoming a fiscal host is appropriate without nonprofit/tax, money-transmission, employment, grant-compliance, and state-law advice.
- **ADAPT — Loomio’s dynamic consent model to territory roles:** **OBSERVED** Loomio’s cooperative publishes role mandates, rotating responsibility, and consent-based coordination.[16] **INFERRED:** Define county roles such as outreach steward, stakeholder verifier, discussion facilitator, claims reviewer, finance liaison, and escalation lead; attach mandates, scope, term, training, and revocation rules to each role. This is an independent governance design, not a copy of Loomio’s co-op structure.
- **ADAPT — Decidim’s participation spaces to seasonal loops:** **OBSERVED** Decidim supports phased processes, assemblies, initiatives, endorsement, voting, and accountability.[18] **INFERRED:** Model each season as a configurable campaign/process with county scoping, explicit gates and outcome states. Use existing civic patterns as inspiration, but create an original UX, terminology, rulebook, and data model for claims/conversions.
- **ADAPT — APIs as controlled integration boundaries:** **OBSERVED** Open Collective offers OAuth/GraphQL/webhooks, Loomio offers an API for threads/polls/memberships, and Decidim supports OAuth plus protected machine-to-machine GraphQL mutations.[4] [12] [20] **INFERRED:** Build a canonical internal identity, role, territory, consent, and ledger-event model; integrate outward through least-privilege adapters rather than making any one external platform the system of record.
- **ADAPT — promotion mechanics:** **OBSERVED** Open Collective offers embeddable contribution components/updates, Loomio supports notifications and chat/email participation, and Decidim has initiatives, newsletters, meetings, blogs, and notifications.[1] [12] [18] **INFERRED:** Use an independent campaign toolkit that combines local landing pages, consented invitation/referral codes, cohort onboarding, event follow-up, and public progress stories, all tied to verified territory and source attribution.

### REJECT

- **REJECT — treating a community credit or claim as cash, a donation, or a hosted balance by default:** **INFERRED:** Open Collective’s rails are designed for legally held money; using them as a proxy for seasonal credits could create accounting, tax, consumer-protection, and user-expectation problems. Keep credit issuance/conversion rules in a purpose-built, auditable subsystem until counsel and policy owners approve their legal treatment.
- **REJECT — using Loomio as the General Ledger or treasury:** **OBSERVED** Its reviewed capabilities are decision collaboration, not fund custody or payout controls.[11] **INFERRED:** Decision records may authorize ledger actions, but cannot replace double-entry accounting, reconciliation, controls, and a legal custodian.
- **REJECT — directly adopting generic public voting for benefits, claim conversion, or high-stakes resource allocation:** **INFERRED:** Decidim’s voting tools are valuable examples, but a U.S. county stakeholder program needs independently specified eligibility, identity assurance, appeal, anti-coercion, conflict-of-interest, accessibility, moderation, and audit procedures first.
- **REJECT — opaque “growth at any cost” recruitment:** **OBSERVED** Decidim’s social contract stresses equal opportunity and privacy/verification, while Loomio stresses meaningful participation.[19] [25] **INFERRED:** The new organization should not reward recruiters merely for raw enrollment; measure verified, informed, retained, and appropriately consented participation.

### DEFER

- **DEFER — selection of a fiscal host or becoming a host:** **REPORTED** The Open Collective ecosystem experienced a major host closure/organizational transfer in 2024.[8] **INFERRED:** Conduct host-specific legal, financial, geographic, payment-rail, insurance, privacy, exit, and service-level diligence before integration.
- **DEFER — self-hosting an AGPL participation stack at national scale:** **OBSERVED** Decidim requires real operational capability, and both Loomio and Decidim use AGPL.[14] [21] **INFERRED:** First establish target user volumes, verification method, moderation model, records-retention schedule, incident response, accessibility criteria, and licensing plan; then run a county pilot with measurable readiness gates.
- **DEFER — automated policy/ledger mutations:** **OBSERVED** Decidim documents highly sensitive machine credentials and OAuth participant-authorized writes; Open Collective scopes include expense/transaction/host powers.[4] [20] **INFERRED:** Do not automate payouts, credit conversions, eligibility changes, or rights revocations until least-privilege controls, approval queues, immutable event logs, monitoring, and rollback/reversal rules are acceptance-tested.
- **DEFER — assertions of adoption, cost, or sustainability beyond sourced facts:** **OBSERVED/UNVERIFIED:** No audited active-user counts, national-scale performance benchmarks, current audited finances, or Kimosabe-specific implementation evidence was found for any of the three platforms. Treat pilots and user research—not GitHub stars—as the decision gate.

## Sources

[1]: https://opencollective.com/how-it-works "Open Collective — How Open Collective works; accessed 2026-10-06"

[2]: https://documentation.opencollective.com/fiscal-hosts/fiscal-hosts "Open Collective documentation — Fiscal Hosts; accessed 2026-10-06"

[3]: https://documentation.opencollective.com/fiscal-hosts/setting-up-a-fiscal-host/fiscal-host-policies "Open Collective documentation — Fiscal Host Policies; accessed 2026-10-06"

[4]: https://documentation.opencollective.com/development/oauth "Open Collective documentation — OAuth; accessed 2026-10-06"

[5]: https://api.github.com/repos/opencollective/opencollective-frontend "GitHub API — opencollective/opencollective-frontend metadata; accessed 2026-10-06"

[6]: https://api.github.com/repos/opencollective/opencollective-frontend/commits?per_page=1 "GitHub API — latest opencollective/opencollective-frontend commit; accessed 2026-10-06"

[7]: https://api.github.com/repos/opencollective/opencollective-api "GitHub API — opencollective/opencollective-api metadata; accessed 2026-10-06"

[8]: https://blog.opencollective.com/the-open-collective-platform-is-moving-to-a-community-governed-non-profit/ "Open Collective blog — The Open Collective Platform is moving to a community governed non-profit; accessed 2026-10-06"

[9]: https://thesocialchangeagency.org/what-we-do/support-for-groups-and-movements/fiscal-hosting/ "The Social Change Agency — Fiscal hosting; accessed 2026-10-06"

[10]: https://help.loomio.org/en/ "Loomio Help — Getting started; accessed 2026-10-06"

[11]: https://www.loomio.com/collaborative-decision-making/ "Loomio — Collaborative decision-making software; accessed 2026-10-06"

[12]: https://www.loomio.com/pricing/ "Loomio — Pricing for collaborative organizations; accessed 2026-10-06"

[13]: https://www.loomio.com/docs/en/policy/terms "Loomio — Terms of Service; accessed 2026-10-06"

[14]: https://api.github.com/repos/loomio/loomio "GitHub API — loomio/loomio metadata; accessed 2026-10-06"

[15]: https://api.github.com/repos/loomio/loomio/commits?per_page=1 "GitHub API — latest loomio/loomio commit; accessed 2026-10-06"

[16]: https://www.loomio.coop/coordination.html "Loomio Cooperative Handbook — Coordination at Loomio; accessed 2026-10-06"

[17]: https://www.techsoup.org/loomio "TechSoup — Loomio nonprofit offer; accessed 2026-10-06"

[18]: https://decidim.org/features/ "Decidim — Features; accessed 2026-10-06"

[19]: https://docs.decidim.org/en/develop/features/participants.html "Decidim documentation — Participants; accessed 2026-10-06"

[20]: https://docs.decidim.org/en/develop/develop/api/authentication.html "Decidim documentation — Authentication with the API; accessed 2026-10-06"

[21]: https://docs.decidim.org/en/develop/install/manual.html "Decidim documentation — Manual installation tutorial; accessed 2026-10-06"

[22]: https://api.github.com/repos/decidim/decidim "GitHub API — decidim/decidim metadata; accessed 2026-10-06"

[23]: https://api.github.com/repos/decidim/decidim/commits?per_page=1 "GitHub API — latest decidim/decidim commit; accessed 2026-10-06"

[24]: https://decidim.org/about/ "Decidim — About the Association; accessed 2026-10-06"

[25]: https://docs.decidim.org/en/develop/whitepaper/decidim-a-brief-overview.html "Decidim documentation — A brief overview / white paper; accessed 2026-10-06"

[26]: https://meta.decidim.org/en/processes/sustainability-governance/f/1795/debates/245?commentId=26053 "MetaDecidim — Economic sustainability discussion; accessed 2026-10-06"

[27]: https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/decidim "EU Interoperable Europe / OSOR — Decidim profile; accessed 2026-10-06"

[28]: https://arxiv.org/abs/1707.06526 "Aragón et al. — The case study of the online discussions in Decidim Barcelona; accessed 2026-10-06"

[29]: https://decidim.org/modules/ "Decidim — Modules; accessed 2026-10-06"

[30]: https://api.github.com/repos/opencollective/opencollective "GitHub API — opencollective/opencollective metadata; accessed 2026-10-06"
