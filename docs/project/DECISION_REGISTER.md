# Decision Register — PathFinder AI

**Authority:** Tutor, PathFinder Project Documentation, Version 3.0 (Final), 10 November 2026.  
**Team-role amendment:** Confirmed by the project owner after the tutor document.

## Binding technical decisions
| Area | Final decision |
|---|---|
| Architecture | Modular monolith, one codebase and one deployment |
| Background work | None in MVP; no worker, queue or Redis |
| Language/framework | TypeScript strict mode; Next.js App Router |
| Database | PostgreSQL hosted on Supabase |
| Authentication | Supabase Auth |
| ORM/migrations | Drizzle ORM and Drizzle Kit |
| UI | Tailwind CSS and shadcn/ui |
| Validation | Zod |
| AI integration | DeepSeek only through Vercel AI SDK and `@ai-sdk/deepseek` |
| Model | `deepseek-v4-flash`, non-thinking mode |
| Package manager | npm; commit `package-lock.json` |
| Hosting | Vercel |
| Eligibility | Deterministic application code for structured criteria; AI cannot decide or override |
| Opportunity data | Admin-curated and verified; no crawler |
| Applications | Official provider channel; PathFinder does not submit |

## Compatibility check required at bootstrap
Latest stable compatible package versions are selected on day one and fixed in `package-lock.json`. The first build task tests structured-output compatibility for `deepseek-v4-flash` with the installed `ai` and `@ai-sdk/deepseek` versions. If structured output is unsupported, use text generation with Zod validation. This is a required verification task, not an unresolved stack choice.

## Team-role amendment
| Person | Confirmed role |
|---|---|
| Joshua Samson Anuoluwapo | Team Leader & Technical Lead |
| Samuel Oladunjoye Chigozirim | Technical Team Member |
| Moses Uvie Uvietabor | Opportunity Research & Data Collection |
| Efeteyan Etinosa Miracle | Opportunity Research & Data Collection |
| Oluwasola Josiah Temidayo | Documentation Lead |
| Shittu Abdulmalik Olasunkanmi | Pitch & Presentation Lead |
| Adebayo Isaac | Demo Lead |

Joshua and Samuel are the technical approvers/reviewers and coordinate code changes and repository delivery. Moses is not a technical approver.

## Product policies that the design must make explicit
The tutor document identifies these as design details rather than settled numeric rules. Propose simple, evidence-based definitions in the specification and flag only material trade-offs:
- Verification/recheck cadence.
- Definition of "closing soon".
- Application status handling and transition rules.
- Relevance factors and any weights.
- Admin review and publishing controls.
Do not invent a universal verification interval or arbitrary ranking weights and present them as tutor-approved.
