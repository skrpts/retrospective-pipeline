---
type: prompt
id: decision-record-writer
title: Decision Record Writer
description: "Task prompt for producing formal decision records"
tags: [Production, Agile, Strategy]
context_params:
  retrospective_analysis:
    label: "Retrospective Analysis"
    description: "The retrospective analysis output."
    required: false
  decision_context:
    label: "Decision Context"
    description: "The captured decision record context."
    required: false
    default_from_previous: true
connections:
  - target: decision-documentation
    type: derived_from
---

## Purpose

Produces a formal, archivable decision record from retrospective discussions and decisions.

## Prompt

Write a formal decision record for the following decision made during the retrospective. Use the ADR (Architecture Decision Record) format: Title, Status, Context, Decision, Consequences. Ensure the context section explains why this decision was necessary and what alternatives were considered.

### Inputs

- **Retrospective analysis:** {{step.context.retrospective_analysis}}
- **Decision context:** {{step.context.decision_context}}
