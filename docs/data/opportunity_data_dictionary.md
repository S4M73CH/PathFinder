# Opportunity Data Dictionary (for Team Nexus data collection)

This dictionary tells the non-technical team exactly how to record each opportunity
in the Google Sheet so it imports cleanly into PathFinder at the end of the project.
It maps one-to-one to the approved database schema (design.md, Data Models).

How to use it:
- One opportunity per row in the Sheet.
- Use the exact column names in `opportunity_sheet_template.csv`.
- Where a field has "Allowed values", use ONLY those values (copy-paste to avoid typos).
- If a fact is not stated by the provider, write `unknown` (do NOT guess, do NOT leave
  a required field blank). Preserving "unknown" is a core project rule.
- Keep applicant nationality, applicant residence, and opportunity destination SEPARATE.
  An international programme is NOT automatically open to Nigerians.
- Do not infer funding from the title, or an open deadline from an old page.

Legend: [required] must be filled; [optional] may be left blank; [unknown-ok] use
`unknown` when the provider does not state it.

## Core identity

| Column | Rule | Allowed values / format |
|---|---|---|
| `title` | [required] Official programme name. | Free text |
| `provider_name` | [required] Organisation offering it. | Free text |
| `provider_website` | [optional] Organisation home page. | URL (https://...) |
| `provider_country` | [optional] Where the organisation is based. | Country name |
| `category` | [required] One fixed category. | `scholarship`, `siwes_it`, `professional_internship`, `fellowship`, `graduate_programme`, `funded_training`, `leadership_opportunity` |
| `description` | [optional] Short summary. | Free text |
| `official_url` | [required] The official page where users apply. | URL (https://...) |

## Status, timing and verification

| Column | Rule | Allowed values / format |
|---|---|---|
| `lifecycle_state` | [required] Current status. | `draft`, `under_review`, `published_open`, `upcoming`, `closing_soon`, `closed_expired`, `unknown_needs_recheck`, `archived` |
| `delivery_mode` | [optional] | `in_person`, `remote`, `hybrid` |
| `deadline` | [unknown-ok] Application deadline. | `YYYY-MM-DD`, or `rolling`, or `unknown` |
| `deadline_timezone` | [optional] Timezone the deadline is stated in. | e.g. `WAT`, `UTC`, `GMT+1` |
| `opening_date` | [optional] When applications open. | `YYYY-MM-DD` or blank |
| `last_verified_date` | [required] Date YOU checked the official page. | `YYYY-MM-DD` |
| `verified_by` | [required] Who checked it (name/initials). | Free text |
| `source_url` | [required] The exact page you verified (often same as official_url). | URL |
| `source_notes` | [optional] What you saw / evidence. | Free text |

## Geography — keep these THREE separate (FR-08)

| Column | Rule | Meaning |
|---|---|---|
| `destination_country` | [unknown-ok] Where the opportunity takes place. | Country or `unknown` |
| `destination_city` | [optional] City, if stated. | City or blank |
| `applicant_nationality_rule` | [unknown-ok] Which nationalities may apply. | e.g. `Open to all`, `Nigerian citizens`, `unknown` |
| `applicant_residence_rule` | [unknown-ok] Residence requirement for applicants. | e.g. `Must reside in Nigeria`, `No restriction`, `unknown` |

## Funding — one column per component (FR-09). Use `unknown` or `not_stated`.

| Column | Rule | Allowed values / format |
|---|---|---|
| `funding_tuition` | [unknown-ok] Tuition coverage. | amount+currency, `fully_covered`, `not_stated`, `unknown` |
| `funding_stipend` | [unknown-ok] Living stipend. | amount+currency+frequency, `not_stated`, `unknown` |
| `funding_travel` | [unknown-ok] Travel support. | `covered`, `not_covered`, `not_stated`, `unknown` |
| `funding_accommodation` | [unknown-ok] Accommodation support. | `covered`, `not_covered`, `not_stated`, `unknown` |
| `funding_notes` | [optional] Anything else about money. | Free text |

## Eligibility criteria (optional structured hints)

You can list up to a few key requirements. Keep each short; the technical team will
structure them. Mark whether each is mandatory.

| Column | Rule | Format |
|---|---|---|
| `criteria_1` ... `criteria_3` | [optional] One requirement each. | e.g. `education_level: undergraduate (mandatory)` |

Notes:
- If a requirement is unclear or can't be stated simply, write it plainly and add
  `(needs review)`. The technical team will flag it for human review rather than guess.
- NYSC status, age, language, documents are all valid requirements to note.