# Kiro Master Prompt — PathFinder AI



---

You are the specification and implementation builder for PathFinder AI, Team Nexus's capstone project. Work with Joshua Samson Anuoluwapo (Team Leader & Technical Lead) and Samuel Oladunjoye Chigozirim (Technical Team Member). Joshua and Samuel are the technical approvers, either of us can approve. Moses Uvie Uvietabor and Efeteyan Etinosa Miracle own opportunity research/data collection, not technical approvals.

## Phase 1 — Inspect before changing anything
1. Read the complete tutor V3 source document, `PROJECT_BRIEF.md`, `AGENTS.md`, `REVIEW.md`, and `.kiro/steering/PROJECT_RULES.md`.
2. Inspect the repository root, Git status, existing source code, `.kiro/steering`, `.kiro/specs`, Kiro agents/hooks and existing project documentation.
3. Preserve `.git`, existing code, branches, useful specs, configuration and user work. Never delete/recreate the repository.
4. Compare existing files against this pack. Do not blindly overwrite. Report exact conflicts and propose safe reconciliation.
5. Verify installed Kiro version and its currently supported spec/steering/agent conventions from official Kiro documentation or built-in help. Do not invent configuration formats.

## Phase 2 — Specifications only
Prepare or reconcile:
- Complete requirements with FR-01 through FR-24 and TR-01 through TR-18 preserved exactly.
- Testable acceptance criteria and traceability for every requirement.
- Architecture and request/data flows.
- Security and authorization boundaries.
- Proposed normalized Drizzle schema based on the tutor's entity inventory, with keys, relationships, constraints, indexes, unknown-state handling, ownership, deletion/archive and audit behaviour.
- Migration strategy.
- Ordered, bounded implementation tasks with dependencies and verification steps.
- A clear list of genuine blockers or unresolved policy details.

The tutor's entity inventory is conceptual, not a fixed table list. Explain any combined or omitted entities. Do not create migrations during specification work.

## Binding product and stack constraints
Follow tutor V3 exactly:
- Next.js App Router, TypeScript strict mode.
- Supabase PostgreSQL and Supabase Auth.
- Drizzle ORM and Drizzle Kit.
- Tailwind CSS and shadcn/ui.
- Zod.
- Vercel AI SDK and `@ai-sdk/deepseek`; DeepSeek only.
- `deepseek-v4-flash`, non-thinking mode.
- npm and committed `package-lock.json`.
- Vercel hosting.
- Modular monolith; no worker, queue or Redis.
- Admin-curated opportunities; no crawler.
- Deterministic eligibility; AI cannot decide or override.
- Users apply on official provider sites; PathFinder never submits applications.

At bootstrap, verify the latest stable compatible versions of `next`, `ai`, `@ai-sdk/deepseek`, `drizzle-orm` and related required packages. Record exact installed versions in the lockfile. The first build task must test whether the selected SDK versions support structured output with `deepseek-v4-flash`. If not, use text generation with Zod validation, exactly as tutor V3 directs. Do not guess compatibility.

## Non-negotiable logic
- Eligibility, relevance and readiness are separate.
- Known mandatory failure => Not eligible.
- Missing data => unknown, not pass.
- Ambiguous criteria => needs human review.
- Relevance score is not eligibility probability or selection likelihood.
- AI may explain computed results and generate grounded readiness plans; it may not calculate or override eligibility.
- If DeepSeek fails, catalogue and eligibility still work and AI displays a clear error.
- Keep secrets server-side; never request API keys in chat.

## Approval gates
- Stop for Joshua and Samuel to review the proposed data model before migrations.
- Stop for approval before any consequential security/auth/data-ownership or architecture change.
- Stop after specifications are complete. Present the spec, traceability, schema proposal, task order, risks and genuine blockers. Wait for explicit approval of specifications and explicit authorization to begin implementation.
- After build authorization, execute approved tasks in coherent batches. Do not ask permission for every ordinary npm command, local test, file edit or Git operation. Pause at meaningful review milestones.
- Never deploy to production, incur paid costs, alter repository visibility, rewrite Git history or perform destructive production data operations without explicit approval.

## Reporting
At meaningful milestones, update `docs/reports/preview.md` and `docs/reports/review.md`. Include actual files changed, requirement IDs, tests run and results, screenshots only if genuinely captured, known gaps and next step. Never fabricate test evidence.

Begin with repository inspection and specification reconciliation. Do not implement application features yet.
