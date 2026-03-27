# OctoAcme — Release Checklist

Purpose: Actionable pre-release, deployment, and post-release steps for Release Manager and PM.

## Pre-release (owner: Release Manager / PM)
- [ ] Acceptance criteria verified for all release items (link issues)
- [ ] All PRs merged and linked to issues (no outstanding merge conflicts)
- [ ] CI passed for all changes in release branch
- [ ] Automated and manual tests executed; test coverage validated
- [ ] Security scans (SAST/SCA) completed and critical findings addressed
- [ ] Migration and data changes reviewed and scheduled
- [ ] Release notes drafted and reviewed (summary, notable changes, migration steps)
- [ ] Rollback / mitigation plan documented and validated (if applicable)
- [ ] Stakeholder notification plan prepared (audience, channel, timing)
- [ ] Support runbook / troubleshooting guide updated and validated
- [ ] Post-release verification checklist prepared (smoke tests, metrics to monitor)
- [ ] Release owner(s) and on-call contacts confirmed

## Deployment (owner: Release Manager / DevOps)
- [ ] Deployment window confirmed and communicated
- [ ] Backup / snapshot created (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Confirm monitoring and dashboards are active for post-deploy
- [ ] Approve production deployment after staging verification
- [ ] Deploy to production using automated pipeline
- [ ] Run post-deploy smoke tests and sanity checks
- [ ] Monitor key metrics and error rates for agreed observation window

## Post-release (owner: Release Manager / PM / Support)
- [ ] Announce release to stakeholders and customers (with release notes)
- [ ] Verify support runbook reflects any new or changed behaviors
- [ ] Confirm no critical incidents; if present, follow incident playbook
- [ ] Add follow-up actions to backlog (bugs, usability issues, improvements)
- [ ] Schedule post-release verification or short retrospective
- [ ] Mark release as complete in project board and update documentation

## Quick go/no-go decision checklist
- [ ] Critical acceptance criteria met
- [ ] CI & security scans green or acceptable risk documented
- [ ] Rollback plan ready and tested
- [ ] Support and on-call notified and prepared

## Release Metadata (to include in release note)
- Release name/number:
- Date:
- Owners:
- Summary:
- Rollback plan:
- Known issues:

## Notes
- Use this checklist as a template for all release types (patch/minor/major). Adjust the checklist depth according to release risk and scope.
