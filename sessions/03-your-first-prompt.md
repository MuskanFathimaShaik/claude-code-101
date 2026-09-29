# Lesson 3: Your First Prompt

## Overview

The quality of Claude Code's output depends heavily on how clearly the task is defined.

A good prompt should provide:

- Clear objective
- Relevant context
- Specific location
- Requirements
- Constraints
- Expected outcome
- Success criteria

## Key Learnings

### 1. Define the Objective

Clearly explain what needs to be accomplished.

Avoid vague instructions such as:

> Add image conversion.

Instead, specify what needs to be changed and where.

### 2. Provide Context

Tell Claude which part of the application is relevant.

For example:

- Specific file
- Existing implementation
- Library that should be used
- Related functionality

### 3. Define Constraints

Explain what Claude should and should not change.

Examples:

- Use the existing library
- Don't change unrelated files
- Follow existing project conventions
- Handle errors properly

### 4. Define Success Criteria

Tell Claude how the work should be considered complete.

Examples:

- Tests should pass
- Existing functionality should continue working
- Validation errors should be handled
- No unrelated files should be modified

## Specification Over Generation

The mindset shift is:

**Specification → Generation**

Instead of asking AI to simply generate code, define the requirements and boundaries first.

## Prompting Example

### Less Effective

> Write a WebP image conversion script.

### More Effective

> Add WebP conversion to `src/pipeline/upload.ts`. Use our existing image library, handle validation errors gracefully, and ensure tests pass.

The second prompt gives Claude:

- Location
- Feature
- Existing dependency requirement
- Error-handling requirement
- Validation criteria

## Main Takeaway

A good prompt behaves more like a clear development specification than a simple question.