# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## QA / Testing

### Role Summary
QA Engineers validate that features meet acceptance criteria, maintain quality standards, and prevent regressions before and after releases.

### Responsibilities
- Write and execute test plans, test cases, and automated test suites
- Validate acceptance criteria for each story or feature
- Identify, document, and track defects to resolution
- Participate in sprint planning to clarify testability of requirements
- Run regression, smoke, and exploratory testing before releases
- Collaborate with developers on test infrastructure and coverage
- Report quality metrics and trends to the Project Manager

### Goals
- Prevent defects from reaching production
- Shorten feedback loops between development and quality verification
- Maintain comprehensive test coverage aligned with risk

### Typical Communication
- Daily standups and sprint planning sessions
- Defect reports and test result summaries
- Pre-release sign-off notes shared with PM and Release Manager

### Interactions with Existing Roles
- Works with **Developers** on defect triage and test automation integration.
- Receives acceptance criteria from **Product Managers** and confirms when criteria are met.
- Provides go/no-go quality signal to the **Project Manager** and **Release Manager** before deployments.
- Escalation: if critical defects are found close to a release, QA escalates to PM and Release Manager to decide on delay or risk acceptance.

---

## Stakeholders

### Role Summary
Stakeholders are business owners, executives, or external partners who fund, sponsor, or are impacted by the project. They provide requirements, approvals, and strategic guidance.

### Responsibilities
- Define high-level business goals and success criteria
- Review and approve project charters, roadmaps, and key milestones
- Participate in steering meetings and change-control decisions
- Provide timely feedback on demos and deliverables
- Champion the project within the broader organization

### Goals
- Achieve business outcomes tied to the project investment
- Stay informed of progress, risks, and decisions without day-to-day involvement
- Ensure the project stays aligned with organizational strategy

### Typical Communication
- Monthly stakeholder updates from the Project Manager
- Milestone demo and review sessions
- Escalation briefings for major risks or scope changes

### Interactions with Existing Roles
- Provides strategic direction to **Product Managers** who translate it into backlog priorities.
- Receives status reports from **Project Managers** and raises concerns or approvals.
- Escalation: unresolved scope or priority conflicts are escalated from PM/PdM to Stakeholders for a decision.

---

## UX Designer

### Role Summary
UX Designers translate product requirements and user research into intuitive workflows, wireframes, and UI specifications that guide development and ensure accessible, user-centered experiences.

### Responsibilities
- Conduct user research, interviews, and usability testing to inform design decisions
- Create wireframes, prototypes, and high-fidelity UI specifications
- Define user journeys and information architecture
- Advocate for accessibility standards (WCAG) across all deliverables
- Participate in backlog refinement to ensure stories include design context
- Iterate on designs based on developer feasibility feedback and QA findings
- Maintain a shared design system and component library

### Goals
- Deliver intuitive experiences that reduce user friction and support adoption
- Shorten design-to-development handoff time by providing clear, annotated specs
- Ensure designs are validated with real users before full build begins

### Typical Communication
- Design reviews and critique sessions with Product Manager and Developers
- Annotated design files (e.g., Figma) linked in user stories
- Usability test reports shared with Product Manager and Stakeholders

### Interactions with Existing Roles
- Collaborates with **Product Managers** to align designs with success metrics and user needs; receives prioritized requirements and returns validated design specs.
- Works with **Developers** to clarify design intent during implementation; reviews built UI against specs before QA handoff.
- Shares usability findings with **Stakeholders** during milestone demos to drive informed decisions.
- Escalation: if technical constraints require significant design trade-offs, the UX Designer and Product Manager jointly present options to Stakeholders.

### Workflow Participation
- **Initiation:** Contributes user research insights and competitive analysis to the problem statement.
- **Planning:** Produces low-fidelity wireframes to size and scope stories with the team.
- **Execution:** Delivers detailed specs sprint by sprint; reviews implemented UI with QA.
- **Release:** Validates UI in staging; confirms accessibility checklist is complete.
- **Retrospective:** Reports usability findings from the release period; proposes design system improvements.

---

## Business Analyst

### Role Summary
Business Analysts gather, document, and refine business requirements, bridging the gap between stakeholders and the technical team. They ensure requirements are complete, unambiguous, and traceable before development begins.

### Responsibilities
- Elicit requirements through workshops, interviews, and document analysis
- Produce Business Requirements Documents (BRD), process maps, and use cases
- Analyze the business impact of proposed changes and identify risks
- Translate stakeholder needs into actionable acceptance criteria and user stories
- Maintain requirements traceability from business goal to implemented feature
- Facilitate sign-off of requirements with Product Manager and key Stakeholders
- Support UAT by confirming test scenarios align with documented requirements
- Identify process inefficiencies and propose improvements

### Goals
- Ensure requirements are stable and agreed upon before development starts, reducing rework
- Provide a clear audit trail from business need to delivered feature
- Reduce ambiguity that causes handoff delays between Product and Engineering

### Typical Communication
- Requirements workshops with Stakeholders and Product Managers
- Written requirement specifications and story acceptance criteria in the backlog tool
- UAT support sessions and sign-off emails with Stakeholders

### Interactions with Existing Roles
- Partners with **Product Managers** to convert business goals into prioritized, well-scoped backlog items; the PdM owns priority, the BA owns completeness of requirements detail.
- Works with **Project Managers** to flag requirement risks or gaps that could affect the timeline.
- Translates stakeholder needs into detailed acceptance criteria for **Developers** and ensures stories are ready for sprint commitment.
- Escalation: if conflicting requirements are discovered, the BA surfaces the conflict to PdM and Stakeholders for a decision before sprint work begins.

### Workflow Participation
- **Initiation:** Documents the problem statement and high-level scope; runs stakeholder interviews.
- **Planning:** Refines epics into stories with clear acceptance criteria; maps dependencies.
- **Execution:** Answers developer clarification questions; reviews in-progress work against requirements.
- **Release:** Supports UAT; confirms all acceptance criteria have been met.
- **Retrospective:** Reports requirement churn metrics; proposes improvements to the requirements process.

---

## Release Manager

### Role Summary
Release Managers plan, coordinate, and own release cycles from final QA sign-off through production deployment and post-release verification. They ensure all pre-release checkpoints are satisfied and communicate release status to all stakeholders.

### Responsibilities
- Maintain the release calendar and coordinate release windows with Developers, QA, and Operations
- Own the release checklist (see `octoacme-release-checklist.md`) and verify each item before deployment
- Coordinate go/no-go decisions with PM, QA, and Security Liaison
- Communicate release plans, deployment windows, and post-release status to Stakeholders and Support
- Manage rollback decisions and procedures when deployments fail
- Track release metrics (lead time, change failure rate, MTTR) and report to PM
- Ensure deployment runbooks are up to date before each release
- Schedule and confirm post-release monitoring periods

### Goals
- Achieve consistent, low-risk releases with measurable improvement in release frequency and change failure rate
- Provide clear, timely communication that minimizes surprise and downtime
- Maintain a reliable rollback capability for every production deployment

### Typical Communication
- Pre-release go/no-go meetings with PM, QA, and Security Liaison
- Release notes and deployment announcements to Stakeholders and Support
- Post-release status reports and incident summaries

### Interactions with Existing Roles
- Coordinates with **Project Managers** to align release windows with sprint and milestone schedules.
- Receives go/no-go quality signal from **QA** and security clearance from the **Security Liaison** before deploying.
- Notifies **Support / Customer Success** of release contents, known issues, and rollback procedures.
- Escalation: if a go/no-go decision cannot be reached, the Release Manager escalates to the Product Manager and, if necessary, to Stakeholders for a scope or timeline decision.

### Workflow Participation
- **Initiation:** Advises on release feasibility and capacity when scoping new projects.
- **Planning:** Establishes release milestones and gates in the project plan.
- **Execution:** Monitors branch health and CI status; flags risks to the release window early.
- **Release:** Owns the deployment checklist execution, go/no-go decision, and post-release verification.
- **Retrospective:** Reports release metrics; identifies checklist gaps or process improvements.

---

## Support / Customer Success

### Role Summary
Support and Customer Success team members represent the voice of the customer inside the project team. They surface user feedback, field production incidents, inform release readiness, and ensure documentation and runbooks are ready for users when features ship.

### Responsibilities
- Capture and escalate production issues and user-reported bugs to the PM and development team
- Represent customer impact in backlog prioritization discussions
- Review release notes and update support runbooks before each release
- Contribute known-issue logs and workarounds to release communication
- Participate in incident response by providing customer impact context
- Feed patterns from support tickets into retrospectives and product roadmap discussions
- Validate that self-service documentation accurately reflects shipped features
- Track customer satisfaction (CSAT/NPS) and share trends with Product Manager

### Goals
- Minimize customer-facing disruption by ensuring support is prepared before every release
- Reduce ticket volume through proactive documentation and clear release communication
- Provide a closed feedback loop between customer experience and product development

### Typical Communication
- Pre-release briefing from Release Manager (release contents, known issues, rollback plan)
- Escalation channels for high-severity production incidents
- Regular syncs with Product Manager to share support trends and customer feedback

### Interactions with Existing Roles
- Collaborates with **Product Managers** to prioritize high-impact customer-reported issues against the roadmap.
- Receives deployment details from the **Release Manager** to prepare support documentation and proactive customer communications.
- Provides customer impact context to **Developers** and **Project Managers** during incident triage.
- Escalation: if a production issue is causing widespread customer impact, Support escalates to PM and Release Manager for an emergency hotfix or rollback decision.

### Workflow Participation
- **Initiation:** Contributes customer pain points and top support themes to the problem statement.
- **Planning:** Reviews release scope for supportability; flags known documentation gaps.
- **Execution:** Monitors production for issues in the current release window; updates runbooks.
- **Release:** Reviews and approves release notes; confirms support readiness before go-live.
- **Retrospective:** Presents customer feedback and support volume data; proposes improvements.

---

## Security Liaison

### Role Summary
The Security Liaison ensures that security requirements are embedded throughout the project lifecycle, from threat modeling in planning through security scans in the release pipeline. They represent the security team's interests and provide the go/no-go security clearance for releases.

### Responsibilities
- Conduct or facilitate threat modeling for new features and integrations
- Define security acceptance criteria and non-functional requirements (authentication, authorization, data protection)
- Review architecture and design for security risks
- Ensure automated security scans (SAST, DAST, dependency audits) are integrated into CI
- Review and approve security-sensitive pull requests or infrastructure changes
- Provide security sign-off as part of the pre-release go/no-go process
- Track and drive remediation of open security findings and vulnerabilities
- Maintain the security runbook and incident response playbook

### Goals
- Prevent security vulnerabilities from reaching production by shifting security left in the SDLC
- Ensure every release has a documented security posture review
- Reduce mean time to remediate security findings

### Typical Communication
- Threat modeling sessions during project planning
- Security review comments in pull requests and design documents
- Pre-release security clearance report shared with Release Manager and PM

### Interactions with Existing Roles
- Works with **Product Managers** and **Business Analysts** during planning to define security requirements alongside functional requirements.
- Reviews **Developer** pull requests for security-sensitive changes; provides guidance on secure coding patterns.
- Provides security scan results and sign-off to the **Release Manager** as part of the release checklist.
- Escalation: if a security finding is critical and cannot be resolved before the scheduled release, the Security Liaison escalates to the PM and Release Manager to decide on delay, compensating controls, or risk acceptance.

### Workflow Participation
- **Initiation:** Reviews project scope for regulatory or compliance considerations.
- **Planning:** Conducts threat modeling; defines security acceptance criteria.
- **Execution:** Reviews PRs, monitors security scan results, and tracks open findings.
- **Release:** Provides final security sign-off on the release checklist.
- **Retrospective:** Reports security metrics (open findings, scan pass/fail rates); proposes improvements.

---

## Data Analyst

### Role Summary
Data Analysts define success metrics, instrument data pipelines, and translate raw data into actionable insights that inform product decisions, validate outcomes, and drive continuous improvement.

### Responsibilities
- Define and document key metrics, KPIs, and measurement plans for each feature
- Instrument analytics events and validate that tracking is correctly implemented by Developers
- Build and maintain dashboards and reports for Product Managers and Stakeholders
- Analyze experiment (A/B test) results and translate findings into recommendations
- Identify data quality issues and work with Developers to resolve them
- Support retrospectives with quantitative evidence of impact (e.g., adoption, performance, error rates)
- Maintain the data dictionary and documentation for all tracked events
- Advise on data privacy and compliance implications of new tracking

### Goals
- Ensure every shipped feature has measurable success criteria tracked from day one
- Accelerate data-informed decisions by providing timely, reliable insights
- Reduce reliance on anecdotal evidence in prioritization and retrospective discussions

### Typical Communication
- Measurement plan documents shared with Product Manager during planning
- Dashboard links and experiment result summaries in sprint reviews
- Ad-hoc analysis reports for Stakeholders and PdM

### Interactions with Existing Roles
- Partners with **Product Managers** to define the measurement plan for each feature before development starts.
- Works with **Developers** to instrument analytics correctly; reviews tracking implementation before release.
- Presents data-driven impact summaries to **Stakeholders** during milestone reviews.
- Escalation: if data reveals an unexpected negative impact post-release (e.g., sharp drop in engagement), the Data Analyst alerts the Product Manager and Project Manager immediately to evaluate a rollback or hotfix.

### Workflow Participation
- **Initiation:** Identifies existing data baselines and gaps relevant to the proposed feature.
- **Planning:** Produces the measurement plan; ensures tracking stories are included in the backlog.
- **Execution:** Reviews analytics instrumentation in PRs; validates data in staging.
- **Release:** Confirms tracking is live and dashboards are updated post-deployment.
- **Retrospective:** Presents quantitative outcomes; recommends metric adjustments for future iterations.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- See `octoacme-role-interactions.md` for cross-role handoff scenarios and `octoacme-release-checklist.md` for the Release Manager's go/no-go checklist.

