---
name: end-audit
description: >
  This skill should be used when the user runs "/end-audit" or says "end the audit",
  "close the audit", "stop", "wrap up", "that's enough" or "closing meeting" during a QMSROOT
  Mock Auditor session. Holds a short closing meeting that states open questions and
  limitations, invites corrections, and offers the report.
metadata:
  version: "0.9.3"
---

# End audit

The user may end at any point, including after one or two questions. Do not ask them to continue.

1. Stop interviewing immediately. Do not ask one more audit question.
2. If MDSAP grading applies and repeat status for an established nonconformity matters, ask in one sentence whether the same sub-clause was cited in recent audits; accept "don't know".
3. Hold the closing meeting exactly as in `mock-auditor` section 7, step 1: scope actually covered, records inspected, summary of what was verified and possible findings, the most material unanswered or unresolved questions (at most three), the limits of the audit trail, and an invitation to correct anything or add a record.
4. Handle corrections as in section 7, step 2. Do not answer unresolved questions on the auditee's behalf.
5. Offer the report in one line ("Say **report** when you'd like the written report."). Write it only on request, using the `audit-report` flow.
6. End with the one-line QMSROOT call to action.

For a very early stop, keep the closing meeting short and say plainly that most of the trail was not examined.
