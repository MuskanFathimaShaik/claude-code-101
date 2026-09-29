# Lesson 8: CLAUDE.md

## Overview

`CLAUDE.md` acts as persistent memory for Claude Code.

A project-level `CLAUDE.md` can provide Claude with important information about the project whenever a new session starts.

It works like an onboarding document for the codebase.

## Why CLAUDE.md Is Useful

Without persistent project instructions, Claude may repeatedly need to discover:

- Project architecture
- Dependencies
- Commands
- Coding conventions
- Existing rules

`CLAUDE.md` keeps these instructions available.

## What to Include

A useful `CLAUDE.md` can contain:

### Project Overview

Describe:

- Technology stack
- High-level architecture
- Important project information

Example:

```text
Next.js 15
Tailwind CSS
Drizzle ORM