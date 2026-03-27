# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises. Each persona includes Role Summary, Responsibilities, Goals, Typical Communication, and Interactions with existing roles. Example participation for common workflows is included.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain unit/integration tests and technical documentation
- Participate in design and code reviews; remediate review feedback
- Assist in sizing and estimating work; identify technical debt
- Instrument code for observability and monitoring
- Help identify technical risks and propose mitigations
- Support production troubleshooting and root cause analysis

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain test coverage and observability

### Typical Communication
- Daily standups, sprint planning, PR comments, design docs

### Interactions
- With PdM: clarify acceptance criteria and feature trade-offs
- With PM: surface scheduling impacts and capacity constraints
- With QA: provide testable builds and reproduce/verify defects
- With Release Manager: provide release-time validations and rollback plans

### Example participation
- Initiation: provide technical feasibility input
- Planning: estimate stories and flag dependencies
- Execution: deliver code, tests, and PRs
- Release: validate deployment steps and migrate data if needed
- Retrospective: share technical improvements and lessons learned

---

## Product Manager (PdM)

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own product vision, prioritize backlog, and measure outcomes.

### Responsibilities
- Define problem statements, success metrics, and acceptance criteria
- Prioritize roadmap and backlog with stakeholder alignment
- Validate solutions via research and metrics
- Make scope trade-offs and value decisions
- Accept or reject completed work against success criteria

### Goals
- Maximize customer value and measurable outcomes
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM, stakeholders, and engineering leads

### Interactions
- With BA: refine requirements into actionable stories
- With UX: align on user journeys and acceptance criteria
- With PM: coordinate scope and timeline decisions
- With Data Analyst: define metrics and instrumentation needs

---

## Project Manager (PM)

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications to enable teams to deliver commitments.

### Responsibilities
- Create and maintain project plans, timelines, and risk registers
- Manage dependencies and resource constraints
- Facilitate kickoff, planning, standups, and retrospectives
- Maintain status reporting and stakeholder communications
- Track action items and follow-ups from retrospectives and incidents

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations

### Typical Communication
- Weekly status updates, risk reports, decision logs

### Interactions
- With PdM: agree on priorities and timeline changes
- With Developers/QA: track progress and remove blockers
- With Release Manager: align release windows and readiness

---

## QA / Testing

### Role Summary
QA validates that software meets quality standards and acceptance criteria before release.

### Responsibilities
- Define and execute manual and automated test plans
- Validate acceptance criteria and regression risks
- Report, triage, and verify defect fixes
- Maintain test environments and test data
- Provide release test-signoff and verification evidence

### Goals
- Prevent regressions and ensure acceptance criteria are met
- Reduce production defects through automation

### Typical Communication
- Test reports in PRs, release checklists, defect triage sessions

### Interactions
- With Developers: clarify defects and acceptance gaps
- With Release Manager: confirm smoke and post-deploy checks

---

## UX Designer

### Role Summary
UX Designers translate product requirements into user journeys, wireframes, and UI specifications, ensuring usability and accessibility.

### Responsibilities
- Produce user journeys, wireframes, prototypes, and UI specs
- Advocate for user-centric design and accessibility best practices
- Conduct usability testing and synthesize feedback into actionable changes
- Create interaction patterns and visual assets for implementation
- Annotate acceptance criteria for UX flows and edge cases
- Maintain design system references and component documentation

### Goals
- Deliver intuitive, accessible user experiences and reduce rework
- Ensure design consistency and measurable usability improvements

### Typical Communication
- Design reviews, annotated deliverables, participation in planning and demos

### Interactions
- With PdM: refine product intent into user journeys and success metrics
- With Developers: provide assets, clarify interactions, and verify implementation
- With QA: ensure test cases include UX flows and accessibility checks

### Escalation / Decision
- If a design change materially impacts scope, escalate to PdM and PM for reprioritization.

### Example participation
- Initiation: produce initial wireframes and success criteria
- Planning: estimate design effort and handoff timing
- Execution: support implementation and review visuals in PRs
- Release: validate final UI and accessibility checks

---

## Business Analyst (BA)

### Role Summary
Business Analysts gather, document, and refine business requirements and processes to translate stakeholder needs into actionable technical specifications.

### Responsibilities
- Elicit and document detailed business requirements and acceptance criteria
- Model and map business processes and impacts of proposed changes
- Create user stories, process flows, and functional specifications
- Facilitate clarification workshops between stakeholders and engineering
- Maintain requirement traceability and change logs
- Produce test scenarios used by QA based on business rules

### Goals
- Reduce ambiguity in requirements; improve predictability of delivery
- Ensure stakeholder needs are testable and prioritized

### Typical Communication
- Requirement docs, workshops, annotated examples and change logs

### Interactions
- With PdM: translate strategic goals into detailed scope and acceptance criteria
- With Developers: clarify functional expectations and edge cases
- With QA: provide acceptance-test scenarios and traceability
- With PM: highlight timeline sensitivity and impacted milestones

### Escalation / Decision
- Unresolved requirement conflicts are elevated to PdM for final prioritization.

### Example participation
- Planning: run impact assessments and produce detailed specs
- Execution: respond to developer clarifications and acceptance test queries

---

## Release Manager

### Role Summary
Release Manager plans, coordinates, and owns release cycles to ensure safe, predictable deployments.

### Responsibilities
- Define release windows and coordinate pipeline gating and sign-offs
- Maintain and enforce pre-release checklist and approvals
- Coordinate cross-team release readiness (Dev, QA, Security, Support)
- Document rollback and mitigation plans and ensure they are tested
- Prepare release notes and stakeholder communications
- Run post-release verifications and retrospectives focused on release reliability

### Goals
- Reduce release-related incidents and rollbacks
- Improve visibility and predictability of deployments

### Typical Communication
- Release status in project channels, coordination with CI/CD/Ops contacts

### Interactions
- With PM: agree on schedule, scope, and go/no-go criteria
- With Developers/QA: confirm merged PRs, passing CI, and smoke tests
- With Support: ensure runbooks and communications are ready
- With Security Liaison: ensure security signoff is included in approvals

### Escalation / Decision
- Go/no-go decision is taken by Release Manager in consultation with PdM and PM

### Example participation
- Pre-release: run checklist and coordinate stakeholder signoffs
- Deployment: execute pipeline and monitor post-deploy metrics
- Post-release: lead release retrospective and capture follow-ups

---

## Support / Customer Success

### Role Summary
Support/Customer Success represents customers, handles incidents, and communicates product impact back to the team.

### Responsibilities
- Triage and document customer issues and incidents; provide reproducible steps
- Provide runbooks and first-line troubleshooting guidance
- Communicate severity and customer impact to the team
- Feed prioritized customer issues and trends to PdM/PM
- Update knowledgebase and user-facing documentation
- Coordinate customer-facing communications for incidents and releases

### Goals
- Minimize customer impact and time-to-resolution
- Surface actionable feedback for product and process improvements

### Typical Communication
- Incident channels, ticketing systems, and status updates

### Interactions
- With Devs: reproduce issues, provide logs and user context
- With PdM/PM: prioritize customer-impacting fixes and inform stakeholder communications
- With Release Manager: coordinate hotfix/patch release timing and messages

### Escalation / Decision
- Critical incidents are escalated per the incident playbook; PM notifies Sponsor as needed

---

## Security Liaison

### Role Summary
Security Liaison ensures security considerations are applied early and that security reviews and scans are completed and triaged.

### Responsibilities
- Coordinate security reviews, threat modeling, and required scans (SAST/SCA)
- Ensure findings are triaged and tracked to resolution
- Advise on secure design patterns and remediation options
- Validate required security signoffs before release
- Maintain contact with on-call security teams and incident playbook

### Goals
- Reduce security-related incidents and integrate security into delivery flow

### Typical Communication
- Security findings in issue trackers/PRs; signoffs in release checklists

### Interactions
- With Developers: review remediation plans and validate fixes
- With QA: confirm security tests and scans are executed
- With Release Manager: ensure security gating is part of go/no-go criteria

### Escalation / Decision
- Critical vulnerabilities may halt release and require immediate remediation

---

## Data Analyst

### Role Summary
Data Analysts define measurement plans, produce reports, and analyze results to validate success metrics and guide prioritization.

### Responsibilities
- Define instrumentation and metrics for features and experiments
- Produce dashboards, experiment analysis, and post-release reports
- Validate feature performance against success criteria
- Support acceptance criteria that require measurable signals
- Assist in post-release monitoring and anomaly detection

### Goals
- Make product decisions data-informed and detect regressions early

### Typical Communication
- Dashboards and summarized analysis for PdM, PM, and stakeholders

### Interactions
- With PdM: translate goals into measurable metrics and targets
- With Developers: specify instrumentation and tracking needs
- With PM/Release Manager: provide post-release metrics for go/no-go

### Escalation / Decision
- Significant metric regressions trigger immediate triage with PdM/PM

---

## How these personas are used in exercises and playbooks
- Use these persona definitions to frame scenarios, role-based responsibilities, and checklists for exercises.
- Each persona entry can be used as a prompt for Copilot Spaces to elicit role-specific guidance or runbook text.

