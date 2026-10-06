---
id: kimosabe-commons-master-handoff-001
title: Kimosabe Commons — Master Handoff and Executive Brief
owner: Donald Haight
prepared_by: Manus
status: founder-working-draft
sensitivity: internal
created: 2026-10-06
source: Open-source DAO platform research and public benefit business engagement
---

# Kimosabe Commons — Master Handoff

Read this first. It states what was researched, what is being proposed, where every
artifact lives, which decisions are still open, and what to do next.

**Nothing in this engagement is legal, accounting, insurance or securities advice.**

## Contents

1. [The answer in one page](#1-the-answer-in-one-page)
2. [What the research actually found](#2-what-the-research-actually-found)
3. [The company being proposed](#3-the-company-being-proposed)
4. [The artifact set](#4-the-artifact-set)
5. [Decisions only the founder can make](#5-decisions-only-the-founder-can-make)
6. [The pre-season gate](#6-the-pre-season-gate)
7. [Next actions](#7-next-actions)
8. [How to read this document](#8-how-to-read-this-document)

The full document set, with suggested reading order by role, is indexed in
[`README.md`](./README.md).

---

## 1. The answer in one page

You asked for the top five open-source DAO management platforms and a start-up public
benefit business that could market, recruit, promote and manage the Kimosabe App and the
Human Blockchain.

**The research answered the question in an unexpected way.** The five leading open-source
DAO management platforms — **Aragon**, **DAOhaus**, **Colony**, **DAOstack**, and
**Snapshot with Tally** — plus the adjacent public-benefit set (**Open Collective**,
**Loomio**, **Decidim**) are all *governance* tools. Not one of them provides:

- a recruiting funnel with a candidate pipeline;
- campaign operations and source attribution;
- territory administration — who holds which ground, and until when;
- verified real-world identity, licensure and jurisdiction;
- seasonal credit accounting that resets without erasing history;
- a general ledger.

> **The gap is not governance. The gap is the roster.** Every platform knows how to vote on
> a proposal. None of them finds the licensed contractor in Hillsborough County who can do
> the work, verifies that they are who they say they are, gives them a season of ground to
> hold, and proves afterwards that it was done.

That gap is the business. **Kimosabe Commons, PBC** is proposed as the recruiting,
promotion and stewardship layer that sits in front of the ledger — the company that makes
the Human Blockchain's two primitives, People and Addresses, into a roster that actually
exists.

**Chartered public benefit:**

> Increasing the number of verified, address-anchored, lawfully organized participants who
> can convert a documented community Need into a documented, evidenced Done — measured as
> verified stakeholder activations, evidenced completions, and retained participation per
> territory per season.

---

## 2. What the research actually found

### The five platforms, and what each one is actually for

| Platform | Licence | What it is | What it contributed | What we refused |
|---|---|---|---|---|
| **Aragon (OSx / App)** | AGPL-3.0 | Modular on-chain governance with plugins and permissions | Function-level separation of powers: approval and execution as different acts by different authorities; least-privilege execution | Token-weighted governance as default representation |
| **DAOhaus (Moloch v3 / Baal)** | GPL-3.0 | Minimalist, battle-tested on-chain membership and treasury | Segregated funds and differentiated rights — a voting position and an economic position can be different things | Ragequit-style pool draining; unrestricted privileged execution |
| **Colony** | GPL-3.0 | Task-and-team-based work organisation with reputation | Scoped teams and budgets, task specifications, **independent evaluation of completed work**, contribution records that are not transferable capital | Reputation bought with stake; wallet-first onboarding |
| **DAOstack (Alchemy / Arc)** | GPL-3.0 | Curated governance with prediction markets | Explicit authority and constrained actions; auditable proposal lifecycles. Read as a pattern, never depended on — default-branch work stopped in 2021–2022 | Any dependency on it |
| **Snapshot + Tally/Cactus** | MIT (Snapshot) | Off-chain signalling with delegation, and a governance front-end | Gasless signal votes, delegate transparency, lifecycle notification, durable public read paths | Treating an off-chain vote as automatic binding authority. Tally wound down and was rebranded Cactus in 2026 |
| **Open Collective · Loomio · Decidim** | MIT · AGPL-3.0 · AGPL-3.0 | Fiscal hosting, decision records, participatory democracy | Fiscal-host separation with **dual approval of real money**; durable decision records; a participation lifecycle with verified tiers and public accountability reporting | Using any of them as the system of record |

### The five patterns we adopted, and the five we refused

**Adopted:** fiscal-host separation with dual real-money approval · participatory lifecycle
with verified participant tiers and public accountability reporting · scoped teams and
budgets with independent task verification and staged release · least-privilege execution
with signal separated from binding authority · durable, appealable, season-aware
contribution records that are not transferable capital.

**Refused:** token-weighted governance as the default representation for a public benefit ·
public-chain personal operational data · ragequit-style pool draining · wallet-first
onboarding · hosted third-party platforms as the system of record.

### Two risks the research surfaced that you should know about

1. **Maintenance risk.** DAOstack is dormant. The DAOhaus core Baal branch is in selective
   maintenance. Tally wound down and rebranded. **Do not build on any of them.** Adopt
   patterns, own your code.
2. **Copyleft exposure.** Aragon OSx, Loomio and Decidim are AGPL-3.0; Colony, Baal and
   DAOstack are GPL-3.0. Any decision to reuse their *code* rather than their *patterns*
   carries a licence obligation that must be handled deliberately.

---

## 3. The company being proposed

| Field | Value |
|---|---|
| Legal name | **Kimosabe Commons, PBC** |
| Brand | Kimosabe Commons ("The Commons") |
| Software | **The Commons Engine** |
| Form | Delaware public benefit corporation — **proposed, not formed** |
| Function | Marketing, recruiting, promotion, community management and governance operations for the Kimosabe App and the Human Blockchain |
| Tagline | *Every address is a stakeholder. Every stakeholder gets a job.* |

**Four programs:** Recruiting and Roster Operations · Promotion and Campaign Production ·
Territory Stewardship · Attestation and Verification.

**Four audiences:** contractors and crews · sponsors and institutions · civic and county
partners · engineers and agent builders.

**The seasonal clock:** Pre-Season (Jan–Feb) → Season (Mar–Nov) → Cool-Down (Dec 1) →
Dispute Resolution (Dec–Feb) → Reset. At the reset every address returns to Need; roles,
seats and baselines renew; history is never erased. That reset is what keeps the network
recruiting instead of defending.

**How it sits beside what you already own:** Market Applications LLC keeps the technology.
United Stakeholders of America, LLC remains the founder-controlled beta container. RRCA
stays an independent operating company and serves as Customer Zero. Kimosabe Commons
licences or receives rights to founder IP under a written agreement; it does not absorb it.
A DBA is not an entity and creates no equity or liability protection.

**What it is not, in any document, ever:** a token issuer, an investment vehicle, an
insurer, an adjuster, an escrow agent, a money transmitter, a bank, a law firm or a
fiduciary. It does not move money and it does not handle claims.

---

## 4. The artifact set

Everything below lives in this repository's `docs/` folder. Each document ends with an explicit
open-questions block, and each material claim is cited to the research or labelled
`REPORTED`, `INFERRED` or `ASSUMED`.

### Governance of the engagement

| Document | Path | What it is |
|---|---|---|
| Project instruction manual | [`00-PROJECT-INSTRUCTION-MANUAL.md`](./00-PROJECT-INSTRUCTION-MANUAL.md) | The constitution: naming, voice, artifact set, specification standard, prohibited-claims register, working protocols |
| Shared engagement brief | [`ENGAGEMENT-BRIEF.md`](./ENGAGEMENT-BRIEF.md) | The common context every author worked from: company, domain model, entity reality, hard constraints |
| **This document** | [`00-START-HERE-MASTER-HANDOFF.md`](./00-START-HERE-MASTER-HANDOFF.md) | The executive brief and index |

### Research

| Document | Path | What it is |
|---|---|---|
| **Landscape synthesis** | [`research/00-dao-platform-landscape.md`](./research/00-dao-platform-landscape.md) | The comparative study: capability matrix, five reusable patterns, five gaps, differentiation thesis, maintenance and licensing risk |
| Aragon | [`research/01-01-aragon.md`](./research/01-01-aragon.md) | Evidence report |
| DAOhaus | [`research/02-02-daohaus.md`](./research/02-02-daohaus.md) | Evidence report |
| Colony | [`research/03-03-colony.md`](./research/03-03-colony.md) | Evidence report |
| DAOstack | [`research/04-04-daostack.md`](./research/04-04-daostack.md) | Evidence report |
| Snapshot and Tally | [`research/05-05-snapshot-tally.md`](./research/05-05-snapshot-tally.md) | Evidence report |
| Public-benefit and civic platforms | [`research/06-06-public-benefit-adjacent.md`](./research/06-06-public-benefit-adjacent.md) | Evidence report: Open Collective, Loomio, Decidim |

### Business

| Document | Path | What it is |
|---|---|---|
| **Business plan** | [`10-business/BUSINESS-PLAN.md`](./10-business/BUSINESS-PLAN.md) | The governing plan: problem, market arithmetic, competitive landscape, operating model, revenue and unit economics, break-even sensitivity, entity strategy, risks, three-year scenarios, first 90 days |
| Entity and governance | [`10-business/ENTITY-AND-GOVERNANCE.md`](./10-business/ENTITY-AND-GOVERNANCE.md) | Entity architecture, why a PBC, charter language drafted for counsel, board and delegation, the sponsorship-versus-securities boundary, the IP boundary, prohibited governance patterns |
| GTM and channels | [`10-business/GTM-AND-CHANNELS.md`](./10-business/GTM-AND-CHANNELS.md) | Positioning, the funnel, seven channels, the twelve-month seasonal campaign calendar, the founding-seat programme, the prohibited-claims wall |

### Product

| Document | Path | What it is |
|---|---|---|
| **SRS** | [`20-product/SRS.md`](./20-product/SRS.md) | Requirements specification: 76 functional requirements and 13 non-functional requirements, data model, event catalogue, ADRs, traceability matrix |
| **PRD** | [`20-product/PRD.md`](./20-product/PRD.md) | Product requirements: personas, journeys, screen inventory, release slices, acceptance criteria, out-of-scope list |
| Role and permission matrix | [`20-product/ROLE-PERMISSION-MATRIX.md`](./20-product/ROLE-PERMISSION-MATRIX.md) | Group-versus-Designation classification for every entity, the full permission matrix, authorization scope, separation of duties, abuse cases |
| Data and ledger model | [`20-product/DATA-AND-LEDGER-MODEL.md`](./20-product/DATA-AND-LEDGER-MODEL.md) | Entities, ER model, identifier scheme, event catalogue, ledger candidate and reconciliation model, seasonal reset model, retention |
| Adversarial review | [`20-product/ADVERSARIAL-REVIEW.md`](./20-product/ADVERSARIAL-REVIEW.md) | 18 findings across six lenses, trust boundaries, residual risk, and the pre-season gate checklist |

### Website

The live marketing, recruiting and promotion site for Kimosabe Commons is
[**https://commons-jjkmfh2h.manus.space**](https://commons-jjkmfh2h.manus.space), with its source
snapshot in [`../site/`](../site) (Manus Webdev project "Kimosabe Commons"). It carries the
public explanation of the company, the territory browser, the roster application and the
sponsor inquiry — both forms persisting to a real database with an authenticated admin
review screen.

---

## 5. Decisions only the founder can make

These are drawn from the open-questions blocks. They are the questions the engagement
could not answer for you.

1. **Form the entity or not.** Kimosabe Commons, PBC is a proposal. Forming it, delaying
   it, or running the first season inside United Stakeholders of America, LLC is your call
   and changes the sequencing of everything else.
2. **The name.** Kimosabe Commons is the working name. Retained alternates: United
   Stakeholders Growth, PBC · The Stakeholder Guild, PBC · Addressable Commons, PBC ·
   Human Blockchain Growth Foundation. Counsel should clear the name before filing.
3. **The first-season territories.** The plan assumes four states as the wedge — Florida,
   Texas, Georgia, North Carolina — patterned on the sample register. The real set should
   be the counties where RRCA or a known operator already has ground.
4. **Seat price and season terms.** The unit economics are model output. The actual seat
   price, campaign rate and attestation fee need one real cost base to price against.
5. **The IP agreement.** Whether founder IP, domains and brands are licensed, contributed
   or assigned — and on what terms — must be written before a sponsor sees a package.
6. **Board composition.** The proposal is founder plus two independent directors with no
   interest in the founder's other operating companies. Confirm the names and the timing.
7. **The capital pathway.** Any pathway creating economic rights requires securities
   counsel. This engagement deliberately did not design one.

---

## 6. The pre-season gate

Before the first sponsored season closes, the adversarial review requires these to be
closed. They are the difference between a company that can be trusted with a sponsor's
money and one that merely says it can.

- [ ] A formed entity with a bank account and a written delegation matrix.
- [ ] The IP and brand agreement signed between the founder and the company.
- [ ] A conflicted-decision recusal rule in writing, covering RRCA and the founder's other entities.
- [ ] One verified operator with a verified licence in one named county, end to end.
- [ ] A published measurement plan agreed with the first sponsor **before** the season opens.
- [ ] An independent verification role that demonstrably does not verify its own work.
- [ ] Season terms published as a written schedule, reviewed for the sponsorship-versus-securities boundary.
- [ ] The prohibited-claims wall adopted as a written internal rule, not just a web page.

---

## 7. Next actions

**This week** — read the business plan and the adversarial review together. The review is
the useful one; it tells you where the plan is thin.

**Next two weeks** — put the entity and IP questions in front of counsel with the charter
draft and the IP boundary section. Decide the first-season territories from your existing
ground, not from the sample register.

**Next thirty days** — take one county, one operator, one Need and one Done through the
funnel manually. Write down everything the manual process needed. That list is the
Release 1 backlog, and it will be different from the SRS in at least three places. That
difference is the most valuable artifact this engagement can produce.

**Then** — publish the season terms, open the founding-seat conversations, and run the
season on the record.

---

## How to read this document

- **Founder intention** — the naming, the chartered benefit, the four programs and the
  seasonal clock are the intended design. They are proposals, not facts.
- **Model output** — every market size, unit economic, budget and three-year figure in the
  business plan and the GTM plan is model output built from labelled assumptions. None is
  a forecast and none is a guarantee.
- **Verified fact** — the platform licences, the maintenance status of DAOstack and the
  DAOhaus Baal branch, and the Tally/Cactus continuity finding are drawn from the research
  and carry their sources.

Nothing here is legal, accounting, insurance or securities advice. Kimosabe Commons, PBC
is a proposed entity, and the site and the roster contain illustrative sample data only.
