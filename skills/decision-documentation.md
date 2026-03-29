---
type: skill
id: decision-documentation
title: Decision Documentation
description: "Captures decisions with context, alternatives considered, and rationale"
tags: [Production, planning:sprint, communication:team]
connections:
  - target: llm-service
    type: runs_on
  - target: decision-record-template
    type: references
---

## Capability

Records project decisions in a structured format that captures the context, alternatives evaluated, rationale for the chosen option, and any consequences or trade-offs accepted.

## When to Use

- Architecture or design decisions
- Process changes agreed in retrospectives
- Scope or priority decisions
- Tool or technology selections

## Inputs

Decision context, alternatives considered, evaluation criteria, chosen option

## Outputs

Structured decision record with context, options analysis, rationale, and consequences
