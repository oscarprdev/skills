---
name: implement-task
description: Implement scoped tasks with minimal, strict adherence to instructions. Use when implementing features from tickets, tasks, or well-defined requirements where scope must be respected and over-engineering avoided.
---

# Implement Task

## Core Principles

- **Minimal implementation**: Only what's asked, nothing more
- **Strict scope**: Do not extend beyond the task instructions
- **No overcomplication**: Choose the simplest solution that works
- **Ask before assuming**: If anything is unclear, ask the user before proceeding

## Workflow

1. **Understand the task**
   - Read the task description carefully
   - Identify explicit requirements only
   - Note any ambiguities or missing details

2. **Clarify if needed**
   - If scope, behavior, or implementation details are unclear, ask the user
   - Do not make assumptions about unspecified requirements
   - Confirm edge cases only if they affect the core implementation

3. **Plan minimally**
   - Identify the smallest set of changes needed
   - Choose the simplest approach that satisfies requirements
   - Avoid adding abstractions, utilities, or features not explicitly requested

4. **Implement**
   - Make changes scoped to the task only
   - Follow existing project conventions
   - Do not refactor unrelated code

5. **Verify**
   - Run relevant tests, linting, and type checks
   - Confirm implementation matches task description exactly
   - Ensure no unintended side effects

6. **Commit and push**
   - Stage all changed files: `git add -A`
   - Commit with a descriptive message: `git commit -m "[task summary]"`
   - Push to remote: `git push`

7. **Notify completion**
   - Report what was implemented
   - List files changed
   - Confirm scope adherence
   - Confirm commit and push completed

## Anti-patterns to Avoid

- ❌ Adding "nice-to-have" features not in scope
- ❌ Creating abstractions "for future use"
- ❌ Refactoring unrelated code "while you're at it"
- ❌ Over-engineering solutions
- ❌ Making assumptions about unclear requirements

## Output Format

When task is complete, notify the user:

```
✅ Task implemented: [task summary]

Changes:
- [file1]: [brief description]
- [file2]: [brief description]

Scope: All requirements met, nothing extra added.
Git: Committed and pushed.
```
