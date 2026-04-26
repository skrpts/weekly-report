---
type: service
id: gmail-mcp
title: Gmail MCP
description: "Gmail MCP server for reading a week's worth of email activity"
tags: [Production, Email]
connections: []
metadata:
  provider: gmail
  protocol: mcp
  auth_type: oauth
  env_var: GMAIL_OAUTH_CREDENTIALS
  required_scopes: [gmail.readonly]
---

## Service Description

Provides access to Gmail via the Model Context Protocol (MCP). This service fetches a week's email history for activity analysis and report generation.

## Configuration

### MCP Server Setup

```json
{
  "mcpServers": {
    "gmail": {
      "command": "npx",
      "args": ["-y", "gmail-mcp-server"],
      "env": {
        "GMAIL_OAUTH_CREDENTIALS": "{GMAIL_OAUTH_CREDENTIALS}"
      }
    }
  }
}
```

## Capabilities Used

- `search_emails` — search emails with date range queries (e.g. `after:2026/04/20 before:2026/04/27`)
- `read_email` — read email content for activity analysis
