# Lesson 6: Context Management Deep Dive

## Overview

Context is Claude's working memory during a session.

It includes information such as:

- Files Claude has read
- Commands Claude has executed
- Tool results
- Conversation history

Because context is finite, it needs to be actively managed.

## Important Commands

### `/context`

Used to check the current context usage.

This helps understand how much of the available context is being consumed.

### `/compact`

Summarizes the existing session to reduce context usage while retaining important information.

Useful during long development sessions.

### `/clear`

Clears the current conversation context.

Useful when starting a completely different task.

## Why Context Management Matters

When context becomes too large:

- Important information can become harder to maintain
- Irrelevant information can remain in the conversation
- Claude may become less focused
- Token usage can increase

## Prompting Shift

### Less Effective

> Find where auth is and fix it.

This can cause unnecessary exploration across the repository.

### More Effective

> Check `src/auth/login.ts` around line 40 and identify the cause of the login issue.

A focused request reduces unnecessary exploration.

## Subagents and Context

Subagents can be used for isolated exploration or research.

Instead of filling the main conversation with every file and tool result, a subagent can perform the exploration and return only the useful result.

## Main Takeaway

Context should be treated as a limited resource.

Use:

- Specific prompts
- `/context`
- `/compact`
- `/clear`
- Subagents

to keep the main session focused.