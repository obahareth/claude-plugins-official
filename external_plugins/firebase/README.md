# Firebase Plugin

Google Firebase MCP integration for Claude Code.

## What It Does

Manage Firestore databases, authentication, cloud functions, hosting, and storage. Build and manage your Firebase backend directly from your development workflow.

## Prerequisites

- Node.js installed
- Firebase CLI credentials (logged in via `firebase login` or Application Default Credentials)

## Optional Configuration

Add arguments to customize behavior:
- `--dir ABSOLUTE_DIR_PATH` - Set project context directory
- `--only FEATURE_1,FEATURE_2` - Limit exposed tools (comma-separated)

Example with options:
```json
{
  "firebase": {
    "command": "npx",
    "args": ["-y", "firebase-tools@latest", "mcp", "--dir", "/path/to/project", "--only", "auth,firestore"]
  }
}
```

## Learn More

See [Firebase MCP Documentation](https://firebase.google.com/docs/ai-assistance/mcp-server) for detailed setup instructions.
