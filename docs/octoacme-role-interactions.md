# OctoAcme — Role Interactions & Handoff Scenarios

This document describes common handoffs, communication channels, and expected SLAs for core role interactions.

## Interaction Matrix (summary)
- PdM ⇄ BA: requirements, acceptance criteria (channel: doc + workshop) — SLA: 3 business days for clarifications
- PdM ⇄ UX: product intent and design alignment (channel: design review) — SLA: 5 business days for initial mock for small features
- PdM ⇄ PM: scope and schedule alignment (channel: weekly sync) — SLA: immediate escalation in next sync
- PM ⇄ Dev: scheduling and capacity (channel: backlog, PRs) — SLA: clarify within one sprint planning session
- Dev ⇄ QA: validation and defect triage (channel: PR & test reports) — SLA: defects triaged within 2 business days
- Release Manager ⇄ Support: runbooks and release readiness (channel: release checklist) — SLA: runbook updated before release

## Example Scenario A — New feature delivery (PdM -> UX -> Dev -> QA -> Release)
1. PdM provides one-pager and success metrics to BA/PdM/PM (channel: project one-pager).
   - Responsibility: PdM owns scope and success definition.
   - SLA: One-pager and initial scope finalized within 5 business days.
2. UX produces wireframes and acceptance criteria (channel: design docs).
   - Responsibility: UX provides annotated mockups and accessibility notes.
   - SLA: Initial mock within agreed sprint or 5 business days for small features.
3. Developers implement feature per acceptance criteria (channel: PR).
   - Responsibility: Developers write tests and documentation.
   - SLA: Iteration within sprint cadence.
4. QA validates feature and runs smoke tests (channel: test reports/PR).
   - Responsibility: QA sign-off required for release.
   - SLA: QA validation within 2–3 business days of PR readiness.
5. Release Manager coordinates release and go/no-go (channel: release checklist).
   - Responsibility: Approve go/no-go with PdM and PM.
   - SLA: Final decision before scheduled deploy window.

## Example Scenario B — Production incident (Support -> Dev -> PM -> Stakeholders)
1. Support triages incident and escalates severity (channel: incident channel, ticket).
   - Responsibility: Support collects logs, customer impact, and reproduction steps.
   - SLA: Initial triage and severity classification within 1 hour for high-severity incidents.
2. Dev investigates and proposes mitigation (channel: incident channel / PR).
   - Responsibility: Dev provides hotfix or mitigation and estimated ETA.
   - SLA: Initial mitigation plan within 2 hours for Sev1.
3. PM coordinates stakeholder communications and escalation (channel: incident updates).
   - Responsibility: PM provides status updates and arranges Sponsor escalation if required.
   - SLA: Status update every 30–60 minutes for active Sev1 incidents.
4. After resolution: run a blameless retrospective and capture action items.

## Example Scenario C — Requirement change (Stakeholder -> BA -> PdM -> PM -> Dev)
1. Stakeholder requests change and provides business rationale (channel: meeting/email).
   - Responsibility: Stakeholder explains impact and desired outcome.
   - SLA: BA acknowledges within 2 business days.
2. BA analyzes impact and drafts updated requirements (channel: requirement doc).
   - Responsibility: BA produces impact analysis and notes affected milestones.
   - SLA: Impact analysis within 5 business days (or as agreed).
3. PdM reprioritizes and communicates to PM and Dev (channel: backlog update).
   - Responsibility: PdM makes final prioritization decision and updates acceptance criteria.
   - SLA: Prioritization decision within next planning session.
4. PM updates project plan and notifies stakeholders of timeline changes.

## Notes on handoffs
- Use a single source of truth (project README / one-pager) to document decisions and acceptance criteria.
- Handoffs must include explicit owner and acceptance criteria for each deliverable.
- For time-sensitive handoffs (incidents, releases), use synchronous channels and follow-up with tickets for tracking.
