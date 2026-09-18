# Adoption of shared workflow changes

Per change from `CHANGES.md` in [spec-driven-guardrails](https://github.com/TiesL/spec-driven-guardrails)
whether this project applies it. No row means: not (yet) applicable —
the question shows up on its own once that changes.

| Change | Answer | Date | Notes |
|---|---|---|---|
| traceability-link-1 | yes | 2026-09-18 | Six agents (F1–F6) each have a fixed, independently testable evaluation process already specified in `docs/prd/agent-specifications.md` — F-number → scenario traceability is straightforward to enforce once test authoring starts. |
| process-prd | yes | 2026-09-18 | This is a spec-first repo; `PRD.md` is the whole point of the current phase. Already substantiated in `PRD.md` itself. |
| architecture-document | yes | 2026-09-18 | Applies once the first structural decision (agent runtime, orchestration mechanism, template storage) is made — not yet, per `PRD.md`'s Architecture section. `ARCHITECTURE.md` scaffold kept ready for that. |
| test-unit | yes | 2026-09-18 | Each agent's step-by-step evaluation logic (scoring, classification, format rules) is deterministic enough to unit-test once implemented. |
| test-feature-gwt | yes | 2026-09-18 | Each agent's "Execution Format" and phase-gate behavior is a natural Given/When/Then feature: given a submitted document, when assessed, then a specific recommendation/classification. |
| test-tdd-seams | yes | 2026-09-18 | No implementation exists yet, so no seams are agreed yet — applies once implementation planning identifies them. |
| quality-review-before-merge | yes | 2026-09-18 | Standard practice; no reason for this project to deviate once PRs start landing. |
| ci-gate-on-merge | yes | 2026-09-18 | Standard practice; applies once a `check` command exists to gate on. |
| stray-closes-guard | yes | 2026-09-18 | Standard practice; every work item will be filed as a GitHub issue per `write-spec`. |
| process-technical-debt-register | yes | 2026-09-18 | `PRD.md`'s Technical debt table already has one entry (the dual-PRD situation) — the register is in active use from day one. |
| process-refactoring-triggers | yes | 2026-09-18 | Standard practice; the six independent agents (DEC-002 REVISED) give a clear place to notice when a "process coordinator, not decision-maker" boundary is being violated. |
| process-diagnose-bug | yes | 2026-09-18 | Applies once there's running code to have bugs in; not yet, but no reason to opt out later. |
| process-model-choice | yes | 2026-09-18 | Relevant from the start: this is an agent-based system, so model/reasoning-effort choice per stage (per `model-choice` skill) is core, not incidental. |
| spec-security | yes | 2026-09-18 | Substantiated in `PRD.md` — Non-Goals: RBAC/permissions explicitly deferred (open item), must be answered before any agent handles real project/financial documents. |
| spec-data-integrity | yes | 2026-09-18 | Substantiated in `PRD.md` — the one fixed invariant so far (agents never overwrite a human decision, DEC-001; Decision Log is append-only) predates any data store. |
| spec-failure-modes | yes | 2026-09-18 | Substantiated in `PRD.md` — every advisor agent's spec already defines explicit "don't invent data, name what's missing" behavior; escalation-not-silent-failure is part of the orchestrator's spec (F7). |
| spec-observability | no | 2026-09-19 | No runtime exists to observe — nothing to substantiate `yes` against. Trigger to revisit: once an implementation/runtime choice is made. (Was incorrectly `yes` since 2026-09-18; corrected per pre-merge review on PR #7, same anti-pattern as `test-integration`.) |
| spec-deployability | no | 2026-09-19 | No environments exist yet. Trigger to revisit: once an implementation/deployment choice is made. (Was incorrectly `yes` since 2026-09-18; corrected per pre-merge review on PR #7.) |
| spec-privacy | yes | 2026-09-18 | Substantiated in `PRD.md` — project documents processed may name individuals in a business context; no special-category personal data anticipated, but needs a real answer once storage is chosen. |
| spec-backup-recovery | no | 2026-09-19 | No data store exists. Trigger to revisit: once a data store is chosen. (Was incorrectly `yes` since 2026-09-18; corrected per pre-merge review on PR #7.) |
| spec-maintainability | yes | 2026-09-18 | Substantiated in `PRD.md` — the six-agent, phase-bound separation (DEC-002 REVISED) is itself the maintainability argument: each agent and each template is an independently understandable unit. |
| spec-testability | yes | 2026-09-18 | Substantiated in `PRD.md` — each agent's fixed step-by-step process and execution format is written in a form that translates directly to test scenarios. |
| spec-documentation | yes | 2026-09-18 | Substantiated in `PRD.md` — the doc set (`docs/prd/PRD.md`, `DECISION-LOG.md`, `agent-specifications.md`, `project-lifecycle-flow.md`, `roles-and-personas.md`, `execution-templates.md`) plus this `PRD.md` traceability layer is the current source of truth, kept current per the "Updating the Decision Log" convention in `README.md`. |
| process-context-document | yes | 2026-09-19 | Domain has real jargon (PID, PSA, DEC-XXX, Portfolio Board vs. Steering Group, governance tiers) not self-evident to a newcomer; cheap to grow incrementally rather than complete upfront. Confirmed with Ties. |
| process-issue-tracking | yes | 2026-09-19 | Already practiced (issue-per-change, PR-per-issue) but issues #1/#3/#5 didn't follow the required Epic/Work-item structure (AC<n> Given/When/Then, `Covers:` field) — this answer commits to fixing that starting with #5, not retrofitting past issues. Confirmed with Ties. |
| test-integration | no | 2026-09-19 | No code and no external dependency exists yet to integration-test. Trigger to revisit: once an implementation choice introduces a real external dependency (e.g. an LLM API call, a document/data store). Confirmed with Ties. |
| spec-performance-scale | no | 2026-09-19 | Not yet tested against a real deployment — no substantiation exists to answer `yes` against. Trigger to revisit: once a real deployment exists. (Corrected during PR #7 review — same "applies, but not yet" anti-pattern as `test-integration`; caught before merge, not a later fix.) |
| spec-compliance | yes | 2026-09-19 | Substantiated in `PRD.md` — DEC-001 (human Go/No-Go) plus an intended audit trail is process-level substantiation; no legal/regulatory retention obligation identified yet, left to adopting organizations. Confirmed with Ties. |
| spec-portability | no | 2026-09-19 | No platform choice has been made — nothing to substantiate `yes` against. Trigger to revisit: once a platform choice is made. (Corrected during PR #7 review — same anti-pattern.) |
| spec-usability | yes | 2026-09-19 | Substantiated in `PRD.md` — outputs are specified to be role-aware, decision-focused, and length-capped so a Board/Steering Group member can act without extra interpretation; matches `agent-specifications.md`. Confirmed with Ties. |
| spec-cost-management | no | 2026-09-19 | No runtime or API usage exists yet — nothing to substantiate `yes` against. Trigger to revisit: once a runtime/API choice is made. (Corrected during PR #7 review — same anti-pattern.) |
