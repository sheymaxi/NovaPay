NovaLend Scrum Master Ops Kit
Prepared for: FirstBank Digital Factory — Scrum Master take-home task
Scenario: NovaLend squad, CBN regulatory reporting deadline in 6 weeks
What's here
File	Artifact
`01-six-week-plan.md`	Sprint/program plan to the CBN deadline, ceremony cadence, capacity accounting, explicit cut/protect list
`capacity_chart.png`	Visual capacity plan referenced in the six-week plan (stretch goal)
`02-raid-log.md`	RAID log — 11 entries, each with owner, mitigation, severity
`03-retro-facilitation-plan.md`	Retro format and questions for a low-morale team that missed two sprints
`04-stakeholder-comms-plan.md`	Reporting cadence to Engineering Leadership, Head of Digital Factory, and Compliance/Risk, plus one fully written sample update
`05-ceremony-redesign.md`	Standup/planning/retro redesign for the remote contractor (5 hrs behind Lagos), with a walked-through concrete day
`06-dependency-map.md`	Mermaid dependency map for the NovaWallet API dependency, with escalation path
`DEFINITION_OF_DONE.md`	Tightened DoD for a regulator-facing deliverable (stretch goal)
`ESCALATION_SCRIPT.md`	Exact escalation script for the NovaWallet dependency risk (stretch goal)
`AI_USAGE.md`	Tools used, prompts, and a documented case of catching/fixing generic AI output
Assumptions made (brief left these open — documenting per Section 4 instructions)
Because the brief intentionally leaves some specifics open, the following assumptions were made and are used consistently across every artifact. These are flagged explicitly to the panel as assumptions to confirm on Day 1, not facts.
Sprint cadence: Three 2-week sprints (Weeks 1–2, 3–4, 5–6). A shorter 1-week cadence was considered to force faster feedback after two missed sprints, but rejected — a team with low morale and a hard deadline needs sprint boundaries stable enough to rebuild trust in the process itself, not more churn.
Squad composition: 2 backend + 2 frontend engineers, 1 QA engineer, 1 product designer, 1 Product Owner (7 delivery members), plus the incoming Scrum Master (facilitation only, not counted in delivery capacity). The remote contractor is one of the four engineers.
Remote contractor's timezone: 5 hours behind Lagos (WAT, UTC+1) — treated as equivalent to US Eastern-adjacent hours for scheduling purposes. Overlap window used throughout: 2:00–4:00pm Lagos / 9:00–11:00am contractor time.
Public holiday: Nigeria's Independence Day (1 October), landing in Week 5–6 of the plan. To be confirmed against the actual 2026 calendar in Week 1.
Approved leave: QA engineer, 5 working days, placed in Sprint 2 (Weeks 3–4). This is the assumption most worth stress-testing early, since QA leave colliding with a compressed testing window is one of the plan's biggest risks (see RAID R3).
CBN deadline date: Treated as immovable per the brief; Friday of Week 6 is the hard submission date, with the last 2 working days reserved as a freeze/UAT/sign-off buffer rather than new-feature time.
How to read this kit
Start with `01-six-week-plan.md` for the overall shape, then `02-raid-log.md` for what could go wrong, then the three facilitation/comms/ceremony documents for how day-to-day execution actually works. `06-dependency-map.md` and `ESCALATION_SCRIPT.md` pair together for the NovaWallet risk specifically.
