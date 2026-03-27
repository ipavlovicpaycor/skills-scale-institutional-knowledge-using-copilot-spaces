# OctoAcme Release Checklist

Use this checklist for every production release. The **Release Manager** owns completion of this checklist and should share it with the PM, QA, and Support teams before the deployment window opens. Copy the checklist into the release PR or issue to track sign-offs inline.

> **How to use:** Create a new issue or PR comment for each release. Paste this checklist and check items off as they are completed. Tag the responsible role next to any item that is blocked.

---

## Pre-Release

### Requirements & Acceptance

- [ ] All stories in the release are in **Done** status and acceptance criteria have been verified by QA.
- [ ] Business Analyst has confirmed that all documented requirements map to delivered features.
- [ ] Product Manager has given product sign-off on the release scope.
- [ ] Any descoped items are documented and communicated to Stakeholders.

### Code Quality & CI

- [ ] All CI pipeline checks (build, unit tests, integration tests) are **passing** on the release branch.
- [ ] Code coverage meets or exceeds the project threshold defined in the Definition of Done.
- [ ] No open P1/P2 defects remain unresolved for features in this release.
- [ ] Code freeze has been communicated to the team and enforced on the release branch.

### Security

- [ ] SAST (static analysis) scan has run and all **critical/high** findings are resolved or have an accepted risk note from the Security Liaison.
- [ ] Dependency vulnerability audit (e.g., `npm audit`, `pip-audit`, Dependabot) has been reviewed; no unresolved critical CVEs.
- [ ] DAST or penetration test has been completed for any new externally exposed endpoints (if applicable).
- [ ] Security Liaison has provided written sign-off for this release.
- [ ] Secrets scan confirms no credentials, tokens, or keys are present in the release branch.

### QA Sign-Off

- [ ] Regression test suite has passed in the staging environment.
- [ ] Smoke tests have passed against the release build.
- [ ] Exploratory testing completed for high-risk areas identified during the sprint.
- [ ] QA Lead has issued a formal go/no-go recommendation.

### Release Preparation

- [ ] Release notes drafted and reviewed by Product Manager and Support/Customer Success.
- [ ] Support runbook updated to reflect new or changed features in this release.
- [ ] Rollback plan documented: steps, responsible parties, and decision criteria are clearly defined.
- [ ] Database migration scripts (if any) have been tested in staging and reviewed by the DBA or lead developer.
- [ ] Feature flags reviewed: confirm which flags are on/off for this release.
- [ ] Deployment runbook reviewed and updated by the Release Manager.
- [ ] Stakeholder notification drafted and ready to send (contents, distribution list, timing confirmed).

### Go / No-Go Meeting

- [ ] Go/No-Go meeting held with PM, QA, Release Manager, and Security Liaison.
- [ ] All blocking items from the meeting are resolved or explicitly accepted with documented rationale.
- [ ] Final **GO** decision confirmed and recorded by the Release Manager.

---

## Deployment

- [ ] Deployment window communicated to all stakeholders and the Support team.
- [ ] On-call/incident-response engineer confirmed and available during the deployment window.
- [ ] Monitoring dashboards opened and baseline metrics noted before deployment begins.
- [ ] Deployment executed per the runbook (e.g., canary rollout, blue/green switch, or direct deploy).
- [ ] Database migrations run successfully (if applicable).
- [ ] Feature flags set to production values as specified in the release plan.
- [ ] Health checks and readiness probes confirm the new version is serving traffic.
- [ ] Initial smoke tests run against the production environment immediately post-deployment.

---

## Post-Release Verification

### Monitoring & Stability

- [ ] Error rates, latency, and key business metrics are within acceptable thresholds for at least 30 minutes post-deployment.
- [ ] No critical alerts or pages triggered in the first monitoring window.
- [ ] Data Analyst confirms analytics events and dashboards are recording correctly.
- [ ] Support/Customer Success confirms no abnormal spike in support tickets or customer complaints.

### Communication

- [ ] Stakeholder notification sent confirming successful deployment.
- [ ] Release notes published to the appropriate channel (e.g., changelog, release page, Slack announcement).
- [ ] Support team briefed on release contents, known issues, and escalation path.

### Rollback Readiness (until stable window closes)

- [ ] Rollback decision criteria reviewed; team remains on standby for agreed stability window.
- [ ] Rollback has **not** been triggered, OR rollback was executed and documented with root cause noted.

### Closure

- [ ] Release issue/PR closed and linked to the relevant milestone.
- [ ] Any post-release bugs or observations logged as follow-up issues with priority assigned.
- [ ] Retrospective meeting scheduled (see `octoacme-retrospective-and-continuous-improvement.md`).
- [ ] Release metrics captured (lead time, deployment frequency, change failure rate, MTTR if applicable).

---

## Quick Reference: Roles and Responsibilities

| Step | Primary Owner | Supporting Roles |
|---|---|---|
| Acceptance criteria verified | QA / BA | Product Manager |
| CI passing | Developer | Release Manager |
| Security scans | Security Liaison | Developer |
| Smoke tests | QA | Release Manager |
| Rollback plan | Release Manager | Developer, PM |
| Stakeholder notification | Release Manager / PM | Support/CS |
| Support runbook update | Support / CS | Release Manager |
| Retrospective scheduling | Project Manager | PM, Release Manager |
