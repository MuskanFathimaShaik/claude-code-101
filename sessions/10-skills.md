# Lesson 10: Skills

## Overview

A Skill is a reusable set of instructions that teaches Claude Code how to perform a specialized task.

A skill contains a `SKILL.md` file.

## Why Use Skills?

Without skills, you may repeatedly provide the same instructions.

For example:

> Review this PR and check brand colors, accessibility, TypeScript strict types, and commit message formats.

If this process is repeated often, the instructions can become a reusable skill.

## How Skills Work

Skills are loaded on demand.

Claude matches the user's request against the skill description and loads the relevant skill when appropriate.

This means the skill instructions do not need to remain in the main context all the time.

## Benefits

Skills help with:

- Repeated workflows
- Team coding standards
- Review checklists
- Commit message formats
- Specialized development tasks

## Mindset Shift

**Re-prompting → Reusable Task Automation**

Instead of repeatedly explaining the same process, document it once as a reusable skill.

## Example

### Without a Skill

> Review this PR and check accessibility, TypeScript strictness, branding, and commit format.

### With a Skill

> Review this PR.

Claude can identify and load the relevant review skill.

## Main Takeaway

Skills turn frequently repeated instructions and workflows into reusable, on-demand capabilities.