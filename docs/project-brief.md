# PaaS Time: Project Brief

*Created 20 Oct 2026. Update as decisions get made.*

## The idea
A productized business-IT offering for Nigerian SMEs: a structured, hierarchical environment where staff work, share files and handle sensitive information, with **access control and accountability** as the core promise. Directory-based roles, secure file sharing, MFA, backups and audit logs, sold as fixed packages in naira and later automated into a self-serve platform.

## Honest framing
- Today this is a managed service, not a PaaS. That is the faster path to revenue.
- Ladder: (1) productized service, (2) templated automation, (3) self-serve platform. Only stage 3 earns the name "PaaS".

## Positioning
- Sell the outcome: "I make sure the wrong person can't see payroll, and I can prove it."
- Security is both a baseline in every package and the main selling point.

## Draft packages (naira prices TBD)
**Baseline in every tier:** MFA on all accounts, least-privilege roles (Admin / Manager / Staff / Guest), audit logs, encrypted and tested backups, patching, staff offboarding checklist.

| Tier | Contents |
|---|---|
| Basic | Baseline |
| Business | Baseline + endpoint protection / device management + monitoring and alerting |
| Secure | Business + phishing awareness training, periodic access reviews, incident-response retainer |

## Possible stack (validate in lab)
Samba AD or Microsoft Entra ID; Nextcloud or SharePoint; centralized logging; automated backups; AWS hosting.

## Market research (20 Oct 2026)
- Local managed IT providers bill in naira on fixed monthly plans: e-Technologies (e-Tech 360), Netcat, Wragby, Cells Station, Layer3.
- Identity specialists in Lagos (Ethnos Cyber, Tiger Logic, Infodata) mostly resell enterprise products to banks and large firms.
- Gap: no public small-business, identity-first packages with transparent naira pricing found. Absence from web search is not proof.
- Cells Station's exec says convincing SMEs to adopt managed services is slow.

## Quote requests
Sent as Boka Inc on 20 Oct 2026. Pending: tiers, per-user vs flat pricing, SLAs, response times.

## Risks
- Trust: need service agreement, NDA, data-handling policy before customer #1.
- Support load: define support hours and SLAs.
- Concentration risk: strict tenant isolation, password vault, MFA on all admin access, no shared credentials.
- USD licence costs against naira revenue.

## Roadmap
1. ~~Choose ONE target customer type.~~ Decided 20 Oct 2026: law firm is the core/demo; school and clinic are variants; max 30 workers per client. See `vertical-templates.md` and `decisions.md`.
2. Build the reference setup in a lab.
3. Draft three tiers; price after quotes arrive.
4. Write the legal pack.
5. Harden our own operations.
6. Later: automate provisioning, then a self-serve dashboard.

## Open decisions
Samba AD vs Entra ID; Nextcloud vs SharePoint; per-user vs flat pricing; business name / branding.
