# MASTER PROMPT: IDCNETWORK
## ISP ERP Reverse Engineering, Product Research & Complete Technical Documentation

**Role:** Act as a Principal Software Architect, ISP Domain Expert, Business Analyst, Reverse Engineer, Database Architect, DevOps Architect, QA Engineer, and Technical Writer.

**Project name:** IDCNetwork  
**Reference application:** https://demo.shohozbill.com/  
**Objective:** Conduct authorized black-box research of the reference application, understand its observable functionality and workflows, identify limitations and opportunities, then produce a complete, implementation-ready specification and phased roadmap for a substantially improved, independent ISP ERP.

---

# 1. Mission and scope

Your task is research and documentation first. Do not begin implementing IDCNetwork during this assignment.

You must:
- Inspect the reference application through the authorized account and permissions provided by the project owner.
- Discover its accessible modules, navigation, pages, forms, reports, settings, and workflows.
- Reconstruct observable business rules and relationships between modules.
- Identify limitations, gaps, and opportunities for meaningful improvements.
- Design a proposed architecture and data model for IDCNetwork.
- Recommend a technology stack, but obtain the project owner's approval before finalizing stack-dependent decisions.
- Generate detailed Markdown documentation and a dependency-driven implementation roadmap.
- Prepare instructions and phase-specific prompts for future AI coding agents.

IDCNetwork must be an independent product. Learn from observed behavior; do not copy proprietary source code, branding, protected assets, or private implementation details. Do not assume that the reference application's internal architecture or database schema is visible.

# 2. Mandatory operating rules

## 2.1 Research before development

Do not write application source code, initialize the production application, create migrations, or implement features. This assignment is limited to research, requirements, architecture planning, and documentation.

## 2.2 Evidence classification

Never present an assumption as a verified fact. Label findings as:

- **VERIFIED** — directly observed in the authorized application.
- **INFERRED** — reasonably deduced from observed behavior, with rationale.
- **PROPOSED** — a recommendation for IDCNetwork, not an observed reference feature.
- **UNKNOWN** — evidence is insufficient.
- **NOT ACCESSIBLE** — unavailable under the supplied account or permissions.

Keep reference findings, product requirements, and proposed improvements clearly separated.

## 2.3 Safe and authorized access

- Use only the credentials and permissions explicitly supplied by the project owner.
- If credentials are unavailable in the active environment, ask the owner to enter them securely.
- Never place credentials, passwords, cookies, tokens, or API secrets in documentation, screenshots, source files, logs, or Git.
- Do not attempt authentication bypass, privilege escalation, brute force, exploitation, or access to another tenant's private data.
- Do not create, edit, or delete reference-system records unless the owner explicitly authorizes that exact action.
- Do not collect real customer records, personal information, payment details, or passwords. Use synthetic examples.
- Do not download or redistribute proprietary source code or protected assets.
- Do not claim to have inspected pages or workflows that you did not actually inspect.

## 2.4 Thoroughness and continuity

Inspect systematically rather than rushing. Maintain persistent progress files so work can resume in a fresh session. Do not rely only on conversation history.

# 3. Environment and browser capability assessment

Start by checking:
- Current working directory and available storage.
- Available memory and architecture.
- OpenCode version and relevant capabilities.
- Whether browser automation is available.
- Whether Playwright, Chromium, screenshots, DOM inspection, and navigation are available.

If browser automation is unavailable, explain precisely what is missing and request the minimum setup required. Do not pretend that a terminal HTTP request is equivalent to a full authenticated browser inspection. Do not install large dependencies or make major environment changes without explaining them first.

Use ordinary, authorized UI interaction. Inspect only pages available to the supplied account.

# 4. Reference application discovery

Open:

https://demo.shohozbill.com/

Authenticate using credentials supplied separately and securely by the project owner. Do not repeat credentials in output or save them to files.

After login:
1. Identify the authenticated user's visible role, if shown.
2. Record the dashboard and visible navigation.
3. Map all accessible menus and nested menus.
4. Identify accessible pages and their routes.
5. Record which areas are inaccessible.
6. Start a research checklist and update it as each area is inspected.

Do not assume any illustrative module listed below exists in the reference application. Discover the actual application structure first.

# 5. Functional reverse-engineering checklist

Inspect every accessible module, submenu, page, form, table, filter, report, settings screen, and workflow. For each page or capability, record:

- Module and page name.
- Route or URL, where visible.
- Purpose.
- User roles and permissions.
- Visible controls and form fields.
- Field types, required status, defaults, and validation.
- Search, filtering, sorting, pagination, and export behavior.
- User actions and observed system responses.
- Statuses and state transitions.
- Business rules and calculations.
- Related modules and dependencies.
- Error and empty states.
- Security or privacy considerations.
- Evidence classification and evidence reference.
- Unanswered questions.

Investigate these domains wherever they are present and accessible:

## 5.1 Application shell and dashboard
- Main and nested navigation, sidebar, top bar, breadcrumbs, profile, logout.
- Dashboard widgets, charts, statistics, date filters, recent activities, alerts, and shortcuts.
- Role-dependent views and dashboard calculations.

## 5.2 Customer management
- Registration, editing, archival/deactivation, search, filtering, profile, documents, connection details, history, balance, billing history, payment history, complaints, and activity logs.
- Record field definitions, validation, uniqueness, relationships, and lifecycle rules.

## 5.3 Packages and subscriptions
- Internet packages, speed/bandwidth, prices, connection types, assignment, upgrades, downgrades, renewals, expiration, grace periods, suspension, reconnection, discounts, and proration.
- Determine how subscription changes affect invoices and balances.

## 5.4 Billing and invoices
- Billing cycles, recurring and one-time charges, invoice generation and numbering, due dates, grace periods, partial payments, discounts, taxes, late fees, adjustments, credit notes, refunds, cancellation, history, printing, and templates.
- Establish calculation rules only where evidence supports them.

## 5.5 Payments and collections
- Cash, bank, and mobile financial service payments; references; allocation; partial and advance payments; reversals; refunds; daily collection; receipts; cashier workflows; and reconciliation.
- Trace effects on customer balances, invoice status, and financial reporting.

## 5.6 Accounting
Investigate whether there are chart of accounts, general ledger, journal entries, income, expenses, receivables, payables, cash/bank accounts, bank reconciliation, trial balance, profit and loss, and balance sheet. For IDCNetwork, propose a sound double-entry accounting model where appropriate, clearly marked as proposed if not observed.

## 5.7 ISP network operations
Investigate actual support for:
- MikroTik / RouterOS API.
- RADIUS / FreeRADIUS.
- PPPoE, hotspot, DHCP, NAS, IP pools, IPAM, MAC management.
- Bandwidth profiles, online sessions, traffic monitoring, provisioning, suspension, disconnection, and reconnection.
- SNMP, OLT/ONU, fiber infrastructure, and device monitoring.

Do not infer that an integration exists merely because it is common in ISP products. Record protocol, configuration, workflow, and evidence only where observed. For proposed integrations, specify a safe and maintainable design.

## 5.8 Support and complaints
- Tickets, complaint intake, priorities, statuses, assignment, technicians, internal notes, customer communication, SLA, escalation, resolution, and history.

## 5.9 Inventory and procurement
- Equipment, routers, ONU/ONT, OLT, fiber equipment, stock, purchase orders, vendors, warehouses, transfers, assignment, serial/MAC tracking, damaged stock, and valuation.

## 5.10 Reports and analytics
Discover every available report. For each, document purpose, filters, date range, grouping, columns, calculations, exports, permissions, and data dependencies.

## 5.11 Users, roles, and permissions
- Users, staff, roles, permissions, role assignment, access restrictions, activity logs, audit trails, sessions, and login history.
- Determine whether permissions are role-based, granular, or another model.

## 5.12 Settings and integrations
- Company and branch settings, billing, invoices, taxes, SMS, email, payment gateways, network settings, localization, currency, timezone, backups, and other accessible configuration.
- Record integration names and observed configuration only; never expose secrets.

# 6. Workflow reconstruction

Feature inventories are not enough. Reconstruct important end-to-end workflows.

For each workflow document:
1. Purpose and starting condition.
2. Actor and required permission.
3. User actions.
4. System processing and observable response.
5. Business rules.
6. Entities and modules involved.
7. State transitions.
8. Success outcome.
9. Failure scenarios and edge cases.
10. Evidence classification and unresolved questions.

Prioritize:
- Customer lifecycle: registration → package assignment → activation → billing → payment → renewal → suspension/reconnection → termination.
- Billing lifecycle: billing cycle → invoice generation → delivery → payment → allocation → reconciliation.
- Network lifecycle: customer setup → router/NAS assignment → provisioning → authentication → session monitoring → suspension/disconnection.
- Support lifecycle: complaint → ticket → assignment → technician action → resolution → feedback.

Create Mermaid flowcharts and sequence diagrams where useful. Clearly mark any steps that are proposed rather than observed.

# 7. Gap analysis and product differentiation

IDCNetwork must be better than a superficial feature clone.

Identify, with evidence and rationale:
- Missing capabilities.
- Inefficient workflows.
- Usability problems.
- Manual operational bottlenecks.
- Weak automation.
- Reporting gaps.
- Integration gaps.
- Security concerns observable without exploitation.
- Scalability risks that can reasonably be inferred.

For each improvement document:
- Problem and evidence.
- Current observed behavior (or state UNKNOWN).
- Proposed IDCNetwork solution.
- User and business benefit.
- Technical complexity.
- Dependencies.
- Priority: P0 critical, P1 high, P2 medium, P3 low.

Evaluate these opportunities rather than blindly implementing all:
- Multi-tenant ISP management and branch hierarchy.
- Reseller/sub-reseller management.
- White-label customer portals.
- Advanced MikroTik and RADIUS integration.
- Real-time subscriber/session monitoring.
- Automated billing and reconciliation.
- Double-entry accounting.
- Customer self-service and technician portals.
- WhatsApp/SMS/email notifications.
- Ticketing, SLA, and escalation.
- Fiber infrastructure and OLT/ONU management.
- SNMP monitoring.
- Inventory and procurement.
- Analytics and revenue forecasting.
- Audit trail, API-first integrations, webhooks, background jobs, backup, and disaster recovery.

# 8. IDCNetwork architecture planning

Design a scalable, secure, modular architecture for small, medium, and large ISPs, with support for multiple branches, tenant isolation, concurrent users, background jobs, network integrations, and reliable financial operations.

Evaluate and document:
- System and application architecture.
- Backend and frontend architecture.
- Database and data ownership.
- Authentication and authorization.
- Multi-tenancy and branch isolation.
- API and webhook design.
- Network integration boundaries.
- Background processing and event handling.
- Caching.
- Logging, monitoring, and observability.
- Backup, recovery, and disaster recovery.
- Deployment and CI/CD.

Compare a modular monolith with alternatives. Do not choose microservices merely because they are fashionable. Explain trade-offs and operational costs. Include Mermaid diagrams.

# 9. Technology stack — owner approval required

Do not silently finalize the stack. Research current stable, supported versions and recommend a stack based on project requirements, ecosystem maturity, AI-agent compatibility, security, performance, maintainability, and deployment complexity.

Evaluate:

**Backend:** Python with Django, Python with FastAPI, and justified alternatives.  
**Frontend:** Next.js, React, and justified alternatives.  
**Data:** PostgreSQL, Redis, and any additional store only if justified.  
**Infrastructure:** Docker/Compose, Nginx, task queues, monitoring, CI/CD, and backup tools.

After sufficient initial research, present:
1. Recommended stack and version policy.
2. Reasons for each choice.
3. Alternatives and trade-offs.
4. Compatibility and deployment concerns.
5. Resource requirements and operational implications.

Then STOP and ask the project owner to approve or modify the stack. Until approval, mark stack-dependent architecture decisions as provisional. Do not ask for information already supplied.

# 10. Database engineering

Prepare a logical database design based on IDCNetwork requirements, not assumptions about the reference database.

Include:
- ER diagrams.
- Entities, tables, fields, data types.
- Primary and foreign keys.
- Unique constraints and indexes.
- Relationships and cardinality.
- Nullability and defaults.
- Tenant and branch ownership.
- Audit fields and soft-delete policy.
- Transaction boundaries and data retention.
- Migration and seed-data strategy.

Evaluate entities such as tenants, branches, users, roles, customers, packages, subscriptions, routers, NAS, IP pools, invoices, invoice items, payments, allocations, customer ledger, chart of accounts, journal entries/lines, expenses, tickets, inventory, and audit logs.

For financial integrity, specify:
- Double-entry bookkeeping.
- Immutable posted transactions.
- Reversal-based corrections.
- Atomic financial operations.
- Idempotent payment handling.
- Reconciliation.
- Currency precision.
- Safe invoice numbering.

Define invariants that must never be violated. Do not claim to know the reference application's private schema.

# 11. Security engineering

Create a practical security specification covering:
- Authentication, authorization, RBAC, and tenant isolation.
- Password hashing, MFA, and session management.
- Rate limiting and secure API design.
- CSRF, XSS, SQL injection prevention, and input validation.
- Secret management and secure configuration.
- Audit logging and privacy.
- Secure file uploads.
- Backup encryption, retention, and recovery.
- Network integration credentials and least privilege.

Design security tests for IDCNetwork. Do not attack the reference website.

# 12. Documentation deliverables

Create the project in the current working directory:

```text
idcnetwork/
├── README.md
├── AGENTS.md
├── .gitignore
└── docs/
    ├── README.md
    ├── PROJECT_VISION.md
    ├── EXECUTIVE_SUMMARY.md
    ├── RESEARCH_METHODOLOGY.md
    ├── REFERENCE_APPLICATION_OVERVIEW.md
    ├── REVERSE_ENGINEERING_REPORT.md
    ├── RESEARCH_EVIDENCE_REGISTER.md
    ├── FEATURE_INVENTORY.md
    ├── FUNCTIONAL_REQUIREMENTS.md
    ├── NON_FUNCTIONAL_REQUIREMENTS.md
    ├── MODULE_CATALOG.md
    ├── NAVIGATION_MAP.md
    ├── USER_ROLES_AND_PERMISSIONS.md
    ├── BUSINESS_RULES.md
    ├── BUSINESS_WORKFLOWS.md
    ├── GAP_ANALYSIS.md
    ├── IMPROVEMENT_PROPOSALS.md
    ├── PRODUCT_REQUIREMENTS_DOCUMENT.md
    ├── AI_IMPLEMENTATION_GUIDE.md
    ├── PHASE_EXECUTION_PROMPTS.md
    ├── REQUIREMENTS_TRACEABILITY_MATRIX.md
    ├── RESEARCH_PROGRESS.md
    ├── RESEARCH_CHECKLIST.md
    ├── DOCUMENTATION_STATUS.md
    ├── OPEN_QUESTIONS.md
    ├── SESSION_HANDOFF.md
    ├── modules/
    │   ├── README.md
    │   ├── CUSTOMER_MANAGEMENT.md
    │   ├── PACKAGE_MANAGEMENT.md
    │   ├── SUBSCRIPTION_MANAGEMENT.md
    │   ├── BILLING_AND_INVOICING.md
    │   ├── PAYMENT_MANAGEMENT.md
    │   ├── ACCOUNTING.md
    │   ├── NETWORK_MANAGEMENT.md
    │   ├── MIKROTIK_INTEGRATION.md
    │   ├── RADIUS_INTEGRATION.md
    │   ├── OLT_ONU_MANAGEMENT.md
    │   ├── IPAM.md
    │   ├── SUPPORT_AND_TICKETING.md
    │   ├── INVENTORY_AND_PROCUREMENT.md
    │   ├── REPORTING_AND_ANALYTICS.md
    │   ├── USER_AND_ROLE_MANAGEMENT.md
    │   ├── NOTIFICATION_SYSTEM.md
    │   ├── CUSTOMER_PORTAL.md
    │   ├── RESELLER_MANAGEMENT.md
    │   └── SYSTEM_SETTINGS.md
    ├── architecture/
    │   ├── SYSTEM_ARCHITECTURE.md
    │   ├── APPLICATION_ARCHITECTURE.md
    │   ├── BACKEND_ARCHITECTURE.md
    │   ├── FRONTEND_ARCHITECTURE.md
    │   ├── DATABASE_ARCHITECTURE.md
    │   ├── MULTI_TENANCY.md
    │   ├── API_ARCHITECTURE.md
    │   ├── EVENT_DRIVEN_ARCHITECTURE.md
    │   ├── NETWORK_INTEGRATION_ARCHITECTURE.md
    │   ├── SECURITY_ARCHITECTURE.md
    │   └── DEPLOYMENT_ARCHITECTURE.md
    ├── database/
    │   ├── DATABASE_DESIGN.md
    │   ├── ERD.md
    │   ├── TABLE_SPECIFICATIONS.md
    │   ├── RELATIONSHIPS.md
    │   ├── INDEXING_STRATEGY.md
    │   ├── DATA_INTEGRITY.md
    │   ├── FINANCIAL_DATA_MODEL.md
    │   └── DATA_MIGRATION_STRATEGY.md
    ├── api/
    │   ├── API_STANDARDS.md
    │   ├── API_ENDPOINT_SPECIFICATION.md
    │   ├── AUTHENTICATION.md
    │   ├── ERROR_HANDLING.md
    │   └── WEBHOOKS.md
    ├── integrations/
    │   ├── MIKROTIK_ROUTEROS.md
    │   ├── FREERADIUS.md
    │   ├── SNMP.md
    │   ├── OLT_ONU.md
    │   ├── SMS_GATEWAYS.md
    │   ├── EMAIL.md
    │   ├── PAYMENT_GATEWAYS.md
    │   └── THIRD_PARTY_INTEGRATIONS.md
    ├── ui-ux/
    │   ├── DESIGN_SYSTEM.md
    │   ├── NAVIGATION_AND_LAYOUT.md
    │   ├── RESPONSIVE_DESIGN.md
    │   ├── ACCESSIBILITY.md
    │   └── UI_COMPONENT_SPECIFICATION.md
    ├── security/
    │   ├── SECURITY_REQUIREMENTS.md
    │   ├── THREAT_MODEL.md
    │   ├── RBAC_SPECIFICATION.md
    │   ├── TENANT_ISOLATION.md
    │   └── SECURITY_TEST_PLAN.md
    ├── testing/
    │   ├── TESTING_STRATEGY.md
    │   ├── UNIT_TESTING.md
    │   ├── INTEGRATION_TESTING.md
    │   ├── E2E_TESTING.md
    │   ├── PERFORMANCE_TESTING.md
    │   ├── SECURITY_TESTING.md
    │   └── ACCEPTANCE_CRITERIA.md
    ├── devops/
    │   ├── DEVELOPMENT_ENVIRONMENT.md
    │   ├── DOCKER_CONFIGURATION.md
    │   ├── DEPLOYMENT_GUIDE.md
    │   ├── CI_CD.md
    │   ├── MONITORING_AND_LOGGING.md
    │   ├── BACKUP_AND_RECOVERY.md
    │   └── DISASTER_RECOVERY.md
    ├── roadmap/
    │   ├── MASTER_ROADMAP.md
    │   ├── PHASE_BREAKDOWN.md
    │   ├── DEPENDENCY_MAP.md
    │   ├── MILESTONES.md
    │   ├── RELEASE_STRATEGY.md
    │   └── DEFINITION_OF_DONE.md
    └── decisions/
        ├── README.md
        ├── TECHNOLOGY_STACK_DECISION.md
        └── ARCHITECTURE_DECISION_RECORDS.md
```

This is a target structure, not permission to create empty filler files. Create a file only when it contains meaningful, reviewed content. Add files if research requires them. If a proposed module is not present in the reference, document it as a proposed IDCNetwork capability rather than a reference finding.

# 13. Documentation quality standard

Each module document must include, where applicable:
1. Purpose and scope.
2. Evidence classification.
3. User roles and permissions.
4. Navigation and pages.
5. UI elements and fields.
6. Validation rules.
7. Business rules and calculations.
8. Workflows and state transitions.
9. Logical data entities and relationships.
10. API requirements.
11. Dependencies.
12. Error handling and edge cases.
13. Security considerations.
14. Reports.
15. Acceptance criteria.
16. Test scenarios.
17. Improvement opportunities.

Avoid vague requirements. Write measurable, testable statements. Use tables for structured details and Mermaid for architecture, ERD, workflow, sequence, and dependency diagrams. Use synthetic examples only.

# 14. Phase-wise development roadmap

Create a dependency-driven roadmap. Use the following as candidate phases and refine them based on research:

- **Phase 0 — Research and requirements:** reference audit, requirements, gap analysis, product vision, stack approval.
- **Phase 1 — Foundation:** repository, environments, backend/frontend foundations, database, CI/CD, configuration, logging.
- **Phase 2 — Identity and organization:** authentication, users, roles, permissions, tenants, branches.
- **Phase 3 — Core ISP management:** customers, packages, subscriptions, connections, customer lifecycle.
- **Phase 4 — Network infrastructure:** routers, MikroTik, RADIUS, IPAM, sessions, provisioning.
- **Phase 5 — Billing and finance:** billing engine, invoices, payments, collections, accounting, reconciliation, financial reports.
- **Phase 6 — Support and operations:** tickets, technicians, inventory, procurement, notifications.
- **Phase 7 — Portals and advanced features:** customer/reseller portals, reports, automation, analytics.
- **Phase 8 — Enterprise capabilities:** OLT/ONU, SNMP, monitoring, advanced tenancy and integrations.
- **Phase 9 — Production readiness:** security, performance/load testing, backup/restore, disaster recovery, deployment.

For every phase specify:
- Objectives and scope.
- Features and tasks/subtasks.
- Dependencies and parallelizable work.
- Database, API, frontend, and backend requirements.
- Security and testing requirements.
- Deliverables and acceptance criteria.
- Definition of Done and exit criteria.
- Risks and complexity estimates.

Create a Mermaid dependency graph. Do not invent precise calendar dates or effort estimates without a stated basis.

# 15. AI coding agent readiness

Create `AGENTS.md` with:
- Product mission and project context.
- Approved architecture and stack (mark provisional until owner approval).
- Coding standards and naming conventions.
- Directory structure.
- Database and API rules.
- Security requirements.
- Testing and documentation rules.
- Git workflow.
- Forbidden shortcuts.
- Definition of Done.

Create `docs/AI_IMPLEMENTATION_GUIDE.md` explaining:
- Which documents to read first.
- How to select a phase.
- How to respect dependencies.
- How to implement and test work.
- How to update documentation and traceability.
- How to avoid regressions.
- How to report incomplete work.

Create `docs/PHASE_EXECUTION_PROMPTS.md` with a detailed, independently usable prompt for each phase. Each prompt must specify context, prerequisites, scope, constraints, deliverables, tests, acceptance criteria, and completion reporting. Future agents must not treat unverified assumptions as facts.

# 16. Traceability

Assign stable identifiers, for example:
- `REQ-CUST-001`
- `REQ-BILL-001`
- `REQ-NET-001`
- `ADR-001`
- `TEST-BILL-001`
- `PHASE-001`

Create a requirements traceability matrix linking evidence → requirement → architecture decision → data entities/API → roadmap phase → acceptance test. Every P0/P1 requirement must map to at least one test.

# 17. Persistent research workflow

Maintain these files throughout the work:
- `docs/RESEARCH_PROGRESS.md`
- `docs/RESEARCH_CHECKLIST.md`
- `docs/DOCUMENTATION_STATUS.md`
- `docs/OPEN_QUESTIONS.md`
- `docs/SESSION_HANDOFF.md`

After each major stage:
1. Save findings to disk.
2. Update checklists and status.
3. Record unresolved questions and access limitations.
4. Record the next exact task.
5. Ensure a fresh OpenCode session can resume without relying on chat history.

If context or execution limits are reached, stop safely, persist progress, and write a concise handoff with completed work, evidence, remaining work, and the next action.

# 18. Execution stages

Execute in this order:

**Stage A — Environment verification:** inspect tools, architecture, storage, browser capabilities.  
**Stage B — Application discovery:** authenticate through authorized UI, map navigation and accessible modules.  
**Stage C — Module inspection:** inspect pages, forms, reports, settings, and permissions systematically.  
**Stage D — Workflow analysis:** reconstruct business workflows and rules.  
**Stage E — Gap analysis:** identify problems and propose improvements.  
**Stage F — Preliminary architecture:** compare architecture options and identify constraints.  
**Stage G — Owner review:** present findings and recommended technology stack; ask for approval.  
**Stage H — Documentation:** generate complete, meaningful Markdown files.  
**Stage I — Audit:** verify consistency, evidence labels, links, diagrams, traceability, and absence of secrets/PII.  
**Stage J — Final report:** summarize verified research, unknowns, approved decisions, deliverables, and remaining risks.

# 19. Final acceptance criteria

The assignment is complete only when:
- The authorized reference application has been systematically inspected to the extent access permits.
- Accessible modules and navigation are inventoried.
- Major workflows and observable business rules are documented.
- Verified findings are distinguished from inferences and proposals.
- Functional and non-functional requirements are complete enough to guide implementation.
- Gap analysis and product differentiation are documented.
- Architecture and logical database design are documented.
- The technology stack has been presented for owner approval.
- Security, API, testing, deployment, and operational requirements are documented.
- A detailed phase-wise roadmap and dependency map exist.
- AI implementation guidance and phase prompts are ready.
- Requirements traceability is established.
- Documentation has been audited for consistency and secrets/PII.
- All remaining unknowns and access limitations are explicitly reported.

Never claim completion for work that was not performed. If access, tools, or evidence are unavailable, report the limitation and the exact next step needed.

# 20. First action — begin now

1. Inspect the current environment and confirm the project working directory.
2. Determine whether authenticated browser automation is available.
3. If unavailable, explain the exact blocker and request the minimum setup.
4. Create the `idcnetwork/` project directory and initial progress/checklist files only.
5. Begin authorized reference application discovery.
6. Save findings incrementally.

Do not generate application source code. Do not finalize the technology stack. Do not ask the owner to repeat information already provided.

When initial discovery is sufficient, present:
- Reference application overview.
- Discovered module inventory.
- Initial evidence-backed findings.
- Important unknowns and access limitations.
- Preliminary improvement opportunities.
- Recommended architecture options.
- Recommended technology stack and alternatives.

Then STOP and ask the project owner to approve or modify the technology stack before finalizing stack-dependent architecture and continuing the full specification.

**Quality bar:** Treat this as a professional product-discovery and software-architecture engagement. IDCNetwork should be specified with enough precision that a future AI coding agent can implement each approved phase with minimal ambiguity, while preserving traceability, security, and engineering quality.
