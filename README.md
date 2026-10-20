# PaaS Time

A productized business-IT offering for Nigerian SMEs: a structured, hierarchical environment where staff work, share files and handle sensitive information, with **access control and accountability** as the core promise.

Today this is a managed service. The ladder to a real PaaS:

1. Productized service with fixed naira packages
2. Templated automation (scripts / Terraform / Ansible)
3. Self-serve platform that provisions a client environment from a chosen tier

## Repo layout

| Path | Purpose |
|---|---|
| `docs/` | Project brief, market research, pricing, decisions |
| `legal/` | Service agreement, NDA, data-handling policy (drafts) |
| `lab/` | Reference setup: directory, roles, MFA, file sharing, logging, backups |
| `automation/` | Provisioning scripts and templates (stage 2) |

## Status

- [x] Idea, positioning and draft tiers (see `docs/project-brief.md`)
- [x] Competitor quote requests sent (20 Oct 2026), replies pending
- [ ] Choose ONE target customer type
- [ ] Build the reference lab
- [ ] Price the three tiers in naira
- [ ] Legal pack
- [ ] Harden our own operations

## Rules for this repo

- No real client data, credentials or keys, ever. Use `.env.example` style placeholders.
- Every client environment gets its own isolated config; nothing shared across tenants.
