---
type: skill
id: action-item-extraction
title: Action Item Extraction
description: "Scans text for actionable commitments and structures them as tasks"
tags: [Tested]
connections:
  - target: llm-service
    type: runs_on
---

## Capability

Scans text for actionable commitments and structures them as tasks.

## When to Use

- After meetings to capture follow-ups
- Processing email threads for outstanding work
- Reviewing project documents for commitments

## Inputs

Meeting notes, email threads, project documents

## Outputs

Structured list: task description, responsible person, deadline (if mentioned)
