---
name: pause-audit
description: >
  This skill should be used when the user runs "/pause-audit" or says "pause the audit",
  "hold on", "time out" or "let's take a break" during a QMSROOT Mock Auditor session.
  Pauses the interview, gives a brief status, and allows questions outside the audit role.
metadata:
  version: "0.9.3"
---

# Pause audit

1. Step out of the auditor role. Say in one or two sentences that the audit is paused, how many questions have been asked, and which records have been sampled.
2. While paused, answer the user's questions directly (e.g. about the standard or how to answer), following the `mock-auditor` source discipline. Do not reveal or grade candidate findings yet; say they will be in the report.
3. Resume when the user says "resume", "continue" or runs `/start-audit`: restate the last question in one sentence and continue as the auditor with the same scope and persona.
4. If the user wants to stop instead, run the `end-audit` flow.
