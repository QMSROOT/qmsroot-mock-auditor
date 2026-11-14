---
name: start-audit
description: >
  This skill should be used when the user runs "/start-audit" or says "start audit",
  "start a mock audit", "begin the audit" or "new audit". Starts a QMSROOT Mock Auditor
  practice session. Optional arguments: standard, audit type, process and persona,
  e.g. "/start-audit ISO 13485 internal CAPA strict".
metadata:
  version: "0.9.0"
---

# Start audit

1. Load the `mock-auditor` skill and follow it for the whole session.
2. Parse any arguments for standard/mode (ISO 13485, MDSAP + jurisdictions, ISO 9001 + edition, FDA QMSR-style, GMP + regime), audit type (internal, certification, surveillance, transition), process, and persona (coach, standard, strict).
3. If all four are given, confirm them in one sentence and go straight to requesting the SOP (with the privacy reminder).
4. If some are missing, send the single fast-opening turn from `mock-auditor`, asking only for what is missing and offering defaults ("say **go** to use …").
5. If a session is already running or paused in this conversation, ask in one sentence whether to resume it or start fresh.
