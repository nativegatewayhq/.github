# Governance

## Roles

- **Contributors** propose plans and changes.
- **Maintainers** review plans, code, compatibility, and release readiness.
- **Repository owners** define local ownership and approve releases.
- **Organization owners** manage shared policy, security, and repository boundaries.

## Decisions

- Repository-local implementation decisions are recorded in timestamped plans or ADRs.
- Cross-repository scope, repository boundaries, licensing, and public contracts are recorded in `roadmap`.
- Security incidents and credential exposure are handled privately before public disclosure.
- Accepted plans require maintainer review before implementation begins.

## Compatibility

Public native-protocol behavior, SDK compatibility, ledger semantics, and plugin contracts require explicit migration and rollback plans before incompatible changes.

## Policy changes

Organization-wide policy changes are proposed through a pull request to this repository. Material changes must explain affected repositories and rollout steps.
