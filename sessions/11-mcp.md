# Lesson 11: Model Context Protocol (MCP)

## Overview

MCP stands for **Model Context Protocol**.

It is an open standard that allows Claude Code to connect with external data sources and services.

## Examples

MCP can connect Claude Code with services such as:

- Databases
- GitHub
- Linear
- Documentation servers

This allows Claude to work with information outside the local repository.

## Why MCP Is Useful

Without external integrations, developers may need to:

1. Search an external service.
2. Copy the information.
3. Paste it into Claude Code.
4. Ask Claude to use it.

With MCP, Claude can interact with supported external services directly.

## MCP Commands

MCP servers can be managed using:

```text
claude mcp add