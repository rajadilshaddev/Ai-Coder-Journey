# Ai-Coder-Journey
# AGENTS.md

## Purpose

This file provides instructions for AI agents operating within this repository.

The goal is to make safe, maintainable, production-ready changes while minimizing regressions and preserving the existing architecture.

---

# Core Rules

## Rule 1: Understand Before Changing

Before writing any code:

1. Read all files related to the task.
2. Trace data flow from frontend to backend.
3. Understand existing patterns.
4. Identify dependencies and side effects.
5. Create a plan before implementation.

Never start coding immediately after receiving a task.

---

## Rule 2: Minimize Changes

Make the smallest change required to solve the problem.

Prefer:

* Extending existing functionality
* Reusing existing utilities
* Reusing existing components

Avoid:

* Large refactors
* Unnecessary abstractions
* Creating duplicate functionality

---

## Rule 3: Preserve Existing Architecture

Follow the repository's established patterns.

Do not:

* Introduce new architectural styles
* Replace frameworks
* Reorganize directories
* Rewrite working code

Unless explicitly instructed.

---

# Development Standards

## Code Quality

All code must be:

* Readable
* Maintainable
* Modular
* Consistent with existing code

Prefer clarity over cleverness.

---

## Naming

Use descriptive names.

Good:

* createTask()
* updateBoardStatus()
* validateUserPermissions()

Avoid:

* doStuff()
* tempData()
* handle()

---

## Functions

Functions should:

* Have one responsibility
* Be easy to test
* Be reasonably short

Break complex logic into helper functions.

---

# Investigation Process

Before implementing:

## For Bug Fixes

1. Reproduce issue
2. Identify root cause
3. Verify root cause
4. Implement minimal fix
5. Test affected functionality

Never patch symptoms without understanding the cause.

---

## For Features

1. Understand requirements
2. Identify affected systems
3. Review similar features
4. Design implementation
5. Implement incrementally
6. Test thoroughly

---

# Testing Requirements

Always validate changes.

Minimum requirements:

* Existing tests continue to pass
* New functionality is verified
* No obvious regressions exist

If tests are available:

Run relevant tests before completing work.

---

# Security Rules

Never:

* Expose secrets
* Hardcode API keys
* Commit credentials
* Disable authentication
* Bypass authorization checks

Always validate:

* User input
* API payloads
* Query parameters
* File uploads

---

# Database Rules

For schema changes:

* Create migrations
* Make migrations reversible
* Preserve existing data
* Avoid destructive operations

Never drop data without explicit approval.

---

# API Rules

Maintain backward compatibility whenever possible.

Avoid:

* Breaking response structures
* Renaming public fields
* Removing endpoints

Unless explicitly requested.

---

# Frontend Rules

When modifying UI:

* Reuse existing components
* Preserve visual consistency
* Maintain accessibility
* Keep responsive behavior intact

Avoid creating duplicate components.

---

# Documentation

Update documentation whenever:

* New features are added
* APIs change
* Configuration changes
* Environment variables change

---

# Git Workflow

Before creating a commit:

1. Review all modified files
2. Remove debugging code
3. Remove console logs
4. Remove unused imports
5. Verify formatting

---

# Pull Request Format

Provide:

## Summary

What changed.

## Reason

Why the change was needed.

## Technical Details

Implementation approach.

## Testing

Validation performed.

## Risks

Potential side effects.

---

# Prohibited Actions

Do NOT:

* Delete large code sections without justification
* Rewrite working systems
* Change unrelated code
* Introduce unnecessary dependencies
* Modify production configuration without approval
* Ignore existing project conventions

---

# Decision Framework

When multiple solutions exist:

1. Choose the simplest solution.
2. Choose the most maintainable solution.
3. Follow existing repository patterns.
4. Minimize risk.
5. Avoid over-engineering.

---

# Completion Checklist

Before marking a task complete:

* Requirements satisfied
* Code reviewed
* Tests passed
* Documentation updated
* No obvious regressions
* No debug code remains

---

# Agent Behavior

The agent should:

* Think before coding
* Explain major decisions
* Prefer small safe changes
* Ask for clarification when requirements are ambiguous
* Avoid assumptions
* Deliver production-ready code

The objective is not to write the most code.

The objective is to solve the problem correctly with the least risky change possible.
