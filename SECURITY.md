# Security Policy

## Reporting a vulnerability

Please do not disclose suspected vulnerabilities in a public issue.

Use GitHub private vulnerability reporting where available. If private reporting is not enabled for the affected repository, use the official contact channel published on https://webowie.com.

Include:

- affected repository and version or commit
- concise description of the issue
- reproduction steps or proof of concept
- expected impact
- any suggested mitigation

## Security principles

webOwie follows these baseline rules:

- least privilege for tokens, services and automation
- no credentials committed to repositories
- explicit trust boundaries and data flows
- review gates for DNS, identity, secrets and destructive infrastructure operations
- local-first processing where practical
- auditable change history
- rollback or recovery paths for production mutations

## Secrets

Never commit API keys, tokens, passwords, certificates, private keys or `.env` files containing live credentials. Use environment variables or an approved secret store.

If a secret is committed accidentally, revoke or rotate it immediately. Removing it from Git history alone is not sufficient.

## AI and agent safety

AI-generated changes are untrusted until reviewed and validated. Agents may prepare plans, code and configuration, but protected operations must remain behind explicit validation and approval boundaries.

## Supported versions

Until an individual repository publishes a version-support matrix, only the current `main` branch and latest tagged release should be assumed to receive security fixes.
