# Product Requirements Document — Portfolio Management Agents

**Status:** Draft / Release 1.0 specification
**Part of:** the Decision Velocity proposition (Ties & Didier). This system covers the *portfolio* cycle — the sibling system, Software Development Workflow Agents, covers the product/release/sprint/day cycle. Integration between the two is an acknowledged, deferred gap (see [Decision Log — Open Items](../decisions/DECISION-LOG.md#open-items-carried-forward)).

---

## 1. Problem Statement

Organizations running project portfolios need consistent, decision-ready information at each governance gate (Idea, Definition, Design, Realization, Go-Live, Closure) — but producing and reviewing that information (project briefs, PIDs, status reports, closure reports) is manual, inconsistent in quality, and slow to get in front of the Portfolio Board or Steering Group. Portfolio Management Agents assess submitted project documentation against a fixed template and process, and give the human decision-makers a clear, evidence-based recommendation — without taking the Go/No-Go decision away from them.

## 2. Goals

- Give every project a consistent, criteria-based assessment at each governance gate, regardless of who wrote the submission or who reviews it.
- Preserve human decision authority at every gate (see [DEC-001](../decisions/DECISION-LOG.md#entry-1)).
- Enforce a strictly linear governance process with no phase-skipping and no exception paths, with backward looping as the only flexibility mechanism (see [DEC-002 REVISED](../decisions/DECISION-LOG.md#entry-2-revised)).
- Produce templates and assessments that plug into an organization's existing governance documents rather than replacing them (see [DEC-004](../decisions/DECISION-LOG.md#entry-4), aligned to Didier's field-tested framework).
- Support organizations of any size and industry — role descriptions are functional, not fixed job titles (see [DEC-003](../decisions/DECISION-LOG.md#entry-3)).

## 3. Non-Goals (Release 1.0)

- Autonomous Go/No-Go decision-making by agents (deferred to a 2.0+ roadmap, see DEC-001).
- Phase-skipping or exception-path routing (explicitly excluded — this is what differentiates this system from the Software Development Workflow Agents system).
- Role-based access control / permissions model (open item, not yet specified).
- Integrations with external HR/Finance/PM systems (open item, not yet specified).

## 4. System Overview

### 4.1 Governance Model

Three governance tiers, six sequential lifecycle phases. Full detail in [`project-lifecycle-flow.md`](./project-lifecycle-flow.md).

| Phase | Governance Gate | Decision Maker |
|---|---|---|
| Idea | Project Idea Approval | Portfolio Board |
| Definition | Project Brief / Concept Approval | Portfolio Board |
| Design | PID Approval (+ optional PSA review) | Portfolio Board |
| Realization | Status Reporting & Escalation Management | Steering Group |
| Go-Live | Go-Live Approval | Steering Group |
| Closure | Project Documentation & Closure Approval | Portfolio Board |

### 4.2 Agent Roster

Six specialized advisor agents, each bound to a phase, each producing an assessment (never a decision). Full specifications in [`agent-specifications.md`](./agent-specifications.md).

1. Project Prioritization Advisor
2. Project Idea Advisor
3. Project Brief Advisor
4. PID Advisor
5. PSA Advisor
6. Project Closure Advisor

Coordination model: a meta-agent orchestrator enforces the linear sequence, maintains context across phases, and facilitates backward loops — it does not make decisions (DEC-002 REVISED).

### 4.3 Human Roles

Eleven roles across four tiers (Portfolio Board, Steering Group, Execution, Supporting). Full detail in [`../decisions/roles-and-personas.md`](../decisions/roles-and-personas.md).

### 4.4 Templates

Nine primary + two supporting Markdown templates, role-aware and phase-mapped, aligned to Didier's field templates. See [`../../templates/execution-templates.md`](../../templates/execution-templates.md).

## 5. Key Decisions

See [`DECISION-LOG.md`](../decisions/DECISION-LOG.md) for full rationale and options considered on: agent decision authority, agent architecture/coordination, end-user roles, and template alignment.

## 6. Open Questions

Tracked in full in the Decision Log's "Open Items Carried Forward" section. Headline items: advisor-role vs. end-user-role system representation, external stakeholder scope, Portfolio Manager role necessity, access/permission model, external system integrations, and the portfolio↔development-workflow integration gap.

## 7. Source Materials

This PRD's roles and templates were aligned against original field documents from Didier (Dutch-language RTF, DOCX, PPTX). Those source files are deliberately not part of this repository — not needed going forward, and not appropriate to publish. Ground truth for structure now lives in [`agent-specifications.md`](./agent-specifications.md), [`roles-and-personas.md`](../decisions/roles-and-personas.md), and [`../../templates/execution-templates.md`](../../templates/execution-templates.md).
