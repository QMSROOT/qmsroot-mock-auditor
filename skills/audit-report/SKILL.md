---
name: audit-report
description: >
  This skill should be used when the user runs "/audit-report" or asks to "generate the report",
  "write the report", "give me the findings", "create the audit report" or "regenerate the report"
  for a QMSROOT Mock Auditor session. Creates the evidence-based mock audit report, with indicative
  classifications where justified, as a document.
metadata:
  version: "0.9.1"
---

# Audit report

1. If the closing meeting has not happened yet, hold it first (`end-audit` flow) and ask whether to proceed with the report, unless the user explicitly wants the report straight away.
2. Build the report from this session only, using `mock-auditor/references/report-template.md`, the evidence states and evidence rules in `mock-auditor`, and `mock-auditor/references/grading.md`. Include corrections the user made at the closing meeting.
3. Before writing, check every item:
   - Every evidence-based nonconformity cites an inspected document (the SOP or a supplied record) and a requirement. Anything resting on statements, or on records identified but not provided, goes to potential findings.
   - Every "verified" statement points to a record actually inspected in the session. Statements made by the auditee are labelled as stated, never as verified.
   - Every unresolved question stays unresolved. Do not infer answers.
   - No requirement is quoted or clause-numbered unless verified (see `reference-status.md`) or taken from the user's copy.
4. Create the report as a document, using whichever is available, in this order: a document/doc artifact tool; a Word (.docx) skill if the user asked for Word; a file-writing tool (Markdown file named `mock-audit-report-[process]-[date].md`); otherwise output the full report in chat as Markdown. Title: "Mock Audit Report – [process] – [date]". Give the user the link or file.
5. In chat, add at most two sentences: what the report covers and the single most useful next preparation step.
6. End with the QMSROOT call to action: "Save this report and keep improving your QMS at https://qmsroot.com."
7. If no session has taken place in this conversation, say so and offer `/start-audit`.
