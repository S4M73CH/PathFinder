# Project Brief

## Project Title
PathFinder AI — Opportunity Discovery and Career Readiness Platform

## Date
01/11/2026

## Prepared By
**Team Nexus** — Project Development Team

**Team members**
1. Joshua Samson Anuoluwapo — Team Leader
2. Moses Uvie Uvietabor — Team Member
3. Samuel Oladunjoye Chigozirim — Team Member
4. Efeteyan Etinosa Miracle — Team Member
5. Oluwasola Josiah Temidayo — Team Member
6. Shittu Abdulmalik Olasunkanmi — Team Member
7. Adebayo Isaac — Team Member

*Team-member details may be edited or expanded by Team Nexus.*

## 1. Executive Summary
PathFinder AI is an AI-assisted opportunity discovery and career-readiness platform for Nigerian university undergraduates and recent graduates. It will help users discover global scholarships, SIWES/IT placements, internships, fellowships, graduate programmes, funded training and leadership opportunities, understand stated eligibility requirements, and prepare through grounded readiness guidance. The MVP will prioritise trustworthy, admin-curated opportunity information, deterministic eligibility assessment, transparent relevance ranking and AI-assisted preparation plans.

## 2. Background & Context
Finding suitable opportunities can be difficult because information is distributed across provider websites, eligibility rules vary by nationality and residence, funding arrangements are not always clear, and deadlines or programme details can become outdated. An international opportunity is not automatically open to Nigerian applicants.

PathFinder addresses this problem by bringing opportunity information into a searchable catalogue and preserving official source links, verification information and uncertainty. Visitors will be able to browse public opportunities without registering. An account will be required for a personal academic/career profile, personalised assessment, saved opportunities and application-progress tracking.

The platform separates three functions:
- **Eligibility:** deterministic evaluation of structured mandatory criteria. Missing information remains unknown; the AI model cannot decide or override eligibility.
- **Relevance:** transparent assessment of how closely an opportunity aligns with a user's profile and goals. A relevance score is not a probability of selection.
- **Readiness:** AI-assisted explanations and preparation plans grounded in verified opportunity facts and known profile gaps.

The MVP will use manually curated and verified opportunity records. Users will complete applications through the official provider channel; PathFinder will not submit applications on their behalf.

## 3. Objectives
- **Primary Objective:** Deliver a functional MVP that helps Nigerian undergraduates and recent graduates discover relevant opportunities, understand stated eligibility, and prepare for applications.
- **Secondary Objectives:**
  - Provide public opportunity browsing, search and filtering.
  - Support academic and career profiles relevant to opportunity assessment.
  - Represent applicant nationality, residence and opportunity destination separately.
  - Represent funding as separate components and preserve unknown/not-stated information.
  - Provide deterministic, criterion-level eligibility results and transparent relevance factors.
  - Use DeepSeek through the Vercel AI SDK for grounded AI explanations and readiness plans, without allowing the LLM to determine eligibility.
  - Allow users to save opportunities and record application progress.
  - Provide administrative opportunity review, verification and publication controls.
  - Protect user data and maintain traceability, automated tests and setup documentation.

## 4. Scope

### In Scope
- Public catalogue of published opportunities, with search and supported filters.
- Opportunity detail pages with provider, eligibility, funding, deadline/status, source evidence and official application link.
- User registration/authentication and academic/career profile management.
- Admin-curated opportunity records and verification workflow.
- Structured eligibility criteria and deterministic eligibility assessment.
- Separate relevance ranking with explainable factors.
- DeepSeek-backed, schema-validated explanations and readiness plans.
- Saved opportunities and basic application-progress tracking.
- Responsive mobile and desktop experience.
- Server-side authorization, protected secrets, automated tests and project documentation.
- Modular-monolith architecture with no separate worker application in the MVP.

### Out of Scope
- Automated application submission.
- Large-scale web crawling or scraping at launch.
- CV/document upload and parsing.
- WhatsApp/email reminders.
- CV or cover-letter generation and AI interview coaching.
- Employer dashboards and university integrations.
- Multi-agent orchestration or multi-provider LLM routing.
- Microservices, a separate worker application, Redis/BullMQ, vector database, pgvector or advanced RAG/vector retrieval unless a documented need is demonstrated and approved.

## 5. Key Deliverables

| # | Deliverable | Description | Due Date |
|---|---|---|---|
| 1 | Approved project brief | Tutor-template project brief for PathFinder AI and Team Nexus | 15/11/2026 |
| 2 | Project specifications | Requirements, architecture/design, tasks, acceptance criteria and requirement traceability | 15/11/2026 |
| 3 | Project foundation | Repository setup, application scaffold, configuration, validation, linting and test foundation | 15/11/2026 |
| 4 | Identity and profile foundation | Authentication approach and undergraduate/recent-graduate profile workflow, subject to approved provider setup | 15/11/2026 |
| 5 | Opportunity catalogue | Curated opportunity records, public browsing, details, search/filter and verification controls | 15/11/2026 |
| 6 | Eligibility and relevance | Deterministic eligibility assessment, criterion-level outcomes and separate explainable relevance ranking | 15/11/2026 |
| 7 | AI readiness capability | DeepSeek-backed, validated explanations and readiness plans grounded in supplied data | 15/11/2026 |
| 8 | Saved opportunities and tracking | Bookmarking and basic user-managed application progress | 15/11/2026 |
| 9 | Quality and handover package | Automated tests, setup guide, data guide, decisions, handover instructions and demonstration script | 15/11/2026 |

*The deliverables and dates reflect the team's stated submission deadline. Their feasibility depends on timely decisions, external service access, team capacity and tutor review.*

## 6. Timeline & Milestones

| Phase | Milestone | Start Date | End Date |
|---|---|---|---|
| 1 | Project initiation, review of source documents and specification | 01/11/2026 | 03/11/2026 |
| 2 | Architecture, data model and specification approval | 04/11/2026 | To be confirmed |
| 3 | Project foundation and core application setup | To be confirmed | To be confirmed |
| 4 | Core product workflows and AI readiness capability | To be confirmed | To be confirmed |
| 5 | Testing, integration, documentation and final demonstration | To be confirmed | 15/11/2026 |
| 6 | Final project submission | 15/11/2026 | 15/11/2026 |

**Overall project period supplied by the team:** 01/11/2026–15/11/2026.  
**Submission deadline:** 15/11/2026. Detailed intermediate dates remain to be agreed with the tutor and team.

## 7. Budget
No approved budget has been provided. Estimated costs are **not yet determined**.

Potential cost areas to assess before use include hosting, managed database services, authentication, domain registration and external API usage. The team must verify free-tier limits, usage restrictions and any billing implications before connecting or enabling paid services.

| Item | Estimated Cost |
|---|---:|
| Hosting and deployment | Not yet estimated |
| Database and authentication services | Not yet estimated |
| DeepSeek API usage | Not yet estimated |
| Domain and other services | Not yet estimated |
| **Total** | **Not yet estimated** |

## 8. Stakeholders & Roles

| Name | Role | Responsibility |
|---|---|---|
| Team Nexus | Project development team | Collaborative planning, design, implementation, testing and submission |
| Joshua Samson Anuoluwapo | Team Leader | Coordinate Team Nexus and lead project delivery |
| Moses Uvie Uvietabor | Team Member | Project-team contribution; specific task allocation to be agreed |
| Samuel Oladunjoye Chigozirim | Team Member | Project-team contribution; specific task allocation to be agreed |
| Efeteyan Etinosa Miracle | Team Member | Project-team contribution; specific task allocation to be agreed |
| Oluwasola Josiah Temidayo | Team Member | Project-team contribution; specific task allocation to be agreed |
| Shittu Abdulmalik Olasunkanmi | Team Member | Project-team contribution; specific task allocation to be agreed |
| Adebayo Isaac | Team Member | Project-team contribution; specific task allocation to be agreed |
| Mr Satar Sarafa | Tutor / Project Supervisor / Approver | Provide supervision and review/approve the project brief and consequential project decisions |

*Individual technical work packages beyond the team-leader role have not yet been assigned.*

## 9. Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Opportunity information becomes outdated | High | High | Use manual curation, official sources, verification timestamps and lifecycle states; do not present uncertain listings as confirmed open |
| Eligibility rules are ambiguous or vary by country | High | High | Preserve source evidence; separate nationality, residence and destination; flag ambiguous criteria for human review |
| Incorrect eligibility decisions | Medium | High | Use deterministic, tested rule evaluators; treat missing data as unknown; never let the LLM decide eligibility |
| AI produces unsupported or fabricated claims | Medium | High | Supply verified facts and computed results only; validate structured output; reject unsupported claims; provide clear failure handling |
| Matching weights create misleading rankings | Medium | Medium | Explain ranking factors, document rationale, test results and obtain approval before fixing weights |
| Authentication/database/hosting choices are delayed | Medium | High | Compare viable options early and obtain approval before implementation or external setup |
| API access, rate limits, latency or cost affect AI features | Medium | Medium/High | Verify DeepSeek API access, model availability, limits and cost; keep catalogue and deterministic checks usable without AI |
| Funding details are incomplete or misunderstood | Medium | High | Store funding components independently and preserve unknown/not-stated values with source evidence |
| Deadline and timezone errors | Medium | High | Preserve source timezone context and display deadline timezone clearly |
| Short delivery window limits testing and integration | High | High | Prioritise MVP workflows, work in small verified increments, agree task ownership and reserve time for integration/testing |

## 10. Success Criteria
The project will be considered successful for the MVP submission when the team can demonstrate and provide evidence that:

1. Visitors can browse published opportunities without registering.
2. Users can create an account and maintain an appropriate academic/career profile, subject to the approved authentication setup.
3. Opportunity records preserve official source links, verification timestamps and lifecycle status.
4. Unverified or confirmed-expired opportunities are not presented as confirmed open opportunities.
5. Structured mandatory eligibility criteria are evaluated deterministically and shown criterion by criterion.
6. Missing information is represented as unknown or requiring review, never silently treated as a pass.
7. Eligibility, relevance and readiness remain separate; relevance never overrides a mandatory eligibility failure.
8. DeepSeek explanations/readiness plans use validated outputs grounded in supplied facts and cannot change eligibility outcomes.
9. Users can save opportunities and record basic application progress.
10. Protected user data and administrative actions are enforced server-side and tested.
11. Core workflows have automated tests and the repository includes clear setup and handover documentation.
12. The team can demonstrate the working MVP and submit the project by 15/11/2026.

## 11. Dependencies & Assumptions

### Dependencies
- Access to the project repository and development environment.
- Timely review and approval by Mr Satar Sarafa.
- Access to a DeepSeek API key and confirmation of applicable model/API limits before enabling AI features.
- Selection and setup of an authentication provider, PostgreSQL hosting/database provider and deployment platform.
- Network access to required external services.
- Team availability and timely integration of individual contributions.
- A manually curated set of opportunity records with official source evidence for meaningful demonstration.

### Assumptions
- The project period is 01/11/2026 to 15/11/2026, with final submission on 15/11/2026, as supplied by Team Nexus.
- Team Nexus is the project development team and Joshua Samson Anuoluwapo is its leader.
- Mr Satar Sarafa is the tutor, project supervisor and approval authority identified by the team.
- The MVP targets Nigerian undergraduates and recent graduates and covers global opportunities only where applicant eligibility can be supported by evidence.
- The product and technical reference (Version 2.0) is authoritative for product scope and confirmed technical decisions.
- The application will use a modular monolith and will not introduce a separate worker application in the MVP.
- DeepSeek is the sole LLM provider in the MVP through the Vercel AI SDK and `@ai-sdk/deepseek`.
- The exact framework version, authentication provider, database host, package manager and deployment configuration remain subject to implementation review and approval.
- API access may be required; no API key, account, paid plan or budget is assumed to exist.
- No project budget has been approved or estimated.

## 12. Approvals

| Name | Role | Signature | Date |
|---|---|---|---|
| Mr Satar Sarafa | Tutor / Project Supervisor / Project Approver | ____________________ | ____________________ |
| Joshua Samson Anuoluwapo | Team Leader, Team Nexus | ____________________ | ____________________ |
