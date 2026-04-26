---
type: service
id: llm-service
title: LLM Service
description: "Language model service for activity analysis, report synthesis, and language polish"
tags: [Production, Tested]
connections: []
metadata:
  serviceType: llm
  auth_type: api_key
---

## LLM Service

This skrpt uses a language model for activity analysis and report generation. The LLM handles theme extraction, accomplishment identification, and report synthesis.

### Configuration

- **Temperature:** 0.3 for analysis, 0.5 for report synthesis
- **Max tokens:** 4,000 for analysis, 8,000 for synthesis (weekly reports tend to be longer)

### Requirements

- A configured LLM provider in skrptiq settings
