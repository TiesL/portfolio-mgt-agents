# Decision Log — Portfolio Management Agents

This log records the product/architecture decisions made during specification of the Portfolio Management Agents system, including the options considered and the rationale for each choice. It is the single source of truth for "why is it built this way" — consult it before proposing changes that would contradict a logged decision, and add a new entry (don't silently overwrite) when a decision is revisited.

Detailed role and persona definitions referenced in Entry 3 live in [`roles-and-personas.md`](./roles-and-personas.md).

---

## Entry 1

**Decision ID:** DEC-001
**Topic:** Agent Decision-Making Authority & Scope
**Status:** Approved (Release 1.0)

**Decision Made:**
Option C — Assessment + Modification Rights (with phased autonomy approach)

**Options Considered:**
- Option A: Assessment & Recommendation Only
- Option B: Assessment + Automated Decisions (Defined Rules)
- **Option C: Assessment + Modification Rights** → CHOSEN
- Option D: Custom approach

**Rationale:**
In Release 1.0, human decision-makers retain all Go/No-Go authority. Agents document project facts and status both:
- **Prior to decisions:** comprehensive assessment and recommendations provided to humans
- **Subsequent to decisions:** agents update project status/metadata in the system based on human-approved decisions

This approach:
1. Preserves human authority in decision-making (critical for governance)
2. Automates documentation & status tracking (reduces manual work)
3. Creates an audit trail and single source of truth for project data
4. Positions for future releases where agents can make autonomous decisions within defined, pre-approved boundaries

**Roadmap Implication:** Future releases (2.0+) can progressively grant decision autonomy for low-risk scenarios (e.g., auto-approve projects scoring above a threshold with all criteria met).

---

## Entry 2 (Superseded — see Entry 2 REVISED below)

**Decision ID:** DEC-002
**Topic:** Agent Architecture & Coordination
**Status:** Superseded by Entry 2 (REVISED)

**Decision Made (original):**
Option C — Specialized Meta-Agent + Phase Agents (with bounded orchestration, permitting phase-skipping for defined "tier" scenarios: New Product / New Release / New Feature)

This version allowed phase skipping under specific documented scenarios and framed exception paths as available but non-liberal. It was corrected immediately after logging — see the revised entry — once it was clarified that the Portfolio Management Agents system (unlike the separate Software Development Workflow system) must be strictly linear with no phase skipping or exception paths at all. Kept here for traceability only; **do not implement against this version.**

---

## Entry 2 (REVISED)

**Decision ID:** DEC-002
**Topic:** Agent Architecture & Coordination
**Status:** Approved (Release 1.0)

**Decision Made:**
Option C — Specialized Meta-Agent + Phase Agents (strictly linear process)

**Options Considered:**
- Option A: Independent Agents, Sequential Flow
- Option B: Coordinated Agent System with Shared Context
- **Option C: Specialized Meta-Agent + Phase Agents** → CHOSEN
- Option D: Single Unified Agent with Phase-Specific Modes
- Option E: Custom approach

**Rationale:**
A meta-agent orchestrator provides intelligent coordination and context management while maintaining strict adherence to a linear process flow.

**Guardrails & Constraints:**

1. **Process Flow: STRICTLY LINEAR**
   - Fixed sequence: Idea → Definition → Design → Realization → Go-Live → Closure
   - NO phase skipping under any circumstances
   - NO exception paths — all projects follow the same sequence

2. **Looping Back (Revisit Earlier Phases): FACILITATED**
   - When new insights emerge during later phases, the orchestrator can request earlier-phase reconsideration
   - Example: Design phase identifies an issue; can route back to Definition for clarification
   - This is the only flexibility mechanism in Release 1.0

3. **Escalation to Humans:** when routing/coordination decisions exceed orchestrator logic, escalate to governance (Portfolio Board / Steering Group per [project-lifecycle-flow.md](../prd/project-lifecycle-flow.md))

**Implication for Architecture:**
- The meta-agent is a process manager/coordinator, not a decision-maker
- It enforces linear flow, maintains context, routes backward when needed, and escalates impediments
- Contrast with the separate Software Development Workflow Agents system (product/release/sprint cycle), which *is* permitted phase-skipping, exception paths and non-linear looping — that flexibility model does not apply here

---

## Entry 3

**Decision ID:** DEC-003
**Topic:** Primary End Users & Roles
**Status:** In Development (Release 1.0)

**Decision Made:**
Role structure organized into four tiers, aligned with Didier's portfolio governance framework (`reference/didier-source-materials/Portfolio Management Rolbeschrijvingen.rtf`):

- **Portfolio Board Tier** (strategic): Portfolio Owner, Business Owner/Division Head, CFO, Portfolio Manager (optional)
- **Steering Group Tier** (project execution oversight): Project Sponsor (Opdrachtgever), Senior User, Senior Supplier
- **Execution Tier** (day-to-day delivery): Project Manager, Project Team/SME
- **Supporting Roles**: Financial/Resource Manager, Organizational Administrator

Full role descriptions (who they are, when they interact, what they need from the system) are documented in [`roles-and-personas.md`](./roles-and-personas.md).

**Rationale:**
- Portfolio Board composition reflects Didier's model: Portfolio Owner (executive sponsor), Business Owners (divisional representation), CFO (financial governance)
- Steering Group structure follows Didier's standard PRINCE2-style model: Opdrachtgever, Senior User, Senior Supplier
- The three governance tiers (Portfolio Board → Steering Group → Execution) preserve clear accountability and decision authority at each level
- Role descriptions define functional needs, not job titles — organizations of any size can combine or split roles as needed
- Client-specific examples (e.g. Feyenoord) from Didier's source material were generalized/removed from our documentation

**Status:** Role structure is defined; open questions on advisor-vs-user role separation, access/permission model, and role-specific dashboards remain tracked in `roles-and-personas.md` under "Questions for Refinement."

---

## Entry 4

**Decision ID:** DEC-004
**Topic:** Execution Template Alignment with Didier's Framework
**Status:** Approved (Release 1.0)

**Decision Made:**
Align all execution templates with the structure and content of the templates Didier provided (`reference/didier-source-materials/templates/`), while:
- Keeping Markdown format (not Word/PowerPoint)
- Keeping English language only
- Keeping checkbox/checklist/fill-in-the-blank structure
- Making every template role-aware (explicit "Primary Roles" designation)
- Creating new Markdown versions of Didier's templates that we didn't previously have

**Options Considered:**
- Keep our original generic templates unchanged — Denied
- Adopt Didier's templates as-is in Word/PowerPoint format — Denied (format/language requirements)
- **Align content/structure with Didier's templates, rebuild in Markdown, English, role-aware — CHOSEN**

**Rationale:**
Didier's templates reflect real, field-tested governance documents already in use. Aligning our system's templates to that structure means the tool produces artifacts that plug directly into an organization's existing governance process rather than introducing a parallel, incompatible format. Markdown was retained (over replicating Word/PowerPoint) because it is the native format for agent-generated output and version control.

**Result:** `templates/execution-templates.md` contains 9 primary templates + 2 supporting templates, each mapped to a lifecycle phase and to the primary role(s) who use it. New templates created to cover gaps versus Didier's set: Project Brief, Project Initiation Document (PID), Project Start Architecture, Go/No-Go Decision, Change Request.

**Note:** All references to the Feyenoord client example present in Didier's source material were removed from our derived documentation, per explicit instruction.

---

## Open Items Carried Forward

These are not yet decided and should be resolved before or during early development:

1. Advisor roles vs. end-user roles — do the six portfolio advisor roles (Project Idea Advisor, Project Brief Advisor, PID Advisor, PSA Advisor, Project Closure Advisor, Project Prioritization Advisor — see `agent-specifications.md`) need distinct system representation from the human end-user roles in `roles-and-personas.md`?
2. External stakeholders (clients, vendors, regulatory bodies) — in scope for Release 1.0 or deferred?
3. Portfolio Manager role necessity — when is this a dedicated position vs. folded into Portfolio Owner/PMO?
4. Role-based access/permission model — not yet specified.
5. Integration points with external systems (HR, Finance, PM tooling) — not yet specified.
6. Relationship/integration touchpoints with the separate Software Development Workflow Agents system (different cadence: portfolio cycle vs. product/release/sprint/day cycle) — acknowledged as a gap, deferred.
