# Claude Code Agents

This repository contains custom agents for Claude Code, Anthropic's official CLI tool.

## About

Claude Code sub-agents are specialized AI assistants that operate within their own separate context windows to handle specific types of tasks. Each sub-agent is designed with a single, clear responsibility and includes a custom system prompt to guide its behavior.

Key features:

- **Context Separation**: Prevents "context pollution" by giving each agent its own dedicated context
- **Task Specialization**: Designed for specific workflows like code review, debugging, or data analysis
- **Tool Access**: Can be configured with specific tools or inherit all tools from the main thread
- **Proactive Delegation**: Claude Code automatically invokes appropriate sub-agents based on context

## Structure

Sub-agents are defined using Markdown files with YAML frontmatter:

```markdown
---
name: your-sub-agent-name
description: Description of when this sub agent should be invoked
tools: tool1, tool2, tool3  # Optional - inherits all tools if omitted
---

Your sub agent's system prompt goes here with specific instructions,
best practices, and constraints the sub agent should follow.
```

## Storage

Sub-agents can be stored at:

- **Project level**: `.claude/agents/` (takes precedence)
- **User level**: `~/.claude/agents/`

## Usage

Sub-agents are automatically invoked by Claude Code when the context matches their description, or can be explicitly called when needed. They enable more efficient problem-solving by delegating specialized tasks to purpose-built AI assistants.
