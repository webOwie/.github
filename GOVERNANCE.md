# webOwie Governance

## Purpose

webOwie is developed as a modular engineering ecosystem. Governance exists to keep architectural decisions explicit, security-sensitive changes reviewable, and repositories understandable as the project grows.

## Decision levels

### Routine changes
Documentation, tests, bug fixes, dependency maintenance and non-breaking implementation details may be handled through normal pull requests.

### Architecture changes
Changes that affect repository boundaries, public interfaces, trust boundaries, persistence formats, authentication, networking, deployment models or agent permissions require an Architecture Decision Record (ADR) in `webowie-docs/adr/`.

### Protected changes
The following require explicit maintainer review and must never be applied solely from generated AI output:

- production DNS and nameserver changes
- authentication and authorization policy changes
- secret-management changes
- destructive infrastructure operations
- repository deletion or visibility reduction
- irreversible data migrations

## Repository ownership

Each repository should have one clear responsibility. New repositories are created only when a component has an independent release lifecycle, security boundary, deployment model or maintenance responsibility.

## Change workflow

1. Open an issue for substantial features or architecture work.
2. Create a focused branch from `main`.
3. Add tests or validation appropriate to the change.
4. Document security and architecture impact in the pull request.
5. Use an ADR when the decision changes system structure or long-term constraints.
6. Merge only after required checks pass.

## AI-assisted development

AI may generate code, documentation, tests and change plans. Generated changes are treated as untrusted input until reviewed and validated. AI systems must not receive unrestricted production credentials or bypass explicit approval gates for protected operations.

## Releases

Projects that produce versioned software use Semantic Versioning where practical. Release notes should identify user-visible changes, security-relevant changes, migration requirements and known limitations.
