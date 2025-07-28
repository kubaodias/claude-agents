# Claude Code Agents

This repository contains custom Claude Code sub-agents.

## About

This is a personal collection of specialized Claude Code sub-agents designed for my development workflows. For detailed information about Claude Code sub-agents, see the [official Anthropic documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents).

## Storage

Sub-agents can be stored at:

- **Project level**: `.claude/agents/` (takes precedence)
- **User level**: `~/.claude/agents/`

## Usage

Sub-agents are automatically invoked by Claude Code when the context matches their description, or can be explicitly called when needed.
