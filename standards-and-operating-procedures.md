# COPA Technology Standards and Operating Procedures

> **Status: DRAFT** — last updated 8 October 2026.

How COPA's software is built and run day to day, within the limits set by the [COPA Technology Governance Policy](governance-policy.md). The technology lead and the Director of Operations maintain this document. It changes as technology changes and doesn't need a board vote, but nothing in it may conflict with the policy.

The sections below describe the standard COPA is holding itself to. Some of it is not in place yet; the gaps are listed next, with target dates, and are removed from the list as they close.

## Where we are today

| Gap | Today | Target |
| --- | --- | --- |
| Service accounts in COPA's name | The COPA.fyi suite's hosting, database, email, analytics and AI accounts are held by the technology lead or his company and billed to COPA | All moved to COPA-owned logins, 16 Oct 2026 |
| Password vault | Not set up yet | COPA-owned vault chosen and in use, 16 Oct 2026 |
| Two-factor sign-in, branch protection, secret scanning, dependency alerts | Two-factor not yet required on COPA's GitHub organization; the rest not yet confirmed on every repository | On for every COPA repository, 16 Oct 2026 |
| Second operator | Only the technology lead can release a change; the Director of Operations is not yet in COPA's GitHub organization | Director of Operations can sign in and release a change, 16 Oct 2026 |
| Architecture overview, runbooks, data export, vendor list | Not written yet | Written and in each repository, 30 Oct 2026 |
| Request portal (Warren) | Runs on the technology lead's own hosting account | Runs on a COPA-owned account before COPA uses it |
| Build forum category | Not created yet | Created when the first program is approved |
| Takeover test | Not run yet | First run after the documentation is written |

## 1. Technology in use today

Everything below is mainstream and widely supported, and each piece can be replaced without rewriting the rest. This list describes current practice. It isn't a requirement, and it changes when something better comes along.

| Layer | Today | How COPA would leave it |
| --- | --- | --- |
| Database | PostgreSQL (hosted on Neon) | Standard dump and restore to any Postgres host |
| Applications | TypeScript, React, Next.js | Runs on any Node.js host or container |
| Hosting | Vercel | Redeploy the same code to another host |
| Code | Git, on GitHub (COPA's organization) | Git history moves to any Git host |
| Email sending | Resend | Swap in any email API or SMTP provider |
| Product analytics | PostHog | Open source; export the events or self-host |
| AI models | Commercial model APIs through standard SDKs | Switch providers in configuration; no single-model features |

New technology is added only when it's widely used, actively maintained, and has a clear exit path. Each addition is recorded in the changelog with its reason.

## 2. How changes are made

All code lives in COPA's GitHub organization (Cirrus-Owners-and-Pilots-Association). Nothing goes live except from there.

1. **Request.** Staff, volunteers or developers describe the change in plain English in the request portal (Warren) or as a GitHub issue.
2. **Build.** An AI agent or a developer makes the change on its own branch. Nothing goes straight to the live system.
3. **Check.** Automated tests and an automated code review run on every change.
4. **Preview.** The requester sees the change working on a preview site before it goes live.
5. **Release.** The change is merged and deployed. A release policy sets which changes ship automatically (small, low-risk changes in approved parts of the code) and which wait for a developer's sign-off.
6. **Record and undo.** Every request, change and release is logged with who asked for it, and any release can be rolled back in one step.

The main branch is protected. Secret scanning and dependency alerts are on for every repository.

## 3. Security and access

- **Accounts:** every service is registered under a COPA-owned login, never a personal one.
- **Credentials:** kept in a COPA-owned password vault. Secrets live in hosting environment settings, never in code.
- **Two operators minimum:** at least two people (one of them the Director of Operations) can sign in to every service and release a change.
- **Least access:** each person gets only what their role needs. Access is reviewed every quarter and removed the day someone leaves, and any keys they could see are rotated.
- **Member data:** never in code, test data or public repositories, and exported only to COPA-controlled destinations.
- **Payment cards:** card numbers and payment details stay with the payment processor. COPA's systems store only the processor's customer and subscription IDs.

## 4. Documentation and continuity

Every system keeps these up to date in its repository:

- **Architecture overview:** what the parts are, what they talk to, and where data lives.
- **Runbooks:** how to release, roll back, restore the database, rotate keys, and handle the common failures.
- **Data export:** a documented way to export all member data in standard formats (CSV, Postgres dump).
- **Vendor list:** every outside service, its monthly cost, the COPA account that owns it, its contract terms (month-to-month where possible), and its exit path.

**Takeover test:** once a year, someone other than the technology lead (by default the Director of Operations) releases a change and restores a backup using only the documentation. Gaps they hit get fixed.

## 5. Connected outside systems

Outside systems connect through their standard APIs, and COPA keeps its own copy of the data it needs, so leaving any one of them never strands member data.

| System | Used for | Status |
| --- | --- | --- |
| Discourse | Forums | Stays; connected more deeply over time |
| Maxio | Charging cards, subscriptions | Stays as the card processor only |
| MailChimp | Email campaigns | Kept in sync from the member record |
| Passport / IdRamp | Sign-in, member profile | In use; future handled by its own program |
| RegFox, Zoho Backstage | Event registration | Synced nightly |
| TalentLMS | Online courses | Matched to member records |
| cirruspilots.org (DNN) | Public website | In use; future handled by its own program |

## 6. Building in public

- **Forum category:** a dedicated Discourse category for the build, with the roadmap, demos, and feature requests and discussion from members.
- **Changelog:** a plain-English entry for every release that members would notice, posted in that category.
- **Hours ledger:** for each program, hours by person, marked billed or donated, updated at least monthly and summarized in the Goal 2 update to the board.
- **Board update:** posted in the Goal 2 Teams channel at least 5 days before each board meeting: what shipped, hours, spend against budget, and what's next.

## 7. Designing for other clubs

- COPA-specific details (names, logos, colors, aircraft models, membership tiers, connected services) live in configuration, not in the code.
- No COPA member data, Cirrus or Garmin content, or COPA trademarks are kept in the code itself.
- Repositories are kept in a state where they could be published once the board decides. That decision, and the license, belong to the board under Section 5 of the Governance Policy.
