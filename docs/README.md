# Kimosabe Commons — Document Index

The complete written package for the Kimosabe Commons engagement: **18 documents, roughly 81,000
words**, organised as one system described at four altitudes — *governance of the work*, *market*,
*money*, and *machine*.

> **Read [`00-START-HERE-MASTER-HANDOFF.md`](./00-START-HERE-MASTER-HANDOFF.md) first.** It is the
> executive brief: the finding, the proposal, the artifact map, the open decisions and the
> pre-season gate. Everything below is the supporting depth.

**Nothing in this document set is legal, accounting, insurance, securities or tax advice.**
Kimosabe Commons, PBC is a proposed entity. Every market size, unit economic, budget and forecast
figure is model output built from labelled assumptions.

---

## Reading paths

| If you are… | Read, in this order |
|---|---|
| **The founder, short on time** | [Master handoff](./00-START-HERE-MASTER-HANDOFF.md) → [Adversarial review](./20-product/ADVERSARIAL-REVIEW.md) → [Business plan](./10-business/BUSINESS-PLAN.md) |
| **Deciding whether to form the entity** | [Master handoff](./00-START-HERE-MASTER-HANDOFF.md) → [Entity and governance](./10-business/ENTITY-AND-GOVERNANCE.md) → [Business plan](./10-business/BUSINESS-PLAN.md) |
| **Raising or recruiting sponsors** | [Business plan](./10-business/BUSINESS-PLAN.md) → [Go-to-market](./10-business/GTM-AND-CHANNELS.md) → [Benefit report on the live site](https://commons-jjkmfh2h.manus.space/benefit-report) |
| **Building the software** | [SRS](./20-product/SRS.md) → [Data and ledger model](./20-product/DATA-AND-LEDGER-MODEL.md) → [PRD](./20-product/PRD.md) → [Role and permission matrix](./20-product/ROLE-PERMISSION-MATRIX.md) → the [website source repository](https://github.com/donaldhaight/kimosabe-commons-site) |
| **Reviewing the research basis** | [Landscape synthesis](./research/00-dao-platform-landscape.md) → the six evidence reports → [Adversarial review](./20-product/ADVERSARIAL-REVIEW.md) |
| **Handing this to another session or person** | [Master handoff](./00-START-HERE-MASTER-HANDOFF.md) → [Engagement brief](./ENGAGEMENT-BRIEF.md) → [Instruction manual](./00-PROJECT-INSTRUCTION-MANUAL.md) |

---

## Governance of the engagement

| Document | Words | What it is |
|---|---:|---|
| [Project instruction manual](./00-PROJECT-INSTRUCTION-MANUAL.md) | 3,879 | The constitution of the work: naming, voice, visual identity, artifact set, specification standard, prohibited-claims register and working protocols. Later documents do not renegotiate their own shape. |
| [Engagement brief](./ENGAGEMENT-BRIEF.md) | 1,677 | The shared context every author worked from: the company, the domain model, the entity reality and the hard constraints. |
| [Master handoff and executive brief](./00-START-HERE-MASTER-HANDOFF.md) | 2,238 | **Start here.** The finding, the proposal, where every artifact lives, the seven open decisions and the pre-season gate checklist. |

---

## Business — the money altitude

| Document | Words | What it is |
|---|---:|---|
| [Business plan](./10-business/BUSINESS-PLAN.md) | 7,356 | The governing plan: problem, market arithmetic, competitive landscape, operating model, revenue and unit economics, break-even sensitivity, entity strategy, risks, three-year scenarios and the first ninety days. |
| [Entity and governance](./10-business/ENTITY-AND-GOVERNANCE.md) | 4,463 | Entity architecture, why a public benefit corporation, charter language drafted for counsel, board and delegation, the sponsorship-versus-securities boundary, the founder-IP boundary and the prohibited governance patterns. |
| [Go-to-market and channels](./10-business/GTM-AND-CHANNELS.md) | 4,494 | Positioning, the funnel, seven channels, the twelve-month seasonal campaign calendar, the founding-seat programme and the prohibited-claims wall. |

---

## Product — the machine altitude

| Document | Words | What it is |
|---|---:|---|
| [SRS — software requirements specification](./20-product/SRS.md) | 9,000 | 76 functional requirements and 13 non-functional requirements, the data model, event catalogue, architecture decision records and the traceability matrix. |
| [PRD — product requirements](./20-product/PRD.md) | 6,979 | Personas, journeys, screen inventory, release slices, acceptance criteria and the explicit out-of-scope list. |
| [Role and permission matrix](./20-product/ROLE-PERMISSION-MATRIX.md) | 4,466 | Group-versus-Designation classification for every entity, the full permission matrix, authorization scope, separation of duties and abuse cases. |
| [Data and ledger model](./20-product/DATA-AND-LEDGER-MODEL.md) | 4,476 | Entities, the ER model, the identifier scheme, the event catalogue, the ledger candidate and reconciliation model, the seasonal reset model and retention. |
| [Adversarial review](./20-product/ADVERSARIAL-REVIEW.md) | 4,086 | 18 findings across six lenses, trust boundaries, residual risk and the pre-season gate checklist. **Read this alongside the business plan — it is the useful one.** |

---

## Research — the market altitude

| Document | Words | What it is |
|---|---:|---|
| [Open-source DAO platform landscape](./research/00-dao-platform-landscape.md) | 4,485 | The comparative study: capability matrix, five reusable patterns, five gaps, the differentiation thesis, and the maintenance and licensing risk. |
| [Aragon](./research/01-01-aragon.md) | 3,424 | Evidence report — AGPL-3.0. Modular on-chain governance, plugin permissions, function-level separation of powers. |
| [DAOhaus](./research/02-02-daohaus.md) | 3,300 | Evidence report — GPL-3.0. Moloch v3 / Baal: minimalist membership and treasury, segregated funds, differentiated rights. |
| [Colony](./research/03-03-colony.md) | 3,576 | Evidence report — GPL-3.0. Task-and-team work organisation, scoped budgets, independent evaluation of completed work. |
| [DAOstack](./research/04-04-daostack.md) | 3,333 | Evidence report — GPL-3.0, default branch dormant since 2021–2022. Read as a pattern, never depended on. |
| [Snapshot and Tally](./research/05-05-snapshot-tally.md) | 4,103 | Evidence report — MIT. Off-chain signalling with delegation; Tally wound down and was rebranded Cactus in 2026. |
| [Public-benefit and civic platforms](./research/06-06-public-benefit-adjacent.md) | 4,611 | Evidence report — Open Collective, Loomio, Decidim. Fiscal-host separation with dual approval of real money, durable decision records, verified participation tiers. |

---

## The website

The live site is **https://commons-jjkmfh2h.manus.space** and its source sits in
**[donaldhaight/kimosabe-commons-site](https://github.com/donaldhaight/kimosabe-commons-site)** (private)
— React 19 + Vite, Express + tRPC, Drizzle on managed MySQL.

It carries the public explanation of the company, a browsable territory register, the roster
application and the sponsor inquiry, both persisting to a real database with reference codes,
consent records, timestamp and source attribution, reviewed through an authenticated admin screen.

That repository is canonical: the Manus webdev project publishes and checkpoints directly into it,
so it always holds the deployed code. An earlier snapshot lived beside these documents; it was
removed so the two cannot diverge.

---

## Content discipline

Every document here is held to a written rule, and the site is held to the same one. **No investment
or securities language** — no invest, ROI, equity, return, yield or token sale. **No claim of
endorsement** by a regulator, insurer, bank or institution. **No implication** that the company is an
insurer, adjuster, escrow agent or money transmitter. Participation is described as sponsorship or
participation and confers no equity, token, return or share of revenue.

Claims are marked `REPORTED`, `INFERRED` or `ASSUMED`, and each document closes with an explicit
open-questions block listing what it could not resolve.
