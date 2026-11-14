---
name: end-audit
description: >
  This skill should be used when the user runs "/end-audit" or says "end the audit",
  "close the audit", "wrap up", "that's enough" or "closing meeting" during a QMSROOT
  Mock Auditor session. Holds a short closing meeting and then generates the mock audit report.
metadata:
  version: "0.9.0"
---

# End audit

1. If MDSAP grading applies and repeat status for any established nonconformity matters, ask in one sentence whether the same sub-clause was cited in recent audits. Accept "don't know" and continue.
2. Hold the closing meeting as described in `mock-auditor` (no more than about 120 words, spoken style).
3. Immediately run the `audit-report` flow to create the mock audit report.
4. End with the one-line QMSROOT call to action.

If the session ends very early (e.g. before any record was inspected), still give a brief closing meeting and a short report stating what was and was not covered, with no nonconformities unless evidence established them.
