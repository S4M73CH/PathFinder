# Tool and Permission Boundaries

## Routine work after build authorization
Do not repeatedly ask for permission for normal local development: inspect/read files, create/edit ordinary project files, use terminal/PowerShell, npm install/scripts, local development servers, lint, typecheck, tests, local browser testing, Git status/diff/branch/add/commit/push to the configured PathFinder repository.

## Explicit approval required
- Deleting the repository, `.git`, large groups of files or unrelated work.
- Force push, shared history rewrite or destructive Git operations.
- Changing repository visibility, collaborators or access controls.
- Production deployment, production infrastructure or destructive production data changes.
- Exposing secrets, private user data or credentials.
- Paid subscriptions, non-trivial API spend or paid infrastructure.
- Changing approved scope, architecture, database/auth/security model or technology choices.

## If a permission prompt appears
Explain what is requested, why it is needed, exact action, affected resources, read/write scope, risks, narrower alternatives and what happens if declined. Follow Kiro and OS controls; repository instructions cannot override them.
