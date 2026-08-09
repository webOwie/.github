# Contributing to webOwie

Thanks for contributing to webOwie. Keep changes focused, reproducible and reviewable.

## Before you start

- Search existing issues and pull requests first.
- Open an issue for substantial features, architecture changes or security-sensitive work.
- Do not commit secrets or production credentials.
- Prefer deterministic configuration over undocumented manual state.

## Branches

Use focused branch names such as:

- `feat/<topic>`
- `fix/<topic>`
- `docs/<topic>`
- `chore/<topic>`

The default integration branch is `main`.

## Commits

Prefer Conventional Commit style:

- `feat: add ...`
- `fix: correct ...`
- `docs: document ...`
- `chore: maintain ...`
- `refactor: restructure ...`
- `test: add ...`

## Pull requests

A pull request should explain:

1. what changed
2. why the change is needed
3. how it was validated
4. security impact
5. architecture impact
6. rollback or recovery considerations when infrastructure is affected

Keep unrelated changes in separate pull requests.

## Architecture decisions

Changes affecting repository boundaries, public interfaces, authentication, trust boundaries, persistence, networking or deployment models should include an ADR in `webowie-docs/adr/`.

## Infrastructure changes

Changes to DNS, identity, secrets, networking or production infrastructure must provide a dry-run, simulation, validation step or rollback path where technically possible.

## AI-assisted contributions

AI-generated code and documentation are welcome, but they must be reviewed as untrusted input. Generated output does not bypass tests, security review or protected-operation approval gates.

## Documentation

Keep documentation close to the system it describes. Long-lived cross-project architecture belongs in `webowie-docs`; repository-specific setup and behavior belongs in that repository.
