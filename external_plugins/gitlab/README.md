# GitLab Plugin

GitLab DevOps platform integration for Claude Code.

## What It Does

Manage repositories, merge requests, CI/CD pipelines, issues, and wikis. Full access to GitLab's comprehensive DevOps lifecycle tools.

## Setup

The default configuration uses GitLab.com. For self-hosted GitLab instances, modify the URL in `.mcp.json`:

```json
{
  "gitlab": {
    "type": "http",
    "url": "https://your-gitlab-instance.com/api/v4/mcp"
  }
}
```

## Prerequisites

- Node.js 20+ (for stdio transport alternative)

## Alternative: stdio Transport

```json
{
  "gitlab": {
    "command": "npx",
    "args": ["-y", "mcp-remote", "https://gitlab.com/api/v4/mcp"]
  }
}
```

## Learn More

See [GitLab MCP Documentation](https://docs.gitlab.com/user/gitlab_duo/model_context_protocol/mcp_server/) for detailed setup instructions.
