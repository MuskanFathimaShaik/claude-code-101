# Lesson 12: Hooks

## Overview

Hooks are scripts configured in `.claude/settings.json` that execute shell commands automatically at specific Claude Code lifecycle events.

They allow developers to create deterministic workflows that run whenever a configured event occurs.

## Key Takeaway

Hooks can execute commands at specific lifecycle events, such as:

- `PreToolUse`
- `PostToolUse`
- `UserPromptSubmit`
- `Stop`

Unlike instructions written in `CLAUDE.md`, hooks are **deterministic**.

When the configured conditions are met, the hook executes automatically every time.

## Why Use Hooks?

Prompts and markdown instructions are useful for guiding Claude, but they are probabilistic.

Claude may occasionally forget or skip an instruction.

Some workflows require a consistent execution guarantee.

Examples include:

- Code auto-formatting
- Audit logging
- Safety checks
- Security rules
- Automated triggers
- Blocking dangerous actions

For these cases, hooks provide a more reliable mechanism.

## Hook Lifecycle Events

### `PreToolUse`

Runs before Claude executes a tool.

This can be used to inspect or prevent an action before it happens.

For example, a hook can block:

- Modifying protected production files
- Executing dangerous commands

A hook can exit with code `2` to block the action.

### `PostToolUse`

Runs after Claude executes a tool.

This is useful for automated actions after a change has been made.

Example:

- Run a formatter after a file is edited.

### `UserPromptSubmit`

Runs when a user submits a prompt.

This can be used when a workflow needs to be triggered whenever a new prompt is submitted.

### `Stop`

Runs when Claude reaches a stopping point.

This can be used for actions that should occur when Claude finishes its current operation.

## Mindset Shift

**Probabilistic Suggestions → Deterministic Guardrails**

Use prompts and `CLAUDE.md` when Claude needs intelligent instructions or guidance.

Use hooks when a rule or action must be executed automatically and consistently.

## Prompting Shift

### Old Way

Add an instruction to `CLAUDE.md`:

> Please run Prettier formatting after modifying any TypeScript file.

This relies on Claude remembering and following the instruction.

### New Way

Configure a `PostToolUse` hook with a matcher for file edits.

The hook can automatically run the formatter whenever the matching edit occurs.

This removes the need to rely on Claude remembering to run the formatter.

## Safety Example

A `PreToolUse` hook can inspect an action before it is executed.

For example, it can prevent:

- Modifying production files
- Executing dangerous commands
- Running commands such as `rm -rf`

If the hook exits with code `2`, the action can be blocked.

## CLAUDE.md vs Hooks

### CLAUDE.md

Used for:

- Project instructions
- Coding conventions
- Architecture guidelines
- Development guidance
- Rules that require Claude's understanding

### Hooks

Used for:

- Automatic formatting
- Safety checks
- Audit logging
- Deterministic triggers
- Blocking actions
- Automated workflows

## Main Takeaway

Hooks provide deterministic automation inside Claude Code.

Use **`CLAUDE.md` and prompts for intelligent guidance**, and use **hooks for actions and rules that must execute consistently every time**.