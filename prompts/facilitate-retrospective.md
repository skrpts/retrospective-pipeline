---
type: prompt
id: facilitate-retrospective
title: Facilitate Retrospective
description: "Core prompt for structuring and analysing retrospective feedback"
tags: [Production, Agile, Communication]
inputs:
  team_feedback:
    label: "Team Feedback"
    description: "Feedback collected from the team"
    example: "Retro notes, survey results, or 1:1 feedback themes"
    required: true
    type: text
  sprint_name:
    label: "Sprint Name"
    description: "Name or identifier for the sprint"
    example: "Sprint 14 — Auth Hardening"
    required: true
    type: text
connections:
  - target: retrospective-facilitation
    type: derived_from
---

## Purpose

Analyses raw retrospective feedback to identify themes, patterns, and actionable improvements.

## Prompt

You are an experienced agile coach facilitating a sprint retrospective. Given the following team feedback, categorise items into "what went well", "what needs improvement", and "ideas for next sprint". Identify recurring themes across feedback items, highlight the top 3 improvement areas by frequency and impact, and suggest specific, measurable action items for each.

### Inputs

{{input.team_feedback}}

Sprint: {{input.sprint_name}}
