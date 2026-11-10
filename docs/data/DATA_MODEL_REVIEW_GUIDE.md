# Data Model Review Guide

The tutor's entity inventory is conceptual, not a final table-by-table schema. Kiro must propose a normalized Drizzle schema and explain why entities are combined or kept separate.

## Entity inventory to account for
- users
- profiles
- skills / user_skills
- experiences
- organizations
- opportunities
- opportunity_categories
- opportunity_locations
- applicant_eligibility
- eligibility_criteria
- funding_components
- opportunity_sources
- verification_events
- eligibility_assessments
- match_results
- saved_opportunities
- applications
- action_plans / tasks

## Required schema proposal content
1. Tables and purpose; explain combined/omitted concepts.
2. Primary keys, foreign keys, unique constraints, check constraints and indexes.
3. Relationships and cardinalities.
4. User ownership and admin access boundaries.
5. Representation of unknown, not stated, ambiguous and needs-review values.
6. Separate applicant nationality, applicant residence and opportunity destination.
7. Multi-component funding with amount, currency, frequency and evidence state.
8. Criterion type/operator/required value/mandatory-or-preferred/source reference.
9. Source URLs, checked dates, evidence notes, reviewer and lifecycle state.
10. Deletion, archive, retention and audit behaviour.
11. Migration strategy, rollback/recovery approach and seed-data approach.

## Mandatory approval gate
Joshua and Samuel review the schema proposal before any migration is generated or run against a database. A migration must never be used to discover whether the schema is correct.
