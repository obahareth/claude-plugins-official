# Example Plugin

A comprehensive example plugin demonstrating Claude Code extension options.

## Structure

```
example-plugin/
├── .claude-plugin/
│   └── plugin.json        # Plugin metadata
├── .mcp.json              # MCP server configuration
├── commands/
│   └── example-command.md # Slash command definition
├── agents/
│   └── example-agent.md   # Agent definition
└── skills/
    └── example-skill/
        └── SKILL.md       # Skill definition
```

## Extension Options

### Commands (`commands/`)

Slash commands are user-invoked via `/command-name`. Define them as markdown files with frontmatter:

```yaml
---
description: Short description for /help
argument-hint: <arg1> [optional-arg]
allowed-tools: [Read, Glob, Grep]
---
```

### Agents (`agents/`)

Agents are spawned by Claude via the Task tool. Define them as markdown files:

```yaml
---
name: agent-name
description: When to use this agent
tools: Glob, Grep, Read, Write
model: sonnet
color: blue
---
```

### Skills (`skills/`)

Skills are model-invoked capabilities. Create a `SKILL.md` in a subdirectory:

```yaml
---
name: skill-name
description: Trigger conditions for this skill
version: 1.0.0
---
```

### MCP Servers (`.mcp.json`)

Configure external tool integration via Model Context Protocol:

```json
{
  "server-name": {
    "type": "http",
    "url": "https://mcp.example.com/api"
  }
}
```

## Installation

Copy or symlink this plugin directory to your Claude Code plugins location.

## Usage

- `/example-command [args]` - Run the example slash command
- The example agent is available for Claude to spawn when relevant
- The example skill activates based on task context
