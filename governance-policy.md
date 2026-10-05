# COPA Technology Governance Policy

> **Status: DRAFT for board review** — not yet adopted. Last updated 5 October 2026.

COPA owns, builds and controls the software its members use. This policy sets the board's guardrails for that software: the outcomes it must deliver, the risks it must avoid, how money is approved, and who is accountable, whoever does the building. The technical detail of how those guardrails are met lives in a separate document, [COPA Technology Standards and Operating Procedures](standards-and-operating-procedures.md). That document can change as technology changes without a board vote, as long as it stays within this policy.

## 1. Purpose and scope

This policy covers all software COPA builds or commissions. That includes the COPA.fyi suite, the member database and CRM, the member portal and every tool that follows. It applies the same way whether the work is done by a volunteer, a director, a contractor or a firm.

Two outside services stay in place and are connected to COPA's software rather than replaced: **Discourse** for the forums, and a **payment processor** (Maxio today) for charging cards and the compliance that comes with it. Every other system is kept, connected or replaced one program at a time, as each program's proposal sets out.

The goal is the four member promises: *I sign in once. I can find it. COPA knows me. I know what to do next.*

## 2. Principles

1. **COPA owns everything.** Code, data, documentation, domains and every service account belong to COPA and are held in COPA's name. The Director of Operations has administrator access to all of it.
2. **No vendor lock-in.** COPA can move any part of its software to another provider in days, not months, without losing data or features. COPA uses mainstream, widely adopted technology that many developers can work with, not one-off or niche tools.
3. **Built for members.** Software serves how COPA members fly, train and own their aircraft. COPA can change it quickly, without waiting on a vendor.
4. **Built in public.** Members can see the roadmap, the progress, the changes, and the hours and cost behind each program, as the work happens.
5. **Integrate what works.** A system is replaced only when that gives members something they can't get otherwise. Discourse and the payment processor are connected, not replaced.
6. **Changes are visible and reversible.** Changes may be made by people or by AI, including changes requested by non-developers. Every change is recorded with who asked for it, and any change can be undone.
7. **Anyone can take over.** Every system is documented well enough that a qualified person who has never seen it can run it. At least two people can operate each system, and no one person holds the only access.
8. **Member data is protected.** Member data is never made public or stored outside COPA-controlled systems. Access is limited to what each role needs, and access is removed when someone leaves. Payment card details stay with the payment processor and are never held in COPA's own systems.
9. **Designed to share.** Software is built so another type club could run it with its own settings. Whether COPA actually publishes it is a separate board decision (Section 5).

## 3. How work is authorized and paid for

Work is approved and funded one program at a time. There is no single open-ended commitment.

1. **Roadmap.** One public list of everything COPA intends to build, in order. Goal leaders add to it, and the board sets priority.
2. **Program proposal.** Each program gets one page: scope, estimated hours and cost, what "done" means, and who builds it.
3. **Approval.** The board approves each program by vote before work starts.
4. **Build and report.** Work happens in public and is reported under Section 4. A program that will exceed its estimate goes back to the board before the overrun happens.

**Paid work by a director.** A director can be paid for software work when the board approves it by vote and that director doesn't vote. The terms (rate, donated hours, ownership, how either side can end it) go in a separate written engagement, not in this policy. Every billed and donated hour is published.

## 4. Reporting

- **To the board, monthly,** in the board's Goal 2 channel at least 5 days before each board meeting: what shipped, hours billed and donated, spend against each program's budget, and what's next.
- **To members, continuously,** in a forum category for the build: the roadmap, demos, the changelog and the hours ledger. Members can propose features and discuss the work there.
- **Yearly,** a summary of what was built, what it cost, and what it costs to run compared with the systems it replaced.

## 5. Decisions still open

- **Open source.** Whether COPA publishes its code for other type clubs, and under what license, is a separate board decision. Until the board decides, code stays private in COPA's repository and is built so it could be shared later (Principle 9).

## 6. Adoption and amendment

The board adopts this policy by vote, and it becomes the board's policy for COPA-built software. Changes also take a board vote.

The technology lead and the Director of Operations maintain [COPA Technology Standards and Operating Procedures](standards-and-operating-procedures.md), which covers the named technologies, architecture, runbooks and security practices. It changes without a board vote, but it must stay within this policy, and its current version is always available to the board.

Where the Operations Manual's Custom Software Policy says something different, this policy applies to new work, and the manual is updated to match at its next revision.
