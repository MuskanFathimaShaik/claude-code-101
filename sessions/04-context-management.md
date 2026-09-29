# Lesson 4: Context Management

## Overview

Claude uses context to understand the current development task.

Context can include:

- Files that were read
- Commands that were executed
- Tool results
- Previous conversation
- Project information

## Key Learnings

### 1. Context Has Limits

Long development sessions continuously add information to the context.

As a session becomes larger and more cluttered, irrelevant or outdated information can make it harder for Claude to stay focused.

### 2. Avoid Unnecessary Context

Not every task requires Claude to inspect the entire repository.

Providing focused instructions helps keep the working context relevant.

### 3. Use Project Rules

Recurring project instructions can be documented in `CLAUDE.md`.

This prevents repeatedly explaining the same rules during every session.

### 4. Reset Between Different Tasks

When moving to a completely different feature, clearing the previous context can help Claude start with a clean focus.

## Mindset Shift

**Passive Chatting → Active Context Curation**

Instead of allowing one conversation to continue indefinitely, actively manage what Claude needs to know.

## Prompting Shift

### Old Approach

Continue one long conversation for every feature.

### New Approach

- Keep tasks focused
- Document recurring rules
- Clear context when changing tasks
- Use context-management commands
- Delegate isolated work to subagents

## Main Takeaway

Effective context management helps keep Claude focused and reduces confusion during longer development sessions.