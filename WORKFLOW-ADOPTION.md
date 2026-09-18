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
| spec-observability | yes | 2026-09-18 | Substantiated in `PRD.md` as not yet applicable — no runtime exists. Revisit once an implementation choice is made. |
| spec-deployability | yes | 2026-09-18 | Substantiated in `PRD.md` as not yet applicable — no environments exist yet. |
| spec-privacy | yes | 2026-09-18 | Substantiated in `PRD.md` — project documents processed may name individuals in a business context; no special-category personal data anticipated, but needs a real answer once storage is chosen. |
| spec-backup-recovery | yes | 2026-09-18 | Substantiated in `PRD.md` as not yet applicable — no data store exists. |
| spec-maintainability | yes | 2026-09-18 | Substantiated in `PRD.md` — the six-agent, phase-bound separation (DEC-002 REVISED) is itself the maintainability argument: each agent and each template is an independently understandable unit. |
| spec-testability | yes | 2026-09-18 | Substantiated in `PRD.md` — each agent's fixed step-by-step process and execution format is written in a form that translates directly to test scenarios. |
| spec-documentation | yes | 2026-09-18 | Substantiated in `PRD.md` — the doc set (`docs/prd/PRD.md`, `DECISION-LOG.md`, `agent-specifications.md`, `project-lifecycle-flow.md`, `roles-and-personas.md`, `execution-templates.md`) plus this `PRD.md` traceability layer is the current source of truth, kept current per the "Updating the Decision Log" convention in `README.md`. |
