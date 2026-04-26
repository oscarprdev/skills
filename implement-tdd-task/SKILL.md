---
name: implement-tdd-task
description: Implement tasks using test-driven development by deriving tests from acceptance criteria first, then writing minimal code to make those tests pass. Use when the user asks for TDD, mentions acceptance criteria/definition of done, or wants tests written before implementation.
---

# Implement TDD Task

## Core Principles

- **Tests first**: Derive and write tests from acceptance criteria before any implementation
- **Requirements-driven**: Tests must reflect the task description, definition of done, and acceptance criteria — never the existing implementation
- **Red-green-refactor**: Write failing tests, implement minimal code to pass, then refactor if needed
- **Strict scope**: Only implement what the tests and criteria require

## Workflow

1. **Understand the task**
   - Read task description, acceptance criteria, and definition of done
   - Identify explicit requirements, inputs, outputs, and edge cases
   - Note ambiguities; ask the user if anything is unclear

2. **Derive tests from criteria**
   - Define test cases based solely on requirements and acceptance criteria
   - Do not read existing implementation to infer tests
   - Cover happy path, edge cases, and error scenarios mentioned in criteria

3. **Write tests**
   - Write the minimal test suite needed to verify acceptance criteria
   - Follow existing project testing patterns and conventions
   - Run tests to confirm they fail (red)

4. **Implement**
   - Write the minimal code needed to make the tests pass
   - Do not change tests to fit implementation; change implementation to fit tests
   - Follow existing project conventions and avoid scope creep

5. **Verify**
   - Run the full test suite to confirm all new and existing tests pass
   - Run linting, type checks, and any other project checks
   - Confirm no unintended side effects

6. **Commit and push**
   - Stage all changed files: `git add -A`
   - Commit with a descriptive message: `git commit -m "[task summary]"`
   - Push to remote: `git push`

7. **Notify completion**
   - Report what was implemented
   - List files changed
   - Confirm all derived tests pass

## Anti-patterns to Avoid

- Reading existing code to define what tests "should" look like
- Changing tests to accommodate implementation instead of fixing the code
- Adding untested features or "nice-to-haves" not in acceptance criteria
- Over-engineering before all tests pass

## Output Format

When task is complete, notify the user:

```
Task implemented (TDD): [task summary]

Tests defined:
- [test1]: [brief description]
- [test2]: [brief description]

Changes:
- [file1]: [brief description]
- [file2]: [brief description]

Scope: All acceptance criteria met; all derived tests pass.
Git: Committed and pushed.
```
