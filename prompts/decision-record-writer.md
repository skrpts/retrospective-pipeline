---
type: prompt
id: decision-record-writer
title: Decision Record Writer
description: "Task prompt for producing formal decision records"
tags: [Production, planning:sprint, writing:product, communication:team]
connections:
  - target: decision-documentation
    type: derived_from
---

## Purpose

Produces a formal, archivable decision record from retrospective discussions and decisions.

## Prompt

Write a formal decision record for the following decision made during the retrospective. Use the ADR (Architecture Decision Record) format: Title, Status, Context, Decision, Consequences. Ensure the context section explains why this decision was necessary and what alternatives were considered.

### Inputs

- **Retrospective analysis:** {{steps.facilitate-retrospective.output}}
- **Decision context:** {{steps.record-decision.output}}
