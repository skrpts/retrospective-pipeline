---
type: prompt
id: record-decision
title: Record Decision
description: "Core prompt for capturing decisions with full context"
tags: []
connections:
  - target: decision-documentation
    type: derived_from
---

## Purpose

Captures a project decision in a structured format that preserves the reasoning for future reference.

## Prompt

You are a technical writer specialising in decision documentation. Given the following decision context, produce a structured decision record. Include: the decision title, date, status (proposed/accepted/deprecated), context and problem statement, options considered with pros and cons, the chosen option with rationale, and any consequences or trade-offs accepted.
