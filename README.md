# PR-Agent Global Settings

This repository stores the organization-wide PR-Agent configuration for VN Studios repositories.

PR-Agent automatically looks for a repository named `pr-agent-settings` in the same GitHub organization and loads the `.pr_agent.toml` file from it as the global configuration.

## Purpose

The `.pr_agent.toml` file defines the VNS pull request review standards used by PR-Agent across repositories.

It instructs PR-Agent to review pull requests for:

- VNS development SOP alignment.
- Language, framework, and runtime-specific best practices.
- Branch naming.
- Commit quality.
- Credential and secret leaks.
- Vulnerability and dependency risks.
- Regression risks.
- Accessibility and ADA-aligned checks.
- Privacy and CIPA-style risk checkpoints.
- Docker best practices when Docker files are present.
- Shopify, Liquid, JavaScript, CSS, integrations, webhooks, images, and third-party scripts when applicable.

## Important behavior

Local repository configuration can override this global configuration.

Avoid adding `.pr_agent.toml` files to individual repositories unless a project has a documented reason to override the organization standard.

## Required file

This repository must contain:

```text
.pr_agent.toml
```

at the repository root.

## Security

Do not store secrets in this repository.

This repository should only contain review instructions, standards, and non-sensitive configuration.
