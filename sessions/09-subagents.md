# Lesson 9: Subagents

## Overview

Subagents are specialized AI assistants that can be spawned by Claude Code to handle separate tasks.

They operate using their own isolated context windows, allowing them to perform research, searching, or other tasks without filling the main conversation's context.

## Key Takeaway

Subagents can run in parallel with the main agent and use their own context.

They are useful for:

- Heavy research
- Searching large codebases
- Multi-step exploration
- Isolated checks
- Tasks where only the final result or summary is needed

The main agent receives the useful result without having to keep the entire exploration process in its context.

## Why Use Subagents?

When Claude needs to read many files to answer a relatively simple question, every file read and tool call can consume the main context window.

For example:

> Find every file using the old API endpoint and summarize them for me.

If the main agent performs the entire search, the conversation can become filled with:

- Search results
- File contents
- Tool calls
- Intermediate findings

A subagent can perform this exploration separately and return only the relevant result.

## How Subagents Help

A subagent handles the **journey**, while the main agent receives the **result**.

### Main Agent

```text
Give task
    ↓
Delegate exploration
    ↓
Receive concise result
    ↓
Continue main task