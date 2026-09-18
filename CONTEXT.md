# Glossary — Portfolio Management Agents

Project jargon → meaning. Separate from `ARCHITECTURE.md`: that's about
structural decisions, this is about language. Optional and living — update
it as a new term arises or an existing one changes meaning, don't try to
make it complete in one go.

| Term | Meaning |
|---|---|
| PID | Project Initiation Document — the artifact assessed at the Design phase gate (F4). Not to be confused with a process ID; this is governance terminology from Didier's field framework. |
| PSA | Project Start Architecture — an optional architecture-quality document reviewed alongside the PID at the Design phase gate (F5), assessed across eight architecture areas. |
| Portfolio Board | The governance tier that decides at the Idea, Definition, Design, and Closure gates. Functional role, not a fixed job title (DEC-003) — a small org may combine it with other roles. |
| Steering Group | The governance tier that decides at the Realization (status/escalation) and Go-Live gates. Functional role, not a fixed job title (DEC-003). |
| Go/No-Go | The human decision at a governance gate to proceed to the next phase, loop back to an earlier one, or stop. Always a human action in Release 1.0 (DEC-001) — no agent has this authority. |
| Governance gate | The decision point at the end of each of the six lifecycle phases (Idea → Definition → Design → Realization → Go-Live → Closure) where a Go/No-Go is made. |
| DEC-XXX | A decision entry's ID in `docs/decisions/DECISION-LOG.md`, e.g. `DEC-001`. "REVISED" after the ID (e.g. `DEC-002 REVISED`) marks a superseding entry — see Entry 2 for the pattern; the original stays in the log for traceability, never deleted. |
| Advisor agent | One of the six specialized agents (F1–F6) that assesses project documentation at a governance gate and issues a recommendation. Never decides — "advisor" is deliberate, distinguishing it from a decision-maker. |
| Meta-agent orchestrator | The single coordinator (F7) that enforces the linear phase sequence and facilitates backward loops. A process coordinator, not a decision-maker — don't read "orchestrator" as implying autonomy over Go/No-Go. |
| F-number | A functionality item's identifier in `PRD.md` (e.g. `F1`), used in a `Covers:` field to link a test scenario or GitHub issue back to the requirement it realizes. |
