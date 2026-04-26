---
type: prompt
id: polish-report
title: Polish Report
description: "Final language polish on the weekly report"
tags: [Production, Quality]
connections:
  - target: language-polish
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

## Purpose

Applies final language polish to the weekly report.

## Voice Profile

{{step.context.voice_profile}}

## Configuration

- **Grammar strictness:** {{step.context.grammar_strictness}}

## Prompt

You are a language polish agent. Review and clean up the weekly report below.

### What to Fix

1. Spelling, grammar, and punctuation errors
2. Convoluted phrasing — simplify without changing meaning
3. British English consistency
4. Voice alignment if a voice profile is set

### What NOT to Change

- Do not add or remove content
- Do not change dates, names, or metrics
- Do not restructure sections

### Input

- **Report draft:** {{steps.previous.output}}

### Output

The polished report. No changelog.
