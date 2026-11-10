# AGENTS.md — PathFinder AI Agent Instructions

These instructions govern builder and supporting agents in the existing PathFinder repository. They operationalize the tutor's V3 source; they do not replace it.

## 1. Read order and source of truth
Before editing, read:
1. `docs/product/PathFinder_Project_Documentation.md` (tutor V3 working copy; original PDF is alongside it).
2. `PROJECT_BRIEF.md`.
3. `docs/project/DECISION_REGISTER.md`.
4. `.kiro/steering/PROJECT_RULES.md`.
5. `REVIEW.md` and current Kiro specifications.

The tutor's V3 document defines product scope, final technical decisions, entity inventory, FR-01–FR-24 and TR-01–TR-18. Preserve all requirement IDs and exact requirement wording. Do not silently alter the product.

## 2. Binding stack and architecture
- Modular monolith: one codebase, one deployment, feature modules.
- TypeScript strict mode; Next.js App Router.
- PostgreSQL hosted on Supabase; Supabase Auth.
- Drizzle ORM and Drizzle Kit migrations.
- Tailwind CSS with shadcn/ui.
- Zod for runtime validation.
- DeepSeek only through Vercel AI SDK and `@ai-sdk/deepseek`.
- Model: `deepseek-v4-flash`, non-thinking mode.
- npm; commit `package-lock.json`.
- Vercel hosting.
- No background worker, queue or Redis in MVP.

Do not add another framework, database, ORM, auth provider, AI provider, queue, vector database or service.

## 3. Product invariants
- Eligibility is deterministic application logic for structured criteria. AI never decides, calculates, certifies or overrides it.
- Eligibility, relevance and readiness are separate operations.
- Relevance is not eligibility probability and does not predict selection.
- A known mandatory failure means Not eligible.
- Missing information is unknown, never a pass.
- Ambiguous criteria stay flagged for human review.
- Use official opportunity sources and preserve provenance and verification timestamps.
- Do not infer Nigerian eligibility, funding, deadlines or open status.
- Users apply through official provider channels. PathFinder never submits applications.
- If DeepSeek fails, catalogue and eligibility remain usable; show a clear AI error, never a fabricated fallback.

## 4. Security and privacy
- Enforce authorization on the server for every protected operation.
- User profile, assessment, saved-opportunity and application data are private to the owner and authorized administrators.
- Keep all secrets and provider keys server-side. Never expose them in client bundles or commit them.
- Validate inputs and AI outputs with Zod.
- Use least privilege and test cross-user access denial.

## 5. Scope control
Do not implement excluded features: broad crawling, CV/document upload or parsing, automated applications, reminders, CV/cover-letter generation, interview coaching, employer dashboards, university integrations, multi-agent orchestration, advanced RAG/vector search, microservices, workers, Redis or queues.

FR-24 (report an inaccurate/expired opportunity) is explicitly lowest priority and only to be built if time allows.

## 6. Working method
- Inspect the existing repository and `.kiro` state before editing. Preserve useful code, specs, settings, branches and Git history.
- Do not blindly overwrite existing files. Compare and reconcile.
- Use small, coherent, verifiable tasks. Trace each task to FR/TR identifiers and acceptance criteria.
- Keep domain logic in feature modules, not page components.
- Write and run relevant tests, especially eligibility and authorization tests.
- Update documentation and decision records when an approved decision changes.
- Maintain `docs/reports/preview.md` and `docs/reports/review.md` at meaningful milestones. Only report actual behaviour, screenshots and test evidence.
- The review agent is read-only and must not change code.
- Report blockers and genuine ambiguities clearly. Do not invent answers.

## 7. Approval gates
Stop for Joshua and Samuel's approval before:
- Database schema acceptance and any migration.
- A consequential change to authentication, authorization or data ownership.
- Any material architecture, product scope or technology change.
- Any production deployment or production data operation.
- Any paid service, subscription or non-trivial spend.
- Destructive actions, force-push/history rewrite, repository visibility/access changes, or secret exposure.

Routine local work (reading, editing ordinary project files, npm commands, local servers, lint, typecheck, tests, local browser checks, Git status/diff/branch/add/commit/push to the configured repository) does not need repeated permission prompts once the owner has authorized the build. Follow Kiro/OS security controls; this file cannot override them.

## 8. Permission transparency
If an action is blocked by a permission prompt, explain: what is requested, why, exact action, affected files/resources, whether read/write, risks, safer narrower alternative and what happens if declined. Group related requests; do not interrupt for routine commands unnecessarily.

## 9. Communication
The project owner is learning. Explain unfamiliar terms briefly, use sequential steps, avoid overwhelming lists, and give exact actionable instructions. Do not pretend a test passed unless it was run.
