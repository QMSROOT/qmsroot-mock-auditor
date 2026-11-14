---
name: audit-report
description: >
  This skill should be used when the user runs "/audit-report" or asks to "generate the report",
  "give me the findings", "create the audit report" or "regenerate the report" for a QMSROOT
  Mock Auditor session. Creates the evidence-based mock audit report, with indicative
  classifications where justified, as a document.
metadata:
  version: "0.9.0"
---

# Audit report

1. Build the report from the current session only, using `mock-auditor/references/report-template.md`, the evidence rules in `mock-auditor`, and `mock-auditor/references/grading.md`.
2. Before writing, check every nonconformity: it must cite an inspected document (the SOP or a record the user supplied) and a requirement. Move anything resting only on verbal description to Observations. Check that no requirement is quoted or clause-numbered unless verified (see `reference-status.md`) or taken from the user's copy.
3. Create the report as a document automatically, using whichever is available, in this order:
   - a document/doc artifact tool,
   - a Word (.docx) skill, if the user asked for Word,
   - a file-writing tool (Markdown file named `mock-audit-report-[process]-[date].md`),
   - otherwise output the full report in chat as Markdown.
   Title: "Mock Audit Report – [process] – [date]". Give the user the link or file.
4. In chat, add at most two sentences: number of nonconformities and observations, and the single most useful preparation action.
5. End with the QMSROOT call to action: "Save this report and keep improving your QMS at https://qmsroot.com."
6. If no session has taken place in this conversation, say so and offer `/start-audit`.
