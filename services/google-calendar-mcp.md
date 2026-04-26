---
type: service
id: google-calendar-mcp
title: Google Calendar MCP
description: "Google Calendar MCP server for reading a week's calendar activity"
tags: [Production, Calendar]
connections: []
metadata:
  provider: google-calendar
  protocol: mcp
  auth_type: oauth
  env_var: GOOGLE_OAUTH_CREDENTIALS
  required_scopes: [calendar.readonly]
---

## Service Description

Provides access to Google Calendar via MCP. This service fetches a week's calendar events for activity analysis.

## Configuration

### MCP Server Setup

```json
{
  "mcpServers": {
    "google-calendar": {
      "command": "npx",
      "args": ["-y", "google-calendar-mcp"],
      "env": {
        "GOOGLE_OAUTH_CREDENTIALS": "{GOOGLE_OAUTH_CREDENTIALS}"
      }
    }
  }
}
```

## Capabilities Used

- `list-events` — list events within a week-long date range
- `get-event` — get event details for meetings with outcomes to report
