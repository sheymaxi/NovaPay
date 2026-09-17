# AI Usage

**Tool used:** Claude (Anthropic), used conversationally to draft, structure, and stress-test all six required artifacts plus the stretch goals, working from the take-home brief directly.

## What I used it for
- First-pass drafting of each artifact's structure, so I could spend my review time on whether the *content* was situationally correct rather than on formatting.
- Generating the Mermaid dependency diagram syntax.
- Generating a capacity chart from numbers I specified (nominal days, leave, holiday, freeze buffer).

## Concrete prompts and what came back

**Prompt 1:** "Draft a 6-week Scrum Master plan for a fintech squad facing a hard regulatory deadline."
**What came back:** A generic three-sprint plan with a standard cadence, no explicit accounting for the public holiday or the approved leave, and no stated trade-off reasoning — it treated the 6 weeks as fully available capacity. **This is exactly the failure mode the brief warns about** — a plan that's aspirational rather than realistic because it quietly ignores the constraints. I caught it by checking the draft against the brief's specific requirement for "capacity accounting for one public holiday and one team member's already-approved leave" and noticed neither was mentioned. I fixed it by explicitly forcing the math: nominal person-days per sprint, minus leave, minus holiday, minus a reserved freeze/UAT buffer in the final sprint — which is what produced the capacity table and chart in the final plan.

**Prompt 2:** "Write a weekly stakeholder update for engineering leadership on this project."
**What came back:** A draft that included a line reading roughly "team morale remains a concern following the two missed sprints." That's true and worth tracking, but it's the wrong level of detail for a written weekly update to engineering leadership — it's the kind of thing that gets forwarded, read out of context, or ends up somewhere it shouldn't (like in front of Compliance, who need something entirely different). I rewrote the update to keep it focused on delivery status, the one concrete NovaWallet risk, and a specific ask, and moved morale entirely into the 1:1 channel with the Engineering Manager, which I made explicit in the comms plan itself so the reasoning is documented, not just applied silently.

**Prompt 3:** "Generate a RAID log for this scenario, at least 8 entries."
**What came back:** A first pass with generic project-management entries — "risk: scope creep," "risk: technical debt," "assumption: requirements are stable" — that could have applied to almost any project and didn't reference the squad, the timezone gap, or the NovaWallet dependency named in the brief. I rejected that draft outright and re-prompted asking for every entry to trace back to a specific fact stated in the brief, then manually checked each of the 11 final entries against the scenario text to confirm none of them were generic filler.

## Judgment applied throughout
The pattern across all three cases was the same: AI output defaults toward generically "correct" project-management content unless explicitly forced to engage with the specific constraints in the brief (the deadline being immovable, the exact leave/holiday, who reads which update). My job was checking every artifact against the scenario's actual facts before accepting it, not just accepting fluent-sounding output.
