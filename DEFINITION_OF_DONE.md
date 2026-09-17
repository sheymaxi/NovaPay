# Definition of Done — Regulator-Facing Deliverable (CBN Report)

A standard engineering DoD ("code reviewed, tests pass, merged to main") is not sufficient for anything feeding the CBN submission. This DoD applies specifically to the NovaLend regulatory reporting path for this 6-week engagement.

A regulator-facing story is **not done** until all of the following are true:

* Code reviewed and merged, with tests passing against the **real** NovaWallet API in staging (not just the mock) at least once before the freeze.
* Data lineage documented end-to-end: every field in the CBN report traced from its source system through each transformation to the final report field.
* Audit trail is immutable and timestamped — no report-relevant data can be silently overwritten without a logged record.
* Reconciliation check run with **zero unexplained variance** — any variance is either resolved or explicitly documented with a reason.
* Report format validated against the actual CBN submission template/schema, not an internal approximation of it.
* Compliance/Risk sign-off obtained and recorded in writing — a verbal "looks fine" does not close this item.
* Access controls verified: only the intended roles can view or export regulator-facing data.
* Rollback plan documented in case an issue is found post-submission.
* A submission-day runbook exists and has been handed to whoever executes the actual CBN filing.



Anything that doesn't meet every item above stays in progress.

