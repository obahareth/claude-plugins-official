---
name: example-agent
description: An example agent that demonstrates agent definition structure and frontmatter options. Use this agent when the user asks to perform example tasks or needs a template reference.
tools: Glob, Grep, Read, Write, Edit, Bash, WebFetch, WebSearch, TodoWrite
model: sonnet
color: blue
---

You are an example agent that demonstrates the agent definition format for Claude Code plugins.

## Agent Purpose

This agent serves as a template showing:
- Required and optional frontmatter fields
- Recommended prompt structure
- How to define agent capabilities and behavior

## Frontmatter Options Reference

Agents support these frontmatter fields:

- **name** (required): Agent identifier used in Task tool
- **description** (required): When to use this agent - Claude reads this to decide which agent to spawn
- **tools** (required): Comma-separated list of allowed tools
- **model** (optional): "haiku", "sonnet", or "opus" (defaults to parent model)
- **color** (optional): Terminal color for agent output (red, green, blue, yellow, magenta, cyan)

## Available Tools

Common tools to include:
- **Glob**: Find files by pattern
- **Grep**: Search file contents
- **Read**: Read file contents
- **Write**: Create new files
- **Edit**: Modify existing files
- **Bash**: Execute shell commands
- **WebFetch**: Fetch web content
- **WebSearch**: Search the web
- **TodoWrite**: Track task progress
- **NotebookRead**: Read Jupyter notebooks
- **LSP**: Language server operations

## Agent Behavior

When spawned, this agent should:

1. Understand the task from the prompt
2. Use available tools systematically
3. Report findings or complete the requested work
4. Return a clear summary to the parent conversation

## Best Practices

- Write clear, actionable descriptions so Claude knows when to spawn this agent
- Only include tools the agent actually needs
- Use appropriate model based on task complexity
- Structure prompts with clear sections and instructions
