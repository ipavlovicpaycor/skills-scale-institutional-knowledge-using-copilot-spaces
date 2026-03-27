# OctoAcme Role Interactions

This document provides a role interaction matrix and three detailed handoff scenarios to illustrate how OctoAcme team members collaborate across the project lifecycle. Use these scenarios to identify accountability gaps, set SLA expectations, and train new team members.

---

## Role Interaction Matrix

The table below shows the primary communication channel and collaboration pattern for each role pair. "→" indicates who typically initiates the interaction.

| From \ To | PM | PdM | Developer | QA | Release Mgr | UX Designer | BA | Support/CS | Security Liaison | Data Analyst | Stakeholder |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **PM** | — | Weekly sync | Sprint planning, blockers | Status / go-no-go | Release scheduling | Design milestone check-in | Requirement risk alerts | Pre-release briefing | Security gate review | Metric review | Status reports |
| **PdM** | Weekly sync | — | Acceptance criteria, roadmap | Story clarity | Release scope | Requirements + feedback | Backlog refinement | Customer feedback intake | Security requirements | Measurement plan | Roadmap updates |
| **Developer** | Blocker escalation | Clarification questions | — | PR hand-off, defect fixes | CI status | Design clarification | Acceptance criteria Q&A | Incident support | Security review response | Instrumentation delivery | — |
| **QA** | Go/no-go signal | Acceptance criteria | Defect reports | — | Release sign-off | UI spec validation | Requirements mapping | UAT support | Security finding context | Test data coordination | — |
| **Release Mgr** | Go/no-go decision | Scope alignment | Deployment coordination | Final QA gate | — | UI freeze confirmation | Requirement completeness | Runbook + release notes | Security sign-off receipt | Analytics readiness | Deployment announcement |
| **UX Designer** | Design milestone updates | Design review | Spec hand-off, UI review | Bug triage | UI freeze sign-off | — | User journey alignment | — | Accessibility review | Engagement data feedback | Design presentations |
| **BA** | Timeline risk alerts | Backlog refinement | Acceptance criteria | UAT scenarios | Scope confirmation | User journey input | — | Supportability review | Compliance requirements | Measurement validation | Requirements sign-off |
| **Support/CS** | Incident escalation | Customer feedback | Incident context | UAT participation | Release readiness | — | Ticket pattern sharing | — | Incident security context | CSAT/NPS sharing | — |
| **Security Liaison** | Security gate | Security requirements | PR review, CVE triage | Scan results sharing | Pre-release sign-off | Accessibility/security overlap | Compliance input | Incident response | — | Privacy review | Compliance reporting |
| **Data Analyst** | Impact reporting | Measurement plan | Instrumentation review | Data quality checks | Analytics readiness | Engagement metrics | Metric definition | Ticket trend analysis | Privacy compliance | — | Outcome reporting |
| **Stakeholder** | Approvals, priorities | Strategic direction | — | UAT approval | Release announcement receipt | Design approval | Requirements sign-off | Customer escalation | Compliance oversight | Outcome review | — |

---

## Scenario A: New Feature — PdM → UX → Dev → QA → Release

**Context:** A new feature request is approved and needs to go from concept to production.

### Handoff 1: PdM → UX Designer

| Attribute | Detail |
|---|---|
| **Trigger** | Feature approved in roadmap; PdM creates a feature brief |
| **Responsibility** | PdM provides problem statement, user goals, success metrics, and constraints. UX Designer acknowledges and schedules a discovery session. |
| **Communication Channel** | Linked design brief in the backlog tool + kick-off meeting invite |
| **Expected SLA** | UX Designer responds within **1 business day**; initial wireframes delivered within **5 business days** of kick-off |
| **Accountability note** | PdM signs off on wireframes before UX moves to high-fidelity specs. If wireframes require significant rework, PdM and UX agree on a revised timeline and notify the PM. |

### Handoff 2: UX Designer → Developer

| Attribute | Detail |
|---|---|
| **Trigger** | PdM has approved high-fidelity designs; stories are ready for sprint commitment |
| **Responsibility** | UX Designer links annotated design files to each story; runs a design walk-through with the development team. Developers raise implementation concerns within the walk-through session. |
| **Communication Channel** | Design file link in story + scheduled walk-through meeting (30–60 min) |
| **Expected SLA** | Walk-through scheduled within **2 business days** of designs being approved; Developer questions answered within **1 business day** |
| **Accountability note** | Any design trade-offs accepted by Developers must be noted in the story and approved by PdM before implementation begins. |

### Handoff 3: Developer → QA

| Attribute | Detail |
|---|---|
| **Trigger** | Developer marks the story as ready for QA (PR merged to integration branch) |
| **Responsibility** | Developer provides a PR description with test evidence, environment notes, and any known edge cases. QA validates against acceptance criteria and the design spec. |
| **Communication Channel** | PR comment / story status transition + Slack notification to QA channel |
| **Expected SLA** | QA begins testing within **1 business day** of handoff; test results within **3 business days** |
| **Accountability note** | Defects found by QA are logged immediately and assigned back to the Developer. P1/P2 defects block the release; P3/P4 are triaged by PM and QA jointly. |

### Handoff 4: QA → Release Manager

| Attribute | Detail |
|---|---|
| **Trigger** | QA completes all test cases; no open blocking defects |
| **Responsibility** | QA issues a formal sign-off note (test summary, pass rate, open non-blocking items). Release Manager adds the QA sign-off to the release checklist. |
| **Communication Channel** | Test summary comment on the release issue + email or Slack DM to Release Manager |
| **Expected SLA** | Sign-off provided within **1 business day** of final test run; Release Manager confirms receipt same day |
| **Accountability note** | If QA identifies a risk but chooses not to block the release, the PM must acknowledge and document the accepted risk in the release checklist. |

---

## Scenario B: Production Incident — Support/CS → Developer → PM → Stakeholders

**Context:** A production issue is reported by a customer and escalated internally.

### Handoff 1: Support/CS → Developer (Incident Triage)

| Attribute | Detail |
|---|---|
| **Trigger** | Support receives a customer report of unexpected behavior or outage |
| **Responsibility** | Support documents the issue (symptoms, affected users, business impact, steps to reproduce) and escalates to the Developer on-call or via the incident channel. Support remains available to provide additional customer context. |
| **Communication Channel** | Incident channel (e.g., `#incidents` in Slack) + incident ticket created |
| **Expected SLA** | On-call Developer acknowledges within **15 minutes** for P1; **1 hour** for P2 |
| **Accountability note** | Support owns customer communication during the incident. Developer owns technical investigation. If the Developer cannot reproduce within 30 minutes, they escalate to the technical lead. |

### Handoff 2: Developer → PM (Impact Assessment)

| Attribute | Detail |
|---|---|
| **Trigger** | Developer confirms the issue is real and has assessed scope/impact |
| **Responsibility** | Developer provides a technical summary (root cause hypothesis, affected components, estimated fix time). PM assesses business impact and decides on incident priority and whether to escalate to Stakeholders. |
| **Communication Channel** | Incident ticket update + direct message to PM |
| **Expected SLA** | PM notified within **30 minutes** of incident confirmation; PM responds with guidance within **15 minutes** |
| **Accountability note** | PM owns the decision to escalate to Stakeholders and approves any emergency changes (hotfix or rollback). Release Manager is looped in if a rollback is under consideration. |

### Handoff 3: PM → Stakeholders (Communication & Decision)

| Attribute | Detail |
|---|---|
| **Trigger** | Incident is P1 or has significant customer/revenue impact; PM decides Stakeholders need awareness |
| **Responsibility** | PM sends a concise status update: what is affected, what is being done, estimated resolution time. Stakeholders respond with business priority guidance if the fix requires trade-offs. |
| **Communication Channel** | Email or executive Slack channel; follow-up verbal call if the incident persists beyond **1 hour** |
| **Expected SLA** | Initial stakeholder notification within **1 hour** of P1 confirmation; updates every **30 minutes** until resolved |
| **Accountability note** | After resolution, PM and Developer lead a post-mortem within **3 business days**. Support contributes customer impact data. Findings and action items are tracked in the retrospective. |

---

## Scenario C: Requirement Change — Stakeholder → BA → PdM → PM → Developer

**Context:** A stakeholder requests a significant change to a feature already in planning or mid-sprint.

### Handoff 1: Stakeholder → BA (Change Request Intake)

| Attribute | Detail |
|---|---|
| **Trigger** | Stakeholder identifies a new need or constraint that changes the agreed scope |
| **Responsibility** | Stakeholder documents the request and business rationale. BA schedules a requirements session to clarify scope, impact, and urgency. BA produces a change impact assessment. |
| **Communication Channel** | Change request form or email → BA creates a formal change note in the backlog tool |
| **Expected SLA** | BA acknowledges within **1 business day**; change impact assessment delivered within **3 business days** |
| **Accountability note** | BA is responsible for ensuring the request is fully understood and documented before it reaches PdM. Incomplete change requests are returned to the Stakeholder for clarification. |

### Handoff 2: BA → PdM (Prioritization Decision)

| Attribute | Detail |
|---|---|
| **Trigger** | BA delivers the change impact assessment to the PdM |
| **Responsibility** | PdM reviews the assessment, compares it against current roadmap priorities, and decides whether to accept, defer, or reject the change. PdM documents the decision and rationale. |
| **Communication Channel** | Backlog tool comment + brief sync meeting with BA and Stakeholder if trade-offs are significant |
| **Expected SLA** | PdM decision within **2 business days** of receiving the impact assessment |
| **Accountability note** | If the change impacts current sprint commitments, PdM must align with PM before communicating the decision to the Stakeholder. |

### Handoff 3: PdM → PM (Scheduling & Impact Planning)

| Attribute | Detail |
|---|---|
| **Trigger** | PdM approves the change and hands it to PM for scheduling |
| **Responsibility** | PM assesses timeline impact, resource availability, and dependencies. PM communicates any schedule changes to Stakeholders and updates the project plan. |
| **Communication Channel** | Updated project plan shared via the project tracker + stakeholder update email |
| **Expected SLA** | PM provides schedule impact within **1 business day** of PdM approval |
| **Accountability note** | PM documents any scope removed or deferred to accommodate the change. This is recorded in the change log and shared with Stakeholders. |

### Handoff 4: PM → Developer (Implementation Briefing)

| Attribute | Detail |
|---|---|
| **Trigger** | Change is scheduled and stories are refined and ready for development |
| **Responsibility** | PM and BA brief the Developer team on the change. Stories are updated with revised acceptance criteria. Developers acknowledge readiness to take on the work in the agreed sprint. |
| **Communication Channel** | Sprint planning meeting + updated stories in the backlog tool |
| **Expected SLA** | Developers confirm capacity and acceptance within the sprint planning session |
| **Accountability note** | If the change introduces technical risk not surfaced during planning, Developers escalate to PM within **1 business day** of picking up the story. |
