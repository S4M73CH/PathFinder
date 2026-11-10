# Project Brief

## Project Title
PathFinder AI: Opportunity Discovery and Career Readiness Platform

## Date
01/11/2026

## Prepared By
Joshua Samson Anuoluwapo, Team Leader, Team Nexus

## 1. Executive Summary
PathFinder AI is an AI-assisted opportunity discovery and career-readiness platform for Nigerian university undergraduates and recent graduates. It helps users discover scholarships, SIWES/industrial training, internships, fellowships, graduate programmes, funded training and leadership opportunities; understand stated eligibility requirements; identify missing information; and prepare using grounded readiness guidance. The MVP combines a curated opportunity catalogue, user profiles, deterministic eligibility checks, separate relevance ranking, AI-assisted explanations, saved opportunities and basic application tracking.

## 2. Background & Context
Opportunities are distributed across many provider websites and channels. Their requirements, deadlines, funding details and nationality restrictions can be difficult to interpret or verify. PathFinder structures this information around official sources, evidence and verification dates. It is an opportunity discovery and recommendation system, not a general-purpose chatbot.

## 3. Objectives
- Build a working MVP for Nigerian undergraduates and recent graduates.
- Provide public browsing, search and filtering of published opportunities.
- Allow users to register and maintain relevant academic and career profile information.
- Compare known profile facts with structured mandatory criteria using deterministic application logic.
- Keep eligibility, relevance and readiness as separate operations.
- Provide grounded AI explanations and readiness plans using DeepSeek.
- Allow users to save opportunities and track basic application progress.
- Allow authorized administrators to curate, verify, publish, close and archive opportunity records.

## 4. Scope

### In Scope
- Public opportunity catalogue, search, filters and detail pages.
- Supabase Auth and profile management.
- Scholarships, SIWES/IT, internships, fellowships, graduate programmes, funded training and leadership opportunities.
- Admin-curated records with official source links, evidence and last-verified timestamps.
- Deterministic eligibility outcomes: Eligible, Likely eligible, Needs review and Not eligible.
- Separate, explainable relevance ranking.
- DeepSeek explanations and readiness plans grounded in verified facts.
- Saved opportunities and basic application tracking.
- User reports of inaccurate or expired listings as the lowest-priority feature, only if time allows.

### Out of Scope
- Automatic crawling or broad scraping.
- Automated application submission.
- CV/document upload or parsing; CV or cover-letter generation.
- Email/WhatsApp reminders or scheduled background workers.
- AI interview coaching.
- Employer dashboards or university integrations.
- Microservices, Redis, queues, vector databases, pgvector, advanced RAG or multiple LLM providers.

## 5. Key Deliverables
| # | Deliverable | Description |
|---|---|---|
| 1 | Approved specifications | Requirements, architecture, data model and implementation tasks |
| 2 | Application foundation | Next.js application, environment configuration, database integration and authentication |
| 3 | Opportunity catalogue | Admin-curated, verified opportunity records and public discovery workflows |
| 4 | Profile and assessment | Profile onboarding, deterministic eligibility and separate relevance |
| 5 | AI readiness assistance | Validated DeepSeek explanations and readiness plans |
| 6 | Tracking | Saved opportunities and basic application progress |
| 7 | Handover | Tests, setup documentation, demo and presentation |

The tutor's V3 delivery plan runs from 1 to 20 November 2026. The project brief does not invent replacement milestone dates.

## 6. Timeline & Milestones
Use the delivery plan in the tutor's V3 source document:
- Planning: 1–9 November.
- Foundation: 10–11 November.
- Core workflows: 11–14 November.
- Eligibility and AI: 14–16 November.
- Tracking and testing: 16–18 November.
- Final documentation and demo: 18–20 November.

The team must report schedule risks early; dates are not evidence that work has been completed.

## 7. Budget
No budget amount is specified in the tutor's V3 technical reference. Prefer free tiers and local development where practical. Obtain explicit approval before paid subscriptions, non-trivial API spend or paid infrastructure.

## 8. Stakeholders & Roles
| Name | Role | Responsibility |
|---|---|---|
| Mr Satar Sarafa | Tutor/Supervisor | Guidance and supervision |
| Joshua Samson Anuoluwapo | Team Leader & Technical Lead | Coordination, technical direction, frontend/user flows, integration, testing, technical reviews and repository delivery |
| Samuel Oladunjoye Chigozirim | Technical Team Member | Works with Joshua on backend, database, Supabase Auth, APIs, eligibility logic, DeepSeek integration and technical reviews |
| Moses Uvie Uvietabor | Opportunity Research & Data Collection | Official-source research, opportunity records, evidence and source/date capture |
| Efeteyan Etinosa Miracle | Opportunity Research & Data Collection | Research, source verification and cross-checking |
| Oluwasola Josiah Temidayo | Documentation Lead | Project documentation and workflow descriptions |
| Shittu Abdulmalik Olasunkanmi | Pitch & Presentation Lead | Pitch, presentation and problem/value explanation |
| Adebayo Isaac | Demo Lead | Demo preparation and plain-language walkthrough |

Joshua and Samuel are the technical approvers. Moses is not assigned technical approval or implementation ownership.

## 9. Risks & Mitigations
| Risk | Mitigation |
|---|---|
| Stale opportunity data | Manual verification, official sources and last-verified timestamps |
| Complex global eligibility | Store applicant nationality, applicant residence and opportunity destination separately |
| Ambiguous criteria | Preserve unknowns and route ambiguous rules for human review |
| Unsupported AI claims | Ground inputs in verified facts and validate output |
| Security/privacy failures | Server-side authorization, ownership checks and server-only secrets |
| Integration complexity | Modular monolith, small verified tasks and review gates |
| Limited time | Prioritize core workflows; FR-24 remains lowest priority |

## 10. Success Criteria
- Visitors can browse, search and filter published opportunities.
- Users can register and manage a profile.
- Eligibility is deterministic, criterion-level and distinguishable from unknown information.
- Relevance is separate from eligibility and not represented as selection probability.
- AI output is validated and does not invent facts.
- Admins can manage opportunity records and verification.
- Users can save opportunities and track application progress.
- Critical workflows have automated tests.
- The team can demonstrate the product and explain its limitations.

## 11. Dependencies & Assumptions
- Supabase project for PostgreSQL and Supabase Auth.
- DeepSeek API key for AI features.
- Vercel account for hosting when deployment is authorized.
- Existing GitHub repository: `S4M73CH/PathFinder`.
- Opportunity records are manually curated; target is approximately twenty verified records before demo, as stated in tutor V3.
- Users apply through official provider channels; PathFinder does not submit applications.
- Exact package versions are selected as the latest stable compatible versions at project bootstrap and fixed in `package-lock.json`.

## 12. Final Technical Decisions
The following are binding decisions from tutor V3:
- Modular monolith; one codebase and one deployment.
- Next.js App Router with TypeScript strict mode.
- PostgreSQL hosted on Supabase.
- Supabase Auth.
- Drizzle ORM and Drizzle Kit.
- Tailwind CSS with shadcn/ui.
- Zod for API input and AI output validation.
- DeepSeek only, through Vercel AI SDK and `@ai-sdk/deepseek`.
- Model `deepseek-v4-flash` in non-thinking mode.
- npm; commit `package-lock.json`.
- Vercel hosting.
- No background worker, queue or Redis in MVP.
- Deterministic application code decides structured eligibility; AI cannot decide or override it.
- Admin-curated opportunity data; no crawler.
- Applications are completed on official provider websites.

## 13. Approvals
| Name | Role | Signature | Date |
|---|---|---|---|
| Joshua Samson Anuoluwapo | Team Leader & Technical Lead | | |
| Samuel Oladunjoye Chigozirim | Technical Team Member | | |
| Mr Satar Sarafa | Tutor/Supervisor | | |
