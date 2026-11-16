---
name: start-audit
description: >
  This skill should be used when the user runs "/start-audit" or says "start audit",
  "start a mock audit", "begin the audit" or "new audit". Starts a QMSROOT Mock Auditor
  practice session. Optional arguments: standard, audit type, process, duration and persona,
  e.g. "/start-audit ISO 13485 internal CAPA 20min strict".
metadata:
  version: "0.9.3"
---

# Start audit

1. Load the `mock-auditor` skill and follow it for the whole session.
2. Parse any arguments for standard/mode (ISO 13485, MDSAP + jurisdictions, ISO 9001 + edition, FDA QMSR-style, GMP + regime), audit type (internal, certification, surveillance, transition), process, duration (about 10, 20 or 40 minutes; default 20), and persona (coach, standard, strict).
3. If standard, audit type and process are given, confirm the full scope in one sentence (filling duration and persona with defaults if missing), then go straight to requesting the SOP (with the privacy reminder).
4. If some are missing, run the fast opening from `mock-auditor`, asking only for what is missing: as selectable options (standard, audit type, duration, style) when an interactive question tool is available and the session is not voice; otherwise as one prose message with defaults ("say **go** to use …").
5. If a session is already running or paused in this conversation, ask in one sentence whether to resume it or start fresh.
