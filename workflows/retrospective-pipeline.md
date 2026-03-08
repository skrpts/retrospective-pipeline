---
type: workflow
id: retrospective-pipeline
title: Retrospective Pipeline
description: "Collects feedback, analyses themes, and produces action items"
tags: [Draft]
connections:
  - target: retrospective-facilitation
    type: uses
  - target: decision-documentation
    type: uses
  - target: facilitate-retrospective
    type: uses
  - target: record-decision
    type: uses
  - target: decision-record-writer
    type: uses
---

## Overview

This workflow structures a sprint retrospective from feedback collection through to documented action items and decisions.

## Pipeline Stages

### Stage 1: Feedback Collection

Invoke the **retrospective-facilitation** skill to structure and collect team feedback across the standard retro categories.

### Stage 2: Theme Analysis

Invoke the **facilitate-retrospective** prompt to analyse collected feedback, identify recurring themes, and prioritise improvement areas.

### Stage 3: Decision Recording

Invoke the **decision-documentation** skill to capture any decisions made during the retrospective with full context and rationale.

### Stage 4: Action Item Documentation

Invoke the **decision-record-writer** prompt to produce formal decision records and action items with owners and due dates.

## Output

Retrospective documentation containing:

- Categorised feedback (what went well, what needs improvement)
- Identified themes and patterns
- Prioritised action items with owners
- Decision records with context and rationale
