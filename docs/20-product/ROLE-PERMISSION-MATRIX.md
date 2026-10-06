---
id: kimosabe-commons-role-permission-matrix-001
title: Role & Permission Matrix — The Commons Engine
owner: Donald Haight
prepared_by: Manus
status: founder-working-draft
sensitivity: internal
created: 2026-10-06
scope: proposed Kimosabe Commons, PBC and its proposed Commons Engine
---

# Role & Permission Matrix

## Plain-language purpose

This companion specification sets Group/Designation classification, role authority, and platform refusals before a Season. It does not replace the SRS, PRD, entity architecture, contracts, or legal advice.

The proposed company is a recruiting, promotion, territory-stewardship, and attestation operator for the Human Blockchain ecosystem. It is **not** an insurer, claims handler, custodian, escrow agent, bank, money transmitter, investment vehicle, or professional licensing authority. “ClaimBuddy” below means an independent operational verifier; it does not adjust or decide insurance claims. The platform produces workflow records and ledger candidates only; qualified accounting professionals own the books. [SRC — ENGAGEMENT-BRIEF.md]

**Design position.** A Group has a Primary Admin, rules, ledger mapping, roster, and durable record boundary. A Designation is a term- and Territory-bound delegated authority; a G-D may graduate only after meeting stated operating gates. The design independently adapts least privilege and scoped work. [SRC — research/01-01-aragon.md] [SRC — research/03-03-colony.md]

## 1. Scope, terms, and governing decisions

### 1.1 Terms

**Person** is a natural person; **Organization** is an operating record; and **Entity** is a legal-entity record. A **Group** has a Primary Admin, rules, roster, ledger mapping, and durable data boundary. A **Designation** is a revocable Role Assignment within a Group, limited by term and, where relevant, Territory. **G-D** is a Designation with an approved path to become a Group. A **Seat** is seasonal capacity, never property. A **consequential action** changes authority, restricted data, evidence, allocation, publication, or reconciliation.

### 1.2 Decision records

**ADR-031 — Designation is the default for human operating roles.** All named human roles below are Designations unless explicitly classified Group or G-D. This prevents a task title from acquiring a separate budget, data silo, or permanent territorial claim without governance.

**ADR-032 — Legal Entity, Group, and Organization are separate records.** A legal entity may be represented by an Organization record and may sponsor or host a Group, but the three records are not interchangeable. In particular, a DBA is not a legal Entity and grants no separate authority. [SRC — ENGAGEMENT-BRIEF.md]

**ADR-033 — Territory rights are renewable permissions, not ownership.** A Territory Allocation and a Role Assignment both carry an effective window and a Season. The Reset revokes the operative scope unless renewed under the next season’s recorded decision.

### 1.3 Classification test

Classify as **G** only when a category needs its own Primary Admin/rules, roster, account mapping, and durable decision/data boundary. Otherwise it is **D**; it is **G-D** only after an approved graduation charter. A title alone never passes the test.

## 2. Group versus Designation classification

### 2.1 Legal and structural entities

| Entity / category | Class | Group / scope | Time, territory, graduation, and reason |
|---|---|---|---|
| **Kimosabe Commons, PBC** (proposed) | G | Root operating Group | Proposed PBC needs standing rules, programs, accounts, and platform boundary; it does not yet exist. |
| **Market Applications LLC** | G | External Genesis Group | Existing technology Entity; access only by written agreement; not absorbed by branding. |
| **USA LLC** | G | Separate beta-container Group | Existing founder-controlled Entity; its DBAs are neither Entities nor Groups. [SRC — ENGAGEMENT-BRIEF.md] |
| **RRCA** | G | External Customer-Zero Group | Independently owned; participation is contractual, and its revenue/licences/assets remain outside platform ownership. |
| **USA foundation** (future) | G, proposed | Separate future Group | If formed, needs separate governance/accounts and written technology work agreement. |
| **Recruiting & Roster Operations** | G | PBC program Group | Standing applicant, onboarding, and roster rules/accounts. |
| **Promotion & Campaign Production** | G | PBC program Group | Standing campaign, content, communication, and outcome boundary. |
| **Territory Stewardship** | G | PBC program Group | Standing allocation, renewal, dispute, and Reset authority. |
| **Attestation & Verification** | G | PBC program Group | Separate verifier roster/method/reversal boundary preserves independence. |
| **Contractor Organization** | G | Participating Organization Group | Own roster, Company Admin, rules, and contract/account boundary. |
| **Sponsor Organization** | G | Participating Organization Group | Own contacts, package/recognition permissions, and report boundary; sponsorship is not investment. |
| **Civic Partner Organization** | G | Participating Organization Group | Own representative, agreement, territory, and data-sharing boundary; no partnership claim without writing. |
| **Engineering & Agent Builder Group** | G | Technology/participating Group | Needs distinct software-release and technical-record access. |
| **Campaign Cell** | G-D | Starts in Promotion | Campaign/audience/territory/window/budget scope. Graduates only with charter, Primary Admin, two accountable designations, account mapping, retention plan, and recurring mandate. Founder must decide whether Season 1 may graduate. |
| **Crew** | G-D | Starts in Contractor Organization | Contractor/work territory, job/task, Season scope. Graduates only with Captain, roster, rules, operating agreement, and approved project/account boundary. |
| **Territory Council** | G-D | Starts in Territory Stewardship | One territory, term, Season, public mandate. Graduates only with approved charter, representative rule, appeal/data steward, and no funds-custody ambiguity. Founder decision required. |

### 2.2 Role designations

| Role / condition | Class | Group | Time/territory and reason |
|---|---|---|---|
| **Licensed Contractor** | D | Contractor Organization | Credential expiry, service territory, work type, Season; a status within the company, never PBC licensure certification. |
| **Independent Sales Representative** | D | Recruiting or Contractor Organization | Agreement/campaign/territory/Season/consent scope; functional commercial role only. |
| **Crew Member** | D | Contractor Organization or Crew | Assignment, job/task, territory, Season; delivery role. |
| **Company Admin** | D | Participating Organization | Entity-limited appointment, renewable; delegated administration, not ownership. |
| **Captain** | G-D | Contractor Organization or Crew | Crew/work territory/project/term/Season; may sponsor, never unilaterally create, a Crew Group after Crew gates are met. |
| **ClaimBuddy** | D | Attestation & Verification | Object/territory/window/conflict/Season; independent process verifier, not insurer, adjuster, or legal actor. |
| **Sponsor** | D | Sponsor Organization | Package, report/recognition permission, campaign/Season; named contact, not the Group. |
| **Civic Partner** | D | Civic Partner Organization | Agreement, program/territory, dates, data limits; authorized representative, not public authority. |
| **Territory Steward** | D | Territory Stewardship | Seat/Territory/term/Season/conflict scope; renewable steward, not territorial owner. |
| **Recruiter** | D | Recruiting & Roster Operations | Source/campaign/cohort/Territory/consent/Season; no perpetual dossier or territory right. |
| **Campaign Producer** | D | Promotion & Campaign Production | Campaign/audience/Territory/budget envelope/window/Season; no budget-release authority. |
| **Verifier** | D | Attestation & Verification | Evidence/method/object/Territory/term/independence scope; ClaimBuddy is its named-method variant. |
| **Administrator** | D | PBC platform function | Environment/short appointment, reviewed each Season; no inherent territorial right. |
| **Company Agent** | D, non-human | Named Organization/Company Group | API/object/Territory/time/rate limit plus human sponsor; never member, officer, fiduciary, or verifier. |
| **Applicant** | D | Recruiting & Roster Operations | Application/consent/territory/retention scope; ends on outcome or withdrawal. |
| **Public Visitor** | neither | PBC public surface | Session/rate limit only. Visitor is an access state, not stakeholder entity or Role Assignment. |

**Founder decisions required:** activation of a Season 1 Territory Council; Campaign Cell/Crew graduation gates and size; contracting Entity; and verifier credential standard.

## 3. Role and permission matrix

### 3.1 Reading the matrix

`Allow` is scoped and audited; `Deny` implies no permission. `C#` means **Conditional** under the stated server-enforced condition; UI display is never authority.

| Code | Server-enforced condition for every C# cell |
|---|---|
| **C1** | Actor owns the record or is assigned to its Organization, Territory, and active Season; consent and source restrictions permit the action. |
| **C2** | Actor is named owner/manager for the parent object and does not change restricted data, price, funding terms, or another Group’s authority. |
| **C3** | Actor accepts only an Offer addressed to their represented Organization after terms/disclosures are acknowledged; no automatic money movement occurs. |
| **C4** | Actor creates the child object only under an approved parent and within active Territory/Season; required agreement exists. |
| **C5** | Actor is assigned as Task assignee; acceptance/completion requires required evidence and no blocked dependency. |
| **C6** | Actor uploads only evidence they originated or are authorized to submit; data classification and consent screening pass. |
| **C7** | Actor is an independent qualified Verifier/ClaimBuddy, passes conflict screen, and is not task performer, creator, Company Admin, or financial approver for the same object. |
| **C8** | Actor may issue a process attestation only after C7 verification and template/method controls; never an attestation of licensure, insurance, legal compliance, or payment. |
| **C9** | Actor acts within a current Seat/Territory; allocation/reassignment needs two human approvals, no conflict, notice, and appeal record. |
| **C10** | Actor administers members only for its own Group; identity/role/territory changes require consent/verification evidence and, when consequential, dual approval. |
| **C11** | Access is limited to a documented legitimate purpose, data class, Organization/Territory/Season scope, and audit trail; restricted exports always need dual approval. |
| **C12** | Action uses an approved campaign/package, audience consent, Territory and publication window; content has required review. |
| **C13** | Report is limited to that sponsor’s contracted package and privacy-safe aggregates; no participant dossier, restricted evidence, or other sponsor data. |
| **C14** | Privileged platform action is performed by two human Administrators, with change ticket, break-glass reason where applicable, audit event, and post-action review. |
| **C15** | Company Agent creates a draft or queue item only under a named human sponsor and configured scope; a human sends, accepts, publishes, approves, or changes authority. |

### 3.2 Matrix

Roles: **LC** Licensed Contractor; **ISR** Independent Sales Representative; **CM** Crew Member; **CA** Company Admin; **CAP** Captain; **CB** ClaimBuddy; **SP** Sponsor; **CP** Civic Partner; **TS** Territory Steward; **REC** Recruiter; **PROD** Campaign Producer; **VER** Verifier; **ADM** Administrator; **AGT** Company Agent; **APP** Applicant/Visitor.

| Permission (one row per permission) | LC | ISR | CM | CA | CAP | CB | SP | CP | TS | REC | PROD | VER | ADM | AGT | APP |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Create a Lead | C1 | C1 | Deny | C1 | C1 | Deny | C1 | C1 | C1 | Allow | C1 | Deny | C1 | C15 | C1 |
| Edit a Lead | C1 | C1 | Deny | C1 | C1 | Deny | Deny | C1 | C1 | Allow | C1 | Deny | C1 | C15 | C1 |
| Convert Lead to Offer | Deny | C2 | Deny | C2 | C2 | Deny | Deny | Deny | Deny | C2 | Deny | Deny | C2 | C15 | Deny |
| Accept an Offer | C3 | C3 | Deny | C3 | C3 | Deny | C3 | C3 | Deny | Deny | Deny | Deny | C3 | Deny | Deny |
| Create a Project | C4 | C4 | Deny | C4 | C4 | Deny | Deny | C4 | C4 | C4 | C4 | Deny | C4 | C15 | Deny |
| Create a Job | C4 | Deny | Deny | C4 | C4 | Deny | Deny | Deny | C4 | Deny | C4 | Deny | C4 | C15 | Deny |
| Create a Job Order | C4 | Deny | Deny | C4 | C4 | Deny | Deny | Deny | C4 | Deny | C4 | Deny | C4 | C15 | Deny |
| Create a Task Request | C4 | C4 | Deny | C4 | C4 | Deny | Deny | Deny | C4 | C4 | C4 | Deny | C4 | C15 | Deny |
| Create a Task | C4 | C4 | Deny | C4 | C4 | Deny | Deny | Deny | C4 | C4 | C4 | Deny | C4 | C15 | Deny |
| Accept a Task | C5 | C5 | C5 | C5 | C5 | C5 | Deny | Deny | C5 | C5 | C5 | C5 | C5 | Deny | Deny |
| Complete a Task | C5 | C5 | C5 | C5 | C5 | Deny | Deny | Deny | C5 | C5 | C5 | Deny | C5 | Deny | Deny |
| Upload evidence | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C6 | C15 | C6 |
| Verify completion | Deny | Deny | Deny | Deny | Deny | C7 | Deny | Deny | Deny | Deny | Deny | C7 | C7 | Deny | Deny |
| Issue an attestation | Deny | Deny | Deny | Deny | Deny | C8 | Deny | Deny | Deny | Deny | Deny | C8 | C8 | Deny | Deny |
| Allocate/reassign Territory Seat | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | C9 | Deny | Deny | Deny | C9 | Deny | Deny |
| Onboard a member | Deny | Deny | Deny | C10 | C10 | Deny | Deny | C10 | C10 | C10 | Deny | Deny | C10 | C15 | C1 |
| View another entity’s data | C11 | C11 | C11 | C11 | C11 | C11 | C13 | C11 | C11 | C11 | C11 | C11 | C11 | C15 | Deny |
| Export data | Deny | Deny | Deny | C11 | Deny | Deny | C13 | C11 | C11 | Deny | Deny | Deny | C11 | Deny | Deny |
| Configure a company | Deny | Deny | Deny | C10 | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | C14 | Deny | Deny |
| Manage roles | Deny | Deny | Deny | C10 | Deny | Deny | Deny | Deny | C9 | Deny | Deny | Deny | C14 | Deny | Deny |
| View ledger-candidate queue | C11 | Deny | Deny | C11 | C11 | C11 | C13 | C11 | C11 | Deny | C11 | C11 | Allow | C15 | Deny |
| Approve a ledger candidate | Deny | Deny | Deny | Deny | Deny | C7 | Deny | Deny | C9 | Deny | Deny | C7 | C14 | Deny | Deny |
| Post a campaign | Deny | Deny | Deny | C12 | Deny | Deny | Deny | C12 | C12 | C12 | C12 | Deny | C12 | Deny | Deny |
| Send member communication | C12 | C12 | Deny | C12 | C12 | Deny | C12 | C12 | C12 | C12 | C12 | Deny | C12 | C15 | Deny |
| View sponsor report | Deny | Deny | Deny | C13 | Deny | Deny | C13 | C13 | C13 | Deny | C13 | Deny | C13 | C15 | Deny |
| Administer platform | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | Deny | C14 | Deny | Deny |

## 4. Authorization model

### 4.1 Scope expression and evaluation

Every server-side authorization decision evaluates this tuple:

```text
(subject Person or service principal,
 legal Entity, active Group, Designation/permission,
 object type + object state, Territory set, Season + time window,
 purpose/data class, agreement/SLA, conflict status, assurance evidence)
```

A Role Assignment therefore contains at minimum: immutable assignment ID; subject; Group; Designation; permission set; Entity/Organization context; Territory IDs and ancestry behavior; Season ID; effective-from and effective-to timestamps; creator/approver; required training or credential evidence; conflict status; revocation reason; and audit correlation ID. An assignment with a missing, expired, suspended, or mismatched field evaluates to **Deny**.

**FR-AUTH-01 (P0).** The API shall enforce authorization on every read of non-public data and every mutation, using the tuple above and object-level state checks. Client-side guards are usability aids only. **Acceptance:** an integration test calling the API directly with a stale or wrong-territory Role Assignment receives a denial and an Audit Event.

**NFR-AUTH-01 (P0).** Privileged mutations shall be deny-by-default, server-authorized, correlation-identified, and immutably audited with actor, effective authority, target, old/new values where lawful, result, and reason.

The system must distinguish a **Group’s permanent structural right** (for example, Attestation & Verification can manage its own process) from a **Designation’s temporary operational right** (for example, a Verifier can review one task in one Territory during a term). The narrower object, territory, and time rule wins. No inherited Group membership grants a person a Designation’s approval power.

### 4.2 API expectations

- The API accepts an authenticated subject identity and resolves, not trusts, claimed role/territory/season headers.
- Each protected request carries a server-generated `correlation_id`; external integrations may supply an idempotency key but cannot choose audit identity.
- Mutation endpoints require an expected object version to prevent silent overwrites and return an explicit policy-denial code, not a misleading “not found.”
- Reads apply row- and field-level filtering. A sponsor may receive an aggregate report but not raw Applicant, Evidence, Consent, Conflict Disclosure, or another sponsor’s data.
- Permission and policy changes are versioned. A cache must not extend a revoked assignment; revocation is checked on the server at mutation time.
- Bulk export is a separate action with a data-class manifest, approvers, expiration, watermark, and Audit Event. It is not implemented as a broad list endpoint.

### 4.3 Company Agent authority boundary

The **Company Agent** is a non-human service principal with no independent legal, financial, governance, or attestation authority. Its human sponsor remains accountable for its outputs.

| Agent action | Rule |
|---|---|
| May do automatically | Classify an inbound message; deduplicate a Lead; draft a task, campaign copy, communication, report narrative, or evidence checklist; flag missing fields; route work; create a low-risk queue item; summarize records within granted scope. All outputs are labelled machine-prepared and audited. |
| May prepare for human approval | A Lead-to-Offer draft; Territory Seat recommendation; member onboarding packet; campaign publication package; verification checklist; ledger-candidate draft; sponsor-report draft; role-change request; dispute chronology. The Agent cannot advance the authoritative state. |
| May never do | Accept or alter a binding agreement; authorize, approve, post externally, or reverse a ledger candidate; move or instruct movement of money; grant/revoke roles or Territory Seats; verify completion; issue an attestation; make a licensure/insurance/legal-compliance conclusion; override consent, retention, conflict, or access controls; export restricted data; send an unsupervised mass communication; act as the sole approver; impersonate a Person. |

This adapts least privilege and separates signal from binding authority. [SRC — research/00-dao-platform-landscape.md] Agent access is capability-scoped, short-lived, revocable, and sampled for human review.

## 5. Territory and time scoping

1. **Territory ancestor rule.** A County assignment can authorize only County descendants explicitly permitted by policy; it does not automatically authorize a State or peer County. ZIP and Carrier Route allocations override a broader assignment where their rule is stricter. An overlay (for example, school district) is a separate Territory relation and must be named in the assignment.
2. **Season rule.** Operational Designations and Seats expire at the earlier of their `effective_to`, suspension/revocation, or Season Reset. Cool-Down permits evidence, reconciliation, and dispute actions only; it does not permit new work, new Offers, or new Territory claims without an exception approval.
3. **Reset rule.** At Reset, every address returns to **Need** for the new Season. The system archives prior assignments and evidence, removes active mutation permissions, and creates no carry-forward territorial entitlement. A next-Season allocation is a new decision referencing—not inheriting—the historical record.
4. **Overlap resolution.** Evaluate in this order: explicit deny/suspension; object-state safety control; narrower Territory; narrower active time window; Designation-specific condition; Group standing authority; platform default. The most restrictive applicable rule wins. A Territory Steward’s temporary Seat cannot expand a Company Admin’s entity right, and a Company Admin cannot defeat the steward’s allocation rule.
5. **Conflict resolution.** Concurrent claims to a Seat create `allocation-disputed` state. Neither claimant may reassign the Seat or approve a related ledger candidate. Territory Stewardship assigns an independent reviewer and records notice, evidence, decision, appeal window, and close.

## 6. Separation of duties and recusals

**FR-AUTH-02 (P0).** A completion is not independently verified if the same Person, Organization, controlled Entity, or Company Agent sponsor both performed/materially directed the work and verifies it. The verification engine must screen direct and declared conflicts; unresolved matches block verification.

**FR-AUTH-03 (P0).** Anything that may affect money, sponsor package performance, ledger posting, restricted member data, bulk export, or a Territory Seat requires two distinct human approvers with compatible scopes. One must be independent of the initiating Group where feasible. The platform records both decisions and prohibits self-approval.

**FR-AUTH-04 (P0).** A Person cannot approve their own application, Offer, evidence, attestation, role assignment, Territory allocation, data export, or ledger candidate. Changing the display actor, using a Company Agent, or acting through a controlled Organization does not cure a conflict.

**Founder recusal rule.** When a decision concerns Market Applications LLC, USA LLC, RRCA, a future foundation, founder-owned domains/brands/IP, or a contract between any of them and the proposed PBC, the founder must disclose the relationship. The decision is routed to a disinterested reviewer/approver under the future entity’s adopted governance process; if none exists, it is marked **recusal-blocked** and cannot be represented as independently approved. RRCA remains independently owned and is not a mechanism to bypass this rule. [SRC — ENGAGEMENT-BRIEF.md]

## 7. Abuse and misuse cases

| ID | Attack / misuse | Affected role(s) | Preventive and detective control | Residual risk |
|---|---|---|---|---|
| RISK-031 | A Company Admin changes an Applicant’s territory to capture a coveted Seat. | CA, TS | C9 dual approval; allocation notice; source evidence; immutable before/after Audit Event; appeal queue. | Colluding approvers may still favor a party; periodic independent allocation sampling is required. |
| RISK-032 | A Captain marks their own crew’s Task complete and asks a friendly verifier to rubber-stamp it. | CAP, CB, VER | C7 conflict graph; no self/organization approval; random secondary review for high-risk Tasks; dispute route. | Undisclosed relationships can evade automated conflict matching. |
| RISK-033 | An Agent is prompted to “approve the ledger” or bulk-export member data. | AGT, ADM | Agent never-authorize rule; capability endpoint allowlist; DLP/classification checks; no Agent export token; prompt/output logging. | A human could copy an Agent draft into an approval without adequate review. |
| RISK-034 | A privileged integration or broad administrator permission executes an unexpected configuration change. | ADM, external integration | Function-scoped permissions, dual control, change ticket, short-lived credentials, break-glass logging and review. This adapts Aragon’s least-privilege lesson. [SRC — research/01-01-aragon.md] | A legitimate pair of administrators can still make a harmful authorized change; recovery drills matter. |
| RISK-035 | A campaign producer sends non-consented or misleading mass recruitment messages. | PROD, REC, AGT | Consent gate, approved audience segment, content review, rate limits, unsubscribe enforcement, communication audit. | Consent data may be stale or an approved message can still be poorly received. |
| RISK-036 | A sponsor uses a report to infer Applicant identity or a competitor’s activity. | SP, CA | C13 aggregate thresholds, cohort suppression, contractual purpose limitation, export controls, watermarking, access logs. | Small-territory aggregates may remain re-identifiable without conservative thresholds. |
| RISK-037 | A malicious or compromised signer uses arbitrary multicall-like authority to drain or redirect a pool. | ADM, finance integration | No unrestricted multicall; allowlisted action types; external accounting reconciliation; dual approval; no platform money movement. DAOhaus documents the danger of broad Shaman/multicall powers. [SRC — research/02-02-daohaus.md] | A downstream custodian or bank may have different controls; platform controls do not eliminate that risk. |
| RISK-038 | Delegates accumulate multiple territories and suppress minority input. | TS, CP, CA | Territory/term cap, disclosure, public mandate record, recall/appeal, no token-weight default. Address delegation concentration is a known design risk. [SRC — research/05-05-snapshot-tally.md] | Influence may concentrate socially even where system caps work. |
| RISK-039 | A Recruiter retains rejected Applicant dossiers for future unrelated outreach. | REC, CA | Purpose/consent checks; Applicant retention timer; access revocation on outcome; deletion workflow and audit. | Lawful retention exceptions and backups create residual data exposure. |
| RISK-040 | A dormant external governance dependency becomes an unpatchable authority or records failure. | ADM, Engineering Group | No core dependency on DAOstack/DAOhaus/Baal; export/migration test; independently controlled system of record. DAOstack is dormant and DAOhaus core activity is uneven. [SRC — research/04-04-daostack.md] [SRC — research/02-02-daohaus.md] | Any vendor or open-source dependency can fail; tested exits reduce but do not remove risk. |

## 8. Open Questions and evidence boundary

### Open Questions

1. Who is the independent second approver for Season 1 Territory Seats, ledger candidates, and restricted exports while the founder is sole decision authority?
2. What credential source, refresh interval, and human escalation process will support “Licensed Contractor” status without representing the PBC as a licensure certifier?
3. Which data attributes constitute an Organization-control relationship for automated conflict screening, and who may resolve a false positive?
4. What geographic hierarchy and overlay precedence will be legally and operationally adopted for the first pilot Territory?
5. Which actions, if any, qualify as low-risk enough for a Company Agent to send without a human click, and how will this be acceptance-tested?
6. Will Sponsor and Civic Partner Organizations receive Company Admins, or only named Designations with a narrower report/communication scope?
7. What governance charter and representation test would justify creating a Territory Council rather than keeping local work inside Territory Stewardship?

### Evidence boundary at close

- **Founder intention / internal context:** proposed Kimosabe Commons, PBC; the four programs; the People-and-Addresses model; the Season clock; and current Entity reality come from the engagement brief and remain subject to founder decision. [SRC — ENGAGEMENT-BRIEF.md]
- **Model output / proposed control design:** the classifications, conditions, permission matrix, Agent boundary, recusal process, and Reset rules are design proposals for implementation and validation, not executed governance policy.
- **Verified research fact:** the comparative lessons about least privilege, scoped work/independent evaluation, arbitrary execution risk, delegation concentration, and maintenance risk are supported by the cited research reports. [SRC — research/00-dao-platform-landscape.md] [SRC — research/01-01-aragon.md] [SRC — research/02-02-daohaus.md] [SRC — research/03-03-colony.md] [SRC — research/05-05-snapshot-tally.md]

Nothing in this document is legal, accounting, insurance, securities, or professional licensing advice.
