# DECISION-LOG.md - Entry 3

## Decision ID: DEC-003
## Topic: Primary End Users & Roles
## Status: In Development (Release 1.0)

---

## Topic 3: Primary End Users & Roles

### Overview

The portfolio management agents system serves multiple interconnected roles organized into three governance tiers:

- **Portfolio Board Tier** (Strategic portfolio-level governance): Portfolio Owner, Business Owners, CFO, Portfolio Manager
- **Steering Group Tier** (Project-level execution oversight): Project Sponsor, Senior User, Senior Supplier  
- **Execution Tier** (Day-to-day project delivery): Project Manager, Project Team Members/SMEs
- **Supporting Roles** (Process and administrative support): Financial/Resource Manager, Organizational Administrator

These roles interact with the system at different phases and have distinct needs for information, decision support, and status tracking. The structure reflects ScripeConnect12's portfolio governance model emphasizing clear accountability at each level.

---

## Portfolio Board Tier (Strategic Portfolio Governance)

### 1. Portfolio Owner (Sponsor)

**Who they are:**
Director or executive-level (CEO/COO) with ultimate responsibility for the entire portfolio, budgets, and strategic alignment of projects with organizational objectives.

**When they interact:**
- Portfolio board meetings (monthly/quarterly)
- High-level gate reviews for major initiatives
- Portfolio rebalancing and strategic decision-making
- Cross-project resource arbitration at executive level

**What they do in the system:**
- Set portfolio strategy and priorities
- Make final approval decisions on major projects
- Approve portfolio-level resource allocation
- Review portfolio health and strategic alignment
- Resolve escalations at the highest level

**What they need from the system:**
- Portfolio-level health dashboard and KPIs
- Executive summary of all active projects and their status
- Strategic alignment evidence and objective achievement tracking
- High-level risk and financial impact summaries
- Escalations requiring executive decision
- Decision audit trail for governance and compliance

**System interaction pattern:**
Portfolio Review → Assessment Summary → Executive Decision → Status Update

---

### 2. Business Owner / Division Head

**Who they are:**
Leadership representative from each business unit or division responsible for bringing business initiatives and representing departmental needs and priorities to the portfolio board.

**When they interact:**
- Portfolio board meetings
- Gate reviews for projects within their business unit
- Business case and requirements validation
- Benefit realization validation

**What they do in the system:**
- Propose and advocate for projects from their division
- Validate business case and strategic fit for their area
- Approve scope and requirements from business perspective
- Track benefits realization for their projects
- Escalate business-level conflicts or dependencies

**What they need from the system:**
- Projects filtered by their business unit
- Business case assessments and ROI projections
- Benefit realization metrics
- Risk status affecting their business area
- Clear visibility into decisions on projects affecting their division

**System interaction pattern:**
Initiative Proposal → Business Validation → Gate Assessment → Benefit Tracking

---

### 3. Chief Financial Officer (CFO)

**Who they are:**
Financial leadership responsible for portfolio-level financial governance, budget oversight, and return on investment (ROI) across all projects.

**When they interact:**
- Portfolio board meetings
- Budget planning cycles
- Financial gate reviews
- Quarterly financial reviews and variance analysis

**What they do in the system:**
- Establish and maintain portfolio financial frameworks
- Approve project budgets and financial allocations
- Monitor portfolio spending and budget variance
- Assess financial feasibility and ROI of projects
- Ensure financial compliance and reporting

**What they need from the system:**
- Portfolio budget status (total, allocated, spent)
- Project-level budget tracking and variance reporting
- Financial impact assessments for new initiatives
- ROI projections and realization tracking
- Financial risk assessment across portfolio
- Regulatory and compliance reporting

**System interaction pattern:**
Budget Planning → Financial Assessment → Budget Approval → Variance Reporting

---

### 4. Portfolio Manager

**Who they are:**
(Optional, depending on organization size) Dedicated coordinator/manager responsible for portfolio process execution, scheduling gates, managing assessments, and facilitating board operations.

**When they interact:**
- Continuously throughout portfolio lifecycle
- Gate scheduling and preparation
- Assessment coordination
- Board meeting facilitation and minutes

**What they do in the system:**
- Manage portfolio gate schedule and calendar
- Coordinate portfolio advisor assessments
- Prepare board meeting agendas and materials
- Maintain portfolio decision logs and documentation
- Monitor portfolio process compliance
- Coordinate with project managers and steering groups

**What they need from the system:**
- Portfolio calendar and gate schedule
- Assessment status tracking and workflows
- Project context and documentation repository
- Board meeting materials and decision logging
- Process compliance monitoring tools
- Portfolio metrics and KPI dashboards

**System interaction pattern:**
Gate Planning → Assessment Coordination → Board Facilitation → Documentation

---

## Steering Group Tier (Project Execution Governance)

### 5. Project Sponsor (Opdrachtgever)

**Who they are:**
Business stakeholder or executive accountable for overall project success, benefits realization, and business outcomes. Acts as the authoritative voice for the project within the organization.

**When they interact:**
- Project gate reviews (Idea, Definition, Design, Realization, Go-Live, Closure)
- Steering group meetings (typically bi-weekly during Realization)
- Escalations involving scope, timeline, budget, or strategic alignment changes
- Project closure and benefits validation

**What they do in the system:**
- Approve project idea and business case
- Validate requirements and scope before design
- Make go/no-go decisions at key gates
- Resolve conflicts between project needs and organizational constraints
- Approve changes to scope, timeline, or budget
- Sign off on project closure and benefits

**What they need from the system:**
- Clear business rationale and value proposition
- Benefit realization progress and metrics
- Project status and timeline tracking
- Risk and issue escalations requiring decision
- Change impact assessments
- Closure documentation and lessons learned

**System interaction pattern:**
Gate Review → Assessment Review → Decision/Approval → Status Monitoring → Closure Approval

---

### 6. Senior User

**Who they are:**
Primary user or representative of the end-user community who will operate or benefit from the project deliverables. Ensures project outputs meet user needs.

**When they interact:**
- Requirements and scope definition (Definition phase)
- Design review and validation
- Acceptance criteria definition
- Testing and UAT (throughout Realization)
- Go-Live readiness assessment
- Post-implementation support planning

**What they do in the system:**
- Validate requirements reflect actual user needs
- Review design against user workflows
- Define acceptance criteria and success measures
- Participate in testing and validation
- Identify risks from user perspective
- Sign off on deliverables meeting user needs

**What they need from the system:**
- Clear requirements and scope (with user context)
- Design documentation and mockups
- Testing plans and progress
- Change impact analysis (how changes affect users)
- Training and go-live readiness documentation
- Post-implementation feedback mechanisms

**System interaction pattern:**
Requirements Input → Design Validation → Testing Participation → UAT Sign-Off → Go-Live Readiness

---

### 7. Senior Supplier

**Who they are:**
Primary delivery organization or lead supplier (can be internal IT/development team or external implementation partner/contractor) responsible for technical delivery and solution implementation.

**When they interact:**
- Throughout project execution phases
- Design and technical feasibility assessment
- Implementation planning and execution
- Quality and testing coordination
- Escalation of technical blockers or risks
- Operational handover

**What they do in the system:**
- Assess technical feasibility and approach
- Plan and coordinate implementation work
- Manage technical quality and testing
- Identify technical risks and mitigation approaches
- Escalate blockers and impediments
- Support operational transition and go-live

**What they need from the system:**
- Clear requirements and design specifications
- Project context and dependencies
- Risk and issue logs (with technical focus)
- Testing status and quality metrics
- Change management and scope control
- Deployment and operational readiness checklist
- Post-implementation support agreements

**System interaction pattern:**
Design Assessment → Implementation Planning → Execution & QA → Escalation Management → Go-Live → Handover

---

## Execution Tier Roles

### 8. Project Manager

**Who they are:**
Business stakeholder or executive accountable for project success, benefits realization, and stakeholder satisfaction.

**When they interact:**
- Idea and Definition phase review and approval
- Project closure review
- Escalations involving scope, timeline, or budget changes
- Ad-hoc updates and milestone reviews

**What they do in the system:**
- Approve project idea and initial scope
- Sign off on project brief before realization
- Approve project closure and benefits validation
- Address escalations requiring business-level decisions
- Validate business case and benefit realization

**What they need from the system:**
- Clear business rationale and value proposition
- Benefit realization progress and metrics
- Budget and timeline tracking
- Risk status and mitigation approach
- Escalation notification with impact summary
- Closure documentation and lessons learned

**System interaction pattern:**
Idea Approval → Brief Approval → Status Monitoring → Closure Approval

---

## Execution Tier Roles

### 4. Project Manager

**Who they are:**
Day-to-day project leader responsible for execution, team coordination, schedule management, and operational reporting.

**When they interact:**
- Throughout all project phases
- Daily/weekly project execution
- Regular status reporting
- Issue and risk management
- Escalation preparation and follow-up

**What they do in the system:**
- Create and maintain project documentation (scope, plan, risks, issues)
- Prepare status reports for governance review
- Escalate issues and risks requiring decision
- Track project metrics and progress
- Coordinate team activities and dependencies
- Manage communication to stakeholders

**What they need from the system:**
- Project context and decision history (what was decided and why)
- Status update templates and reporting guidance
- Issue and risk logging and tracking
- Escalation procedures and decision routing
- Audit trail of approvals and decisions
- Integration with project planning tools (timeline, capacity, budget)
- Communication templates for stakeholder updates

**System interaction pattern:**
Phase Entry → Status Tracking → Issue Management → Escalation → Decision Follow-up → Phase Exit

---

### 9. Project Team Member / Subject Matter Expert

**Who they are:**
Execution-level contributors (developers, architects, business analysts, etc.) and domain experts involved in project delivery under the Senior Supplier direction.

**When they interact:**
- During project planning and estimation
- As input to risk and issue identification
- During technical/domain decision points
- Status reporting on their work areas
- During testing and quality validation

**What they do in the system:**
- Provide input to project scope and feasibility assessment
- Identify technical or operational risks
- Contribute to issue resolution and decision-making
- Report progress on assigned work
- Validate acceptance criteria and deliverables
- Participate in testing and quality assurance

**What they need from the system:**
- Clear project scope and objectives (their role in delivery)
- Decision context and rationale for decisions affecting their work
- Risk and issue logs relevant to their work areas
- Clear acceptance criteria and success measures
- Change/decision notification when scope/approach changes
- Work assignment and status tracking

**System interaction pattern:**
Input to Planning → Risk/Issue Input → Decision Context → Status Contribution → Quality Validation

---

## Supporting Roles

### 10. Financial/Resource Manager

**Who they are:**
Operational support role responsible for budget tracking, resource allocation, and capacity planning.

**When they interact:**
- During project budgeting and cost estimation
- Monthly/quarterly budget reviews
- Resource conflict escalation
- Budget variance analysis
- Project closure financial review

**What they do in the system:**
- Track project budget and spending
- Identify budget variances and escalate
- Monitor resource allocation and utilization
- Identify capacity constraints
- Report on portfolio financial health
- Validate cost data in closures

**What they need from the system:**
- Project budget and spending data
- Resource allocation and utilization tracking
- Budget variance alerts and summaries
- Portfolio-level financial reporting
- Cost data for escalations and decisions
- Audit trail of budget-related decisions

**System interaction pattern:**
Budget Input → Tracking → Variance Reporting → Escalation → Decision Impact

---

### 11. Organizational Administrator / System Manager

**Who they are:**
Operational role responsible for system administration, governance process enforcement, and documentation management.

**When they interact:**
- System setup and configuration
- User access management
- Process compliance monitoring
- Document archival and retrieval
- Reporting and metrics generation

**What they do in the system:**
- Maintain user access and permissions
- Ensure process compliance (gates followed, decisions logged, escalations tracked)
- Archive and manage project records
- Generate portfolio reports and dashboards
- Maintain system health and data integrity

**What they need from the system:**
- User and permissions management tools
- Audit trail and compliance reporting
- Process compliance monitoring and alerts
- Document management and search
- Portfolio dashboard and reporting
- System health and usage metrics

**System interaction pattern:**
Configuration → Monitoring → Compliance → Reporting

---

## Cross-Cutting User Needs

All roles share these common needs:

1. **Clear Process Orientation**
   - Know which phase a project is in
   - Understand what decisions/actions are needed at current phase
   - Know what happens next and when

2. **Context & Decision History**
   - Understand why decisions were made (rationale, options considered)
   - Access prior phase assessments and findings
   - Know who made decisions and when

3. **Status & Visibility**
   - Know project/portfolio status at a glance
   - Identify risks, issues, and escalations requiring action
   - Track progress toward milestones

4. **Coordination Support**
   - Know who else is involved (dependencies, stakeholders)
   - Understand what's expected of them at each phase
   - Receive timely notifications of phase transitions or decisions

5. **Audit Trail**
   - Document all decisions and approvals
   - Track change history and rationale
   - Support retrospectives and process improvement

---

## Organizational Context Assumptions

The system is designed to support:

- **Any organizational size** — from small teams to large enterprises
- **Any industry vertical** — roles are functional, not industry-specific
- **Varying governance maturity** — from minimal governance to highly structured
- **Multiple project types** — strategic, operational, maintenance, transformation

The role descriptions above define functional needs, not job titles. A small organization might combine multiple roles into fewer people; a large organization might specialize roles further.

---

## Source & Alignment Notes

This role structure is based on **ScripeConnect12's portfolio governance framework** documented in "Portfolio Management Rolbeschrijvingen.rtf". Key alignment points:

- **Portfolio Board composition** reflects ScripeConnect12's emphasis on Portfolio Owner (executive sponsor), Business Owners (divisional representation), CFO (financial governance)
- **Steering Group structure** follows ScripeConnect12's standard model of Project Sponsor (Opdrachtgever), Senior User, and Senior Supplier
- **Three-tier model** (Portfolio Board → Steering Group → Execution) emphasizes clear accountability and decision authority at each level
- **Flexibility in organization size**: Portfolio Manager role is optional; smaller organizations may have fewer distinct positions

---

## Questions for Refinement (TBD)

1. **Advisor Roles vs. User Roles**: Do we need to define the 6 portfolio advisor roles (Project Idea Advisor, Brief Advisor, etc.) separately from these end-user roles? (Advisors provide assessment; users make decisions and execute)

2. **External Stakeholders**: Should we include external roles (clients, vendors, regulatory bodies) who might interact with the system in larger, more complex implementations?

3. **Portfolio Manager Necessity**: When is a dedicated Portfolio Manager role needed vs. embedded in Portfolio Owner or Executive/PMO responsibilities?

4. **Cross-Project Roles**: Are there roles needed for managing dependencies and cross-project issues that we haven't identified?

5. **Role-Specific Features**: What specific system features, dashboards, or UI/UX elements are unique to each role's workflow?

6. **Access & Permissions**: How should role-based access control be implemented? What can/cannot each role see/do?

7. **Integration Points**: Which external systems (HR, Finance, Project Management tools) should integrate with the portfolio management system, and how does each role use those integrations?

---

## Decision Summary

**Completed:**
- Aligned role structure with ScripeConnect12's Portfolio Board and Steering Group model
- Expanded Portfolio Board from generic "member" into 4 specific roles: Portfolio Owner, Business Owner, CFO, Portfolio Manager
- Expanded Steering Group from generic "member" into 3 specific roles: Project Sponsor, Senior User, Senior Supplier
- Clarified reporting relationships and interactions between tiers
- Refined role descriptions to emphasize decision authority and responsibilities

**What remains to be decided:**
- Whether to expand role descriptions with use cases, pain points, or specific feature requirements
- Document role-specific UI/UX needs and dashboard views
- Define role-based access/permission levels (what each role can see/do in system)
- Integration requirements for each role (HR systems, Finance systems, Project Management tools)
- Portfolio Manager role necessity and scope (organization size-dependent)

**Next steps:**
- Validate complete role structure against target customer profiles for Decision Velocity
- Define access/permission model based on role tiers
- Plan role-specific features, dashboards, and integrations
- Develop role-specific training/onboarding materials for implementation

