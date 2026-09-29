# Lesson 7: Code Review

## Overview

Claude can generate and modify code quickly, but its output should still be reviewed.

Do not rely only on Claude's final summary such as:

> All features have been added and tests pass.

The actual changes should be inspected.

## `/diff`

Use `/diff` to inspect the actual changes made during the session.

Check:

- What files changed
- What code was added
- What code was removed
- Whether unrelated files were modified
- Whether the implementation matches the requirement

## `/code-review`

`/code-review` can launch an isolated reviewer with a clean context.

The purpose is to provide an independent review rather than relying only on the same context that produced the implementation.

## Why Independent Review Helps

The original coding session may have biases because Claude already has a history of decisions from the implementation.

A separate review can help identify:

- Subtle bugs
- Weak or missing tests
- Hard-coded values
- Unrequested changes
- Other implementation issues

## Review Mindset

**Blind Trust → Verification & Triaging**

AI-generated code should be inspected before being accepted.

## Review Findings

Classify findings into:

### Fix Now

Issues that clearly need to be corrected.

### Ask Why

Issues that require clarification or understanding before deciding what to do.

### Leave It

Issues that are acceptable or intentional.

## Main Takeaway

Use Claude to accelerate development, but maintain human verification through actual diff inspection and independent review.