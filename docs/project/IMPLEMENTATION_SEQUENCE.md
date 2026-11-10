# Implementation Sequence

This sequence follows tutor V3's build order. Kiro must reconcile it with the actual repository and approved specifications; it is not permission to begin implementation.

1. Day-one compatibility checks: latest stable compatible versions; verify DeepSeek structured-output support with installed `ai` and `@ai-sdk/deepseek`.
2. Project foundation: Next.js, TypeScript strict mode, Tailwind, shadcn/ui, lint/test tooling, environment example and lockfile.
3. Propose normalized database schema and migration strategy; stop for Joshua and Samuel approval.
4. Supabase Auth, protected routes and server-side authorization.
5. Profile onboarding and editing.
6. Admin opportunity management and verification.
7. Public catalogue, search, filters and detail pages.
8. Deterministic eligibility engine and unit tests.
9. Relevance ranking and explainable factors.
10. DeepSeek explanations and readiness plans with Zod validation.
11. Saved opportunities and application tracking.
12. Responsive/accessibility polish, security review and release preparation.
13. FR-24 inaccurate/expired opportunity reporting only if time allows.

If time is constrained, simplify AI readiness first. Do not cut deterministic eligibility, authorization or source verification.
