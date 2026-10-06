# Kimosabe Commons

Research, business plan, product specification and live website for **Kimosabe Commons, PBC** — a proposed
Delaware public benefit corporation that provides the marketing, recruiting, promotion, community
management and governance operations for the Kimosabe App and the Human Blockchain.

> **Every address is a stakeholder. Every stakeholder gets a job.**

**Live site:** https://commons-jjkmfh2h.manus.space
**Document index:** [docs/README.md](docs/README.md) — all 18 documents, with reading paths by role

---

## What this repository is

This is the complete working package for the engagement *"research the top five open-source DAO
management platforms and propose a startup public benefit business, including business plan, SRS,
PRD and website."* It contains the research that answered the question, the company proposed on the
back of it, the specification for the software that company would run, and the delivered website.

**Nothing in this repository is legal, accounting, insurance, securities or tax advice.** Kimosabe
Commons, PBC is a **proposed** entity. Every roster, seat, territory and financial figure in the
documents and on the website is labelled model output or illustrative sample data.

---

## Start here

Read **[`docs/00-START-HERE-MASTER-HANDOFF.md`](docs/00-START-HERE-MASTER-HANDOFF.md)** first. It is
the executive brief: what was researched, what is proposed, where every artifact lives, which
decisions remain open, and the pre-season gate checklist.

For the whole set with suggested reading order, use the
**[document index](docs/README.md)**.

---

## The finding

The five leading open-source DAO management platforms — Aragon, DAOhaus, Colony, DAOstack, and
Snapshot with Tally — plus the adjacent public-benefit set (Open Collective, Loomio, Decidim) are
all *governance* tools. None of them provides a recruiting funnel, campaign attribution, territory
administration, verified real-world identity and licensure, seasonal credit accounting, or a general
ledger.

> **The gap is not governance. The gap is the roster.**

Kimosabe Commons is proposed to fill that gap: the layer that turns a map of people and addresses
into a verified roster — who is licensed, who owns the claim, who can act, what territory they hold,
and what they completed this season.

**The chartered public benefit:**

> Increasing the number of verified, address-anchored, lawfully organized participants who can
> convert a documented community Need into a documented, evidenced Done — measured as verified
> stakeholder activations, evidenced completions, and retained participation per territory per
> season.

---

## Repository layout

```
README.md                              This file
docs/README.md                         Document index and reading paths
docs/
  00-START-HERE-MASTER-HANDOFF.md      Executive brief and index — read this first
  00-PROJECT-INSTRUCTION-MANUAL.md     The governance constitution for the engagement
  ENGAGEMENT-BRIEF.md                  Shared context every author worked from
  10-business/
    BUSINESS-PLAN.md                   The governing business plan
    ENTITY-AND-GOVERNANCE.md           Entity architecture, charter, board, boundaries
    GTM-AND-CHANNELS.md                Positioning, funnel, channels, seasonal calendar
  20-product/
    SRS.md                             Requirements specification (76 FR / 13 NFR)
    PRD.md                             Product requirements, personas, releases
    ROLE-PERMISSION-MATRIX.md          Entity classification and the permission matrix
    DATA-AND-LEDGER-MODEL.md           Entities, identifiers, events, ledger, reset model
    ADVERSARIAL-REVIEW.md              18 findings, trust boundaries, pre-season gate
  research/
    00-dao-platform-landscape.md       Comparative study and differentiation thesis
    01-01-aragon.md                    Evidence report
    02-02-daohaus.md                   Evidence report
    03-03-colony.md                    Evidence report
    04-04-daostack.md                  Evidence report
    05-05-snapshot-tally.md            Evidence report
    06-06-public-benefit-adjacent.md   Evidence report

site/                                  Website source snapshot (see below)
```

Every document above is browsable and linked from the **[document index](docs/README.md)**.

---

## The website

[`site/`](site) is a snapshot of the source for the live site: React 19 + Vite, Express + tRPC,
Drizzle ORM on managed MySQL, TypeScript and Tailwind 4.

It carries the public explanation of the company, a browsable territory register, the roster
application and the sponsor inquiry — both forms persisting to a real database with reference codes,
consent records, timestamp and source attribution, reviewed through an authenticated admin screen.
Server-rendered per-route metadata, a crawler-readable pre-hydration content block, sitemap, robots
and the platform route manifest are included. The design ("Civic Ledger") and the implementation
plan are recorded in [`site/plan.md`](site/plan.md).

The site is the top of funnel only. The back-office operations system described in the SRS and PRD
is a separate build.

### Running the site locally

```bash
cd site
pnpm install
# provide DATABASE_URL for a MySQL instance, then:
pnpm db:push
pnpm dev            # http://localhost:3000
```

---

## Content discipline

The documents and the site are held to a written rule: **no investment or securities language** (no
invest, ROI, equity, return, yield or token sale); **no claim of endorsement** by a regulator,
insurer, bank or institution; and **no implication** that the company is an insurer, adjuster,
escrow agent or money transmitter. Participation is described as sponsorship or participation and
confers no equity, token, return or share of revenue.

---

## The decisions that remain open

1. Form the entity or run the first season inside an existing one.
2. The name, cleared by counsel before filing.
3. The real first-season territories — drawn from ground already held, not from the sample register.
4. Seat price and season terms, priced against one real cost base.
5. The founder-IP agreement: licensed, contributed or assigned.
6. Board composition and timing.
7. The capital pathway, if any — this engagement deliberately did not design one.