# CLAUDE.md

Guidance for Claude Code (or any agent) working in this repository.

## What this repo is, right now

This is a **specification repository**, not a codebase. There is no application code yet. The `docs/`, `templates/`, and `reference/` directories are the complete product brief for a system that has not been built. Do not assume any implementation details beyond what these documents state.

## Recommended first step

Start in **Plan Mode**. Read, in this order:

1. `docs/prd/PRD.md`
2. `docs/decisions/DECISION-LOG.md`
3. `docs/decisions/roles-and-personas.md`
4. `docs/prd/agent-specifications.md`
5. `docs/prd/project-lifecycle-flow.md`
6. `templates/execution-templates.md`

Then propose an implementation plan (tech stack, architecture, milestones) rather than writing code immediately — the human owner (Ties) wants to review scoping before development starts.

## Hard constraints — do not design around these, ask first if you think one should change

- The governance flow is **strictly linear**: Idea → Definition → Design → Realization → Go-Live → Closure. No phase-skipping, no exception/fast-track paths. The only permitted flexibility is looping back to a prior phase when new information emerges (DEC-002 REVISED in the Decision Log).
- Agents **assess and recommend**; they do not decide. Every Go/No-Go remains a human action in Release 1.0 (DEC-001).
- The meta-agent orchestrator is a **process coordinator**, not a decision-maker — it enforces sequence, maintains cross-phase context, and escalates impediments to humans it cannot resolve.
- Role definitions in `roles-and-personas.md` are **functional**, not literal job titles — the system must not hard-code assumptions that only fit large enterprises (e.g. don't assume every tier maps to a distinct person).
- All generated documents/templates: **English language, Markdown format, checkbox/fill-in-the-blank structure, role-aware** (each template states its primary role(s) and phase).
- Never introduce or reference the client examples (e.g. Feyenoord) present in the original Dutch source material under `reference/didier-source-materials/` — those are historical field examples, not part of this product's identity.

## Updating the Decision Log

If a design or scoping decision is made while working in this repo — including ones you propose and the human approves — add a new dated entry to `docs/decisions/DECISION-LOG.md` rather than editing history. If a decision supersedes an earlier one, mark the earlier entry "Superseded by Entry N" (see Entry 2 for the pattern) rather than deleting it.

## What NOT to touch

- `reference/didier-source-materials/` is read-only reference material (original field documents from co-founder Didier, in Dutch, Word/PowerPoint format). If a template needs to evolve, change `templates/execution-templates.md` and record why in the Decision Log — don't edit the source files.
