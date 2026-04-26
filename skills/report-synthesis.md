---
type: skill
id: report-synthesis
title: Report Synthesis
description: "Produces a stakeholder-ready weekly report from the activity analysis"
tags: [Production, Quality]
connections:
  - target: llm-service
    type: runs_on
context_params:
  voice_profile:
    label: "Voice Profile"
    description: "Your writing style for the report — tone and formality"
    required: false
  report_format:
    label: "Report Format"
    description: "How to structure the report — Bullet Points, Narrative, or Formal"
    default: "Bullet Points"
    required: false
  report_audience:
    label: "Report Audience"
    description: "Who will read this — Team, Manager, or Executive"
    default: "Manager"
    required: false
---

## Capability

Takes the activity analysis and produces a formatted weekly report tailored to the target audience and format.

## What It Does

1. **Summary** — one-paragraph overview of the week
2. **Accomplishments** — what was completed, shipped, or decided
3. **In progress** — what's being worked on and expected completion
4. **Blockers** — what's stuck and what's needed to unblock
5. **Next week** — planned focus areas and upcoming deadlines
6. **Metrics** — meetings attended, emails processed, key conversations

## Report Format

- **Bullet Points** — each section as a bulleted list. Fast to read, easy to scan. The default.
- **Narrative** — flowing prose with paragraph breaks. Better for context-heavy reports.
- **Formal** — numbered sections with headers, suitable for executive review or archiving.

## Report Audience

- **Team** — detailed, includes specifics. Assumes context.
- **Manager** — balanced, highlights outcomes and blockers. The default.
- **Executive** — high-level, focuses on impact and risks. Omits tactical detail.

## Outputs

Formatted weekly report in markdown.
