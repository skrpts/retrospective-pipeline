---
type: prompt
id: extract-action-items
title: Extract Action Items
description: "Core prompt for identifying and structuring action items from text"
tags: [Production]
connections:
  - target: action-item-extraction
    type: derived_from
---

## Purpose

Extracts actionable commitments from unstructured text and formats them as a structured task list.

## Prompt

Analyse the following text and extract all action items. For each, identify: the task, who is responsible, and any deadline mentioned.
