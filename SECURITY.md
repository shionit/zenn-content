# Security Policy

## Scope

This repository hosts personal blog content for [Zenn.dev](https://zenn.dev).
It contains no application code, APIs, or user data.

## Reporting a Vulnerability

If you discover a security issue in the repository infrastructure (GitHub Actions
workflows, Dockerfile, or Renovate configuration), please open a
[GitHub Issue](https://github.com/shionit/zenn-content/issues) with the label
`security`.

For sensitive matters, contact the maintainer directly via the email listed on
their GitHub profile.

## Automated Security Tooling

| Tool | Purpose |
|---|---|
| Renovate | Automated dependency updates with SHA pinning for Actions |
| StepSecurity Harden Runner | Runtime monitoring of GitHub Actions jobs |
| GitHub Dependabot alerts | Vulnerability alerts for known CVEs |
| GitHub Secret Scanning | Detects accidentally committed credentials |
