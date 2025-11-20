# GitHub Plugin

Official GitHub MCP server for Claude Code.

## What It Does

Create issues, manage pull requests, review code, search repositories, and interact with GitHub's full API directly from Claude Code.

## Setup

1. Create a GitHub Personal Access Token with appropriate scopes
2. Set the environment variable:
   ```bash
   export GITHUB_PERSONAL_ACCESS_TOKEN=your-token-here
   ```

## Required Environment Variables

- `GITHUB_PERSONAL_ACCESS_TOKEN` - Your GitHub PAT with appropriate scopes

## Alternative: Docker Setup

For local server deployment:
```json
{
  "github": {
    "command": "docker",
    "args": ["run", "-i", "--rm", "-e", "GITHUB_PERSONAL_ACCESS_TOKEN", "ghcr.io/github/github-mcp-server"],
    "env": {
      "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_PERSONAL_ACCESS_TOKEN}"
    }
  }
}
```

## Learn More

See [GitHub MCP Server](https://github.com/github/github-mcp-server) for detailed documentation.
