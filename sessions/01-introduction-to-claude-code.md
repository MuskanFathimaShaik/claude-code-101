# Lesson 1: Introduction to Claude Code

## Overview

Claude Code is an agentic command-line tool that works directly inside the local development environment.

Unlike a traditional AI chat interface, Claude Code can interact with the project's:

- Files
- File system
- Terminal
- Commands
- Development tools

This allows Claude to work with the actual codebase instead of relying on manually copied code or error messages.

## Key Learnings

### 1. Agentic Development

Claude Code can inspect the project, understand its structure, execute commands, and make changes.

The important difference is that the AI can take actions within the development environment rather than only providing suggestions through a chat interface.

### 2. Working With the Actual Codebase

Instead of manually copying files into an AI chat, Claude can navigate the repository and locate the relevant files itself.

This gives Claude access to the surrounding project context needed to understand a task.

### 3. Co-Developer Mindset

The main mindset shift is:

**From Chat Assistant → Co-Developer**

Instead of treating AI as an external Q&A tool, treat it as a developer working alongside you in the terminal.

## Prompting Shift

### Old Approach

> How do I fix this JavaScript error: [paste error log]?

The developer manually provides the error and waits for a suggested solution.

### New Approach

> Run `npm test`, read the error logs, and inspect the codebase to see what breaks.

Claude can investigate the problem directly.

## Main Takeaway

Claude Code is most useful when it can interact with the actual development environment rather than being used only as a chat-based coding assistant.