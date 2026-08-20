# Organization Contribution Policy

Native AI Gateway repositories use a **Plan First** development workflow.

## Core workflow

1. Read the target repository's `AGENTS.md`, `CONTRIBUTING.md`, and `plans/README.md`.
2. Find the accepted plan governing the requested change.
3. If no plan exists, create one from `plans/TEMPLATE.md` before implementation.
4. Implement only the accepted scope.
5. Run the plan's required verification.
6. Record reproducible evidence before marking the plan complete.

## Plans are an append-only decision log

- New work uses a timestamped `plan` file.
- Material scope or design changes use a new `change` file.
- Withdrawals use a new `rollback` file.
- Existing accepted plans retain their historical scope and acceptance criteria.
- Status, timestamps, checklist results, and verification evidence may be updated in place.
- Cross-repository work uses the same `initiative` value but a separate local plan in each affected repository.

## Mandatory invariants

Changes must not violate these project-wide guarantees:

1. A logical request is never charged twice.
2. Concurrent requests cannot make available balance negative.
3. A provider timeout is not assumed to be a provider failure.
4. Monetary changes remain auditable through an append-only ledger.
5. Provider credentials and service API key plaintext never enter logs.
6. Fallback preserves operation semantics and billing conditions.
7. Asynchronous work and settlement survive process restarts.
8. Repeated polling and webhooks are idempotent.
9. Pricing and routing policies have versions and effective times.
10. A control-plane outage does not automatically become a data-plane outage.

## Pull requests

Every non-trivial pull request must include:

- plan ID and link;
- purpose and scope;
- tests executed and their results;
- security and billing impact;
- compatibility or migration impact;
- rollback approach.

Small typo, broken-link, formatting, or test-only fixes may state why no plan is required.

Repository-local instructions take precedence where they are more specific and do not weaken these organization-wide invariants.
