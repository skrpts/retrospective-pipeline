---
type: skill
id: decision-record-composition
title: Decision Record Writer
description: "Composing formal, archivable decision records in ADR format from the retrospective analysis and captured decisions"
tags: [Production, Agile, Documentation]
connections:
  - target: llm-service
    type: runs_on
  - target: decision-record-template
    type: references
---

## Decision Record Writer

This skill turns the retrospective analysis and the captured decision context into a formal, archivable decision record following the ADR (Architecture Decision Record) format.

### Core Capability

Given the retrospective themes and the structured decision context from earlier stages, this skill writes a clean, self-contained decision record: Title, Status, Context, Decision, and Consequences. It grounds the Context section in why the decision was necessary and which alternatives were weighed, so the record stands on its own for future readers.

### Method

1. **Ground the context:** Draw on the retrospective analysis to explain the problem the decision addresses and the forces at play.
2. **State the decision:** Record the chosen option plainly, with the rationale and the alternatives that were considered.
3. **Trace the consequences:** Capture the trade-offs accepted and any follow-on actions or risks.

### Output Structure

A single decision record in ADR format (Title, Status, Context, Decision, Consequences), ready to archive alongside the retrospective. This is the terminal deliverable, handed to the language-polish stage for final presentation.
