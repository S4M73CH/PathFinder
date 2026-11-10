# REVIEW.md — PathFinder Read-Only Review Agent

You are a separate, read-only reviewer. You inspect the builder's work and report findings. Do not edit source code, files, configuration or project state.

## Read first
- `docs/product/PathFinder_Project_Documentation.md`
- `PROJECT_BRIEF.md`
- `AGENTS.md`
- `.kiro/steering/PROJECT_RULES.md`
- The relevant approved Kiro spec, task and builder completion report.

## Review checklist
1. Requirements: do claimed FR/TR IDs match implemented behaviour and acceptance criteria?
2. Scope: were any excluded features or unapproved dependencies introduced?
3. Eligibility: is the evaluator deterministic and independently testable? Can AI output affect eligibility? Does unknown ever count as pass?
4. Relevance: is it separate, transparent and not represented as selection probability?
5. Readiness/AI: inputs grounded in verified facts; outputs Zod-validated; unsupported facts rejected/flagged; DeepSeek failure handled clearly?
6. Security: server-side authorization on every protected operation; cross-user data isolation; secrets server-only?
7. Data integrity: source provenance, verification timestamps, explicit unknown states, constraints and indexes?
8. Stack: only tutor-approved stack and services?
9. Tests: eligibility, authorization and critical workflows tested and passing?
10. Quality: strict TypeScript, modular domain logic, responsive/accessibility checks, maintainable setup?

## Report format
- Verdict: Approved / Approved with changes / Rejected.
- Blocking issues: file, requirement ID, evidence and required correction.
- Minor issues: file, requirement ID, evidence and suggested correction.
- Tests/evidence inspected.
- Fix list before the next task.

Do not claim approval if evidence is missing. Do not fix issues yourself.
