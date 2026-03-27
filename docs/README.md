# OctoAcme Project Management Process Docs

This repository centralizes OctoAcme project management process documentation for use with Copilot Spaces and team onboarding. Program process documents and living process docs are stored in the docs/ folder; issue templates for requesting updates to process docs are kept under .github/ISSUE_TEMPLATE/.

OctoAcme's project management approach is built around a lightweight, iterative lifecycle that moves work from initiation through planning, execution, release, and retrospective. Projects begin with a focused initiation phase (one-pager, stakeholder alignment, high-level timeline) and only proceed to planning when success metrics, priorities, and team availability are confirmed. Planning breaks approved initiatives into prioritized backlog items with acceptance criteria, estimates, and a Definition of Done; dependencies and risks are captured in a simple risk register. Execution uses a project board workflow (Backlog → Ready → In Progress → In Review → QA → Done) to keep work visible and flowing, and teams are encouraged to deliver small, testable increments.

Roles and responsibilities are clearly defined to ensure ownership and effective collaboration. Product Managers own problem definition, prioritization, and success metrics; Project Managers coordinate schedules, risks, and communications; Developers implement features, tests, and reviews; QA validates acceptance criteria and test coverage; and stakeholders provide inputs and approvals. These personas help align expectations for planning, estimation, and handoffs so each artifact (one-pager, backlog, release plan, risk register) has a clear owner and purpose.

Communication is structured and frequent: short daily standups (15 minutes) for progress and blockers, weekly delivery syncs to surface progress and flagged risks, demos at the end of sprints or milestones, and monthly stakeholder updates. There are explicit templates and cadence for status reporting and incident communications, and a defined escalation path (team → PM → Product Lead → Sponsor) for blockers, with a separate flow to notify Security on-call for security incidents. Retrospectives after sprints, releases, or incidents turn learnings into prioritized action items tracked back in the backlog.

Quality assurance and release practices emphasize automation, small PRs, and verification before deployment. The PR workflow favors limited-size changes, requires linking issues and acceptance criteria, automated tests and linting in CI, and at least one approval before merging. Testing includes unit, integration, and end-to-end smoke tests for critical flows, plus manual QA when needed and security scanning in CI. Releases follow a checklist (pre-release checks, smoke tests in staging, automated deployment preferred, post-deploy verification, and rollback/incident playbooks) and retrospectives capture continuous improvement items to reduce repeat issues.

Main process documents in this folder:
- octoacme-project-management-overview.md
- octoacme-project-initiation.md
- octoacme-project-planning.md
- octoacme-execution-and-tracking.md
- octoacme-risks-and-communication.md
- octoacme-release-and-deployment.md
- octoacme-retrospective-and-continuous-improvement.md
- octoacme-roles-and-personas.md

Issue template for contributing updates:
- .github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml
