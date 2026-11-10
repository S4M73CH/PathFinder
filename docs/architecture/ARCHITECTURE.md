# Architecture — PathFinder AI

## Architectural style
A modular monolith: one Next.js application, one codebase and one initial Vercel deployment. Feature modules own domain logic and communicate through typed interfaces. No microservices or separate worker in the MVP.

## Runtime components
1. Browser — public catalogue and authenticated user/admin interfaces.
2. Next.js App Router — pages, server actions/route handlers where needed, server-side session and authorization checks.
3. Feature modules — identity, profiles, opportunities, eligibility, matching, readiness, applications and verification/admin.
4. Supabase PostgreSQL — primary relational store.
5. Supabase Auth — identity and session management.
6. Internal AI module — one boundary around Vercel AI SDK and `@ai-sdk/deepseek`.
7. DeepSeek — `deepseek-v4-flash` non-thinking mode.

## Module responsibilities
| Module | Responsibility |
|---|---|
| Identity | Supabase Auth, session and account integration |
| Profiles | Education, nationality, residence, skills, experience and goals |
| Opportunities | Catalogue, detail, category, location, funding and search |
| Eligibility | Deterministic criterion evaluation and outcome |
| Matching | Separate relevance score and explainable factors |
| Readiness | Grounded AI explanations and readiness plans |
| Applications | Saved opportunities and application progress |
| Verification/Admin | Source evidence, review, publishing, lifecycle and audit |

## Request flows
### Public discovery
Browser → Next.js route/page → Opportunities module → PostgreSQL → public response.

### Personal eligibility
Authenticated browser → server session check → ownership authorization → Profiles + Opportunities → Eligibility module → deterministic result → response.

### AI readiness
Authenticated request → authorization → computed eligibility/relevance and minimum relevant profile facts → Readiness module → internal AI module → Vercel AI SDK → DeepSeek → Zod validation → response. AI output never changes eligibility.

### Admin publishing
Admin request → server-side admin authorization → Verification/Admin module → source and lifecycle checks → PostgreSQL → published catalogue.

## Security boundaries
- Server-side authorization on every protected read/write.
- User-owned profile, assessment, saved and application records cannot be accessed by another user.
- Admin rights are checked server-side, not inferred from hidden controls.
- Provider keys and service credentials are server-only.
- AI receives only the minimum profile data and verified opportunity facts needed for the task.
- Validate all API input and structured AI output with Zod.

## Resilience
DeepSeek outage must not disable public catalogue browsing or deterministic eligibility. AI-dependent actions return a clear failure state, with no invented answer.

## Exclusions
No crawler, microservices, worker, queue, Redis, vector database, pgvector, advanced RAG, CV/document ingestion, automated applications, reminders, employer dashboards, university integrations or extra AI providers.
