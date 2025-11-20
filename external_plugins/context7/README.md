# Context7 Plugin

Upstash Context7 MCP server for Claude Code.

## What It Does

Pull up-to-date, version-specific documentation and code examples directly from source repositories into your LLM context. Add "use context7" to prompts to fetch relevant documentation.

## Prerequisites

- Node.js >= v18.0.0

## Optional: API Key for Higher Rate Limits

For higher rate limits and private repository access, get an API key and configure:

```json
{
  "context7": {
    "command": "npx",
    "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
  }
}
```

Or use the remote server:
```json
{
  "context7": {
    "type": "http",
    "url": "https://mcp.context7.com/mcp",
    "headers": {
      "Authorization": "Bearer YOUR_API_KEY"
    }
  }
}
```

## Learn More

See [Context7 GitHub](https://github.com/upstash/context7) for detailed documentation.
