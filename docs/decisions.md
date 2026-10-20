# Decisions Log

Record each decision here with the date and the reason, so we stop re-arguing settled things.

## Open

| Decision | Options | Status |
|---|---|---|
| Target customer type | Law firm, clinic, logistics, school, accounting, other | Open |
| Identity platform | Samba AD vs Microsoft Entra ID | Open |
| File platform | Nextcloud vs SharePoint | Open |
| Pricing model | Per user vs flat | Open (waiting on competitor quotes) |
| Business name / branding | TBD | Open |

## Decided

| Date | Decision | Why |
|---|---|---|
| 2026-10-20 | Start as a productized managed service, not a self-serve PaaS | Fastest path to revenue; automation comes after the reference setup is proven |
| 2026-10-20 | Repo is private | Will hold client-facing templates and service terms |
| 2026-10-20 | Design for a maximum of 30 workers per client | Keeps the reference setup simple (one tenant, small footprint), support load manageable, and pricing easy to explain |
