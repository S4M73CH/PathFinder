# Development Workflow

## Stage 1 — Repository inspection
Inspect Git status, source files, current Kiro specs/steering/agents and project documentation. Preserve useful work. Report conflicts before changing them.

## Stage 2 — Specification reconciliation
Prepare complete requirements, architecture, data model proposal and ordered tasks. Preserve all FR/TR IDs. No implementation.

## Stage 3 — Review gate
Joshua and Samuel review:
- Requirements and acceptance criteria.
- Architecture and security boundaries.
- Database schema proposal and migration strategy.
- First bounded implementation task.
Kiro stops and waits for explicit approval of specifications and explicit authorization to build.

## Stage 4 — Build
After authorization, implement approved tasks in small coherent batches. Run relevant tests and update reports. Ordinary local development actions do not need repetitive permission prompts.

## Stage 5 — Review and correction
The read-only reviewer checks work against source documents and reports Approved / Approved with changes / Rejected. Builder makes corrections; reviewer does not edit.

## Stage 6 — Handover
Provide setup instructions, environment variable names, tests and results, known limitations, demo steps and deployment status. Production deployment requires separate explicit approval.

## Completion report
- Task and FR/TR identifiers.
- Files created/changed.
- Behaviour implemented.
- Tests actually run and exact results.
- Known gaps/blockers.
- Next bounded task.
