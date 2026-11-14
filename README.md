# QMSROOT Mock Auditor

Practise the audit before it matters. A voice- and text-friendly mock auditor for quality professionals, free to use.

**Status: version 0.9.2 (pilot).** Feedback welcome via https://qmsroot.com.

## What it does
- **Fast start:** one setup turn with tick-box options for standard, audit type, duration and style where your Claude app supports them (a short prose question otherwise, e.g. in voice), or just say "go" for defaults (ISO 13485, internal audit, internal audit process, 20 minutes, standard auditor). The auditor confirms the scope before the first question.
- **Your own procedure:** asks you to upload your SOP, questions you on what it actually says, and compares it with the standard.
- **Evidence sampling:** asks for records (schedules, reports, CAPA links, competence records) and follows audit trails like a real auditor.
- **Follows your evidence trail:** each question builds on what you actually said and showed. A plausible answer is treated as a claim until a record supports it.
- **Clear evidence states:** separates what was verified from an inspected record, what you stated, records identified but not provided, and questions left unresolved.
- **Scope discipline:** asks before extending into another process.
- **One short question at a time:** built for live and voice practice.
- **Personas:** coach, standard or strict auditor.
- **Modes:** ISO 13485, MDSAP (by jurisdiction), ISO 9001 (edition as you state it), FDA QMSR-style inspection, GMP (by regime).
- **Close-out on your terms:** end at any time. The closing meeting names the open questions and the limits of the trail and invites corrections; then, when you ask, you get an evidence-based mock audit report with indicative classifications where justified, potential observations, coaching, and the evidence requests and unresolved questions.
- **Source discipline:** quotes requirements only from your own copy of the standard or verified references; everything else is marked as paraphrase.
- **Privacy prompts:** reminds you to anonymise names, suppliers and patient data before every upload.

## Installation

### Claude (web, desktop and Cowork)
- **From the Claude directory (once listed):** open **Customize → Plugins → Discover**, search for "QMSROOT Mock Auditor" and add it.
- **Before it is listed:** download this repository as a ZIP (green **Code** button → **Download ZIP**), then in Claude open **Customize → Plugins**, choose to add or upload a plugin, and select the ZIP. Upload options depend on your plan and organisation settings.

### Claude Code
Add the QMSROOT marketplace and install the plugin from your terminal:

```bash
claude plugin marketplace add malikaamirde-lang/qmsroot-mock-auditor
claude plugin install qmsroot-mock-auditor@qmsroot
```

Or in one step inside a Claude Code session (Claude Code v2.1.275 or later):

```
/plugin install qmsroot-mock-auditor --marketplace malikaamirde-lang/qmsroot-mock-auditor
```

To update later: `claude plugin update qmsroot-mock-auditor@qmsroot`.

### Check it works
Start a new conversation and type `/start-audit` or "audit me". The auditor should welcome you and ask, in one message, which standard, audit type, process and auditor style you want.

If you previously uploaded an older standalone "mock-auditor" skill, turn it off under **Customize → Skills** so this version is used.

## Commands
| Command | What it does |
|---|---|
| `/start-audit [standard] [type] [process] [duration] [persona]` | Start a session, e.g. `/start-audit MDSAP US,CA surveillance complaints 20min strict` |
| `/pause-audit` | Pause, ask questions outside the interview, then resume |
| `/end-audit` | End now: closing meeting with open questions, then corrections |
| `/audit-report` | Write (or rewrite) the mock audit report |

Natural language works too: "audit me on CAPA", "pause", "end the audit".

## What the plugin runs and sends
The plugin contains only instructions and reference text. It runs no scripts, installs no packages, connects to no external services and sends no data anywhere. Documents you upload are handled by Claude like any other conversation content. The report is created with whatever document tool your Claude session already has (a Claude doc, a Word file or a Markdown file), or shown in the chat.

## Limitations
- Educational practice only. Not an audit, certification decision or regulatory advice. Classifications in the report are indicative and do not predict any auditing organisation's or regulator's decision.
- Professional validation of the methodology is pending.
- Many framework facts (editions, dates, timelines) are deliberately marked unverified; see `skills/mock-auditor/references/reference-status.md`.
- Anonymise everything you share. Your organisation's AI policy applies.

## Licence
QMSROOT Mock Auditor is © 2026 MAXCERT LTD, trading as QMSROOT, and free to use under the **QMSROOT Free-Use Licence** (see [LICENSE.md](LICENSE.md)). In short:

- **You may** install and use it for free, as an individual, employee, auditor, consultant or commercial organisation, including for internal training and professional audit preparation. You may use it while delivering your own paid consulting or training, and use the reports you create however you like.
- **You may not** sell it, rebrand it, hand it out as part of a paid product, course or service, or publish modified versions without written permission from QMSROOT. Point people to this repository or the Claude directory instead.
- **QMSROOT keeps** its copyright and branding; notices and links must stay intact.
- **Educational tool only:** it is not a certification, audit or regulatory-compliance guarantee.
- **Separately licensed:** the QMSROOT platform, backend intelligence and integrations (including any future QMSROOT connector) are not covered by this licence.

The summary is for convenience; [LICENSE.md](LICENSE.md) governs. For permissions or partnerships, contact QMSROOT via https://qmsroot.com.

## Roadmap
- QMSROOT connector (MCP): pull SOPs and records from QMSROOT directly, and push mock audit reports back. Not included in this version.

## Contents
```
.claude-plugin/plugin.json       plugin manifest
.claude-plugin/marketplace.json  lets Claude Code install from this repository
skills/mock-auditor/             core auditor behaviour + references
skills/start-audit/              /start-audit
skills/pause-audit/              /pause-audit
skills/end-audit/                /end-audit
skills/audit-report/             /audit-report
LICENSE.md                       QMSROOT Free-Use Licence
```

---
More at https://qmsroot.com
