# Stakeholder Communications Plan — NovaLend / CBN Deadline

Different audiences need different information at different depths — sharing team morale details with Compliance, or sprint-mechanics jargon with the Head of Digital Factory, wastes their time and buries the thing they actually need to act on. This plan separates content by what each audience can and needs to do with it.

| Audience | Frequency | Format & channel | Content focus |
|---|---|---|---|
| **Engineering Leadership** | Weekly, Friday EOD | Written async update (Slack/email); 10-min live only if status is Red | RAG status, what shipped, blockers that need their help specifically, NovaWallet dependency risk. Not team morale detail — that's handled 1:1 with the Engineering Manager, not in a written update that could be forwarded. |
| **Head of Digital Factory** | End of Sprint 1 and Sprint 2, plus a final pre-submission update (effectively bi-weekly, adapted from "monthly" since the whole engagement is only 6 weeks) | 1-page written summary | Business-impact framing: deadline confidence (%, plain language), scope trade-offs made and why, anything that needs their authority to unblock. No sprint velocity jargon. |
| **Compliance/Risk** | Triggered, not scheduled — immediately on any material change to deadline risk (e.g., NovaWallet slip > 3 days), plus one proactive Week 1 touchpoint to agree review SLA and share the draft report format early | Concise written note, decision-oriented | What CBN needs, what's ready for their review now, and exactly what decision or sign-off is being asked of them. Never sprint mechanics. |

## Why the cadence differs from the brief's literal "monthly"

A calendar-monthly update to the Head of Digital Factory doesn't fit meaningfully inside a 6-week engagement — it would mean exactly one touchpoint before the deadline. Instead, updates are tied to sprint boundaries (functionally every two weeks), which still respects the spirit of "less frequent, more strategic than the weekly engineering update" while actually giving them enough visibility to act if something needs their authority.

## Sample status update — Engineering Leadership, end of Sprint 2

> **Subject: NovaLend / CBN Deadline — Week 4 Status: AMBER**
>
> **Status: Amber.** On track for the Week 6 deadline, but two risks need visibility now rather than in Week 6.
>
> **Shipped this sprint:**
> - Reporting engine and audit trail logic complete, tested against the mocked NovaWallet API.
> - Reconciliation checks passing on all test data sets.
>
> **What's at risk:**
> 1. **NovaWallet API** — still not available in staging as of today (originally committed for start of this sprint). We're continuing development against our mock, so we are not blocked yet, but if it isn't live by Wednesday next week, our final integration and QA window in Sprint 3 shrinks from 2 days to under 1. **Ask: can you help us get a firm commitment date from the NovaWallet EM this week?** We'll escalate through the dependency path in parallel, but a nudge from your level would help.
> 2. **QA capacity** — as planned, QA is on approved leave this sprint. Engineers have taken on peer-review-based testing in the interim per plan; this is on track and not a new risk, just flagging it stays visible.
>
> **What we're protecting no matter what:** core CBN report fields, audit trail integrity, and the Compliance sign-off checkpoint. If the NovaWallet delay continues, the first thing to flex is UX polish on regulator-facing screens, not the report itself.
>
> **Next update:** Friday, end of Sprint 3 Week 1, or sooner if the NovaWallet date changes materially.

This is written so an engineering leader could act on the one concrete ask (a nudge to the NovaWallet EM) without needing a follow-up meeting to understand what's being asked of them.
