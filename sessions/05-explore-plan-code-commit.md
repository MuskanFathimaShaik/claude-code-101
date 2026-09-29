# Lesson 5: Explore → Plan → Code → Commit

## Overview

A reliable Claude Code development workflow is:

**Explore → Plan → Code → Commit**

This workflow separates understanding, planning, implementation, and review.

## 1. Explore

First, Claude investigates the existing codebase.

It can:

- Read relevant files
- Understand the architecture
- Find related implementations
- Identify dependencies
- Understand existing patterns

The goal is to understand the current implementation before changing it.

## 2. Plan

After exploration, create an implementation plan.

Plan Mode can be used to formulate and review the approach before modifying files.

The plan should identify:

- Files that need changes
- Implementation approach
- Required dependencies
- Potential impacts
- Testing requirements

The plan can then be reviewed before implementation begins.

## 3. Code

Once the plan is approved, Claude implements the changes.

Implementation should follow:

- The approved plan
- Project conventions
- Explicit requirements
- Success criteria

Tests should be run to verify the implementation.

## 4. Commit

After implementation:

- Review the changes
- Run code review
- Generate an appropriate commit message
- Commit the changes
- Push when ready

## Mindset Shift

**Plan First → Edit Second**

Instead of immediately modifying files, understand the project and agree on the implementation approach first.

## Prompting Example

### Immediate Implementation

> Implement feature X in the codebase.

### Better Workflow

> Explore the upload pipeline, create a plan for WebP conversion with the required dependencies, and wait for my approval before modifying any files.

## Main Takeaway

Planning before implementation reduces unnecessary course corrections and allows design problems to be identified before files are changed.