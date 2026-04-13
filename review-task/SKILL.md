---
name: review-task
description: Review a ready-to-review task. Reads the task file, audits the implementation against conventions, docs and patterns, finds and fixes bugs, then moves to completed. Use when a task needs a thorough code review before being closed.
argument-hint: <path to task file or task slug>
---

You are a senior engineer performing a rigorous, objective code review on work you did not write.
Treat this as a real peer review — be thorough, be honest, fix what is wrong.

You will receive a path or slug in $ARGUMENTS pointing to a task file inside:
  .agents/PRDs/[prd-name]/plans/tasks/ready-to-review/

## Step 1 — Locate & read the task
- If a full path is given, read it directly
- If a slug or number is given, search `.agents/PRDs/*/plans/tasks/ready-to-review/` for a matching file
- Derive [prd-name] from the file path
- Read the task file in full, paying close attention to:
  - Summary and Context
  - Technical Detail
  - Acceptance Criteria
  - Implementation Notes left by the implementor
  - Files Changed list

## Step 2 — Load review context
Before looking at a single line of implementation, build a complete picture of the standards this code must meet:

### Conventions
- Read the project's CLAUDE.md, README, CONTRIBUTING or equivalent docs if present
- Identify naming conventions, folder structure rules, import ordering, and code style patterns from existing files neighbouring the changed ones
- Note error handling patterns used consistently across the codebase
- Note how the project handles logging, validation, and edge cases

### Architecture & patterns
- Read files adjacent to the changed ones to understand how the surrounding system works
- Identify the architectural pattern in play (layered, feature-based, etc.) and check the implementation respects it
- Check how similar features were implemented elsewhere in the codebase and compare

### Libraries
- For each library listed in the task, check how it is used in the rest of the project
- Verify the implementation uses the same patterns and APIs, not a different style introduced ad-hoc

### Dependencies
- Read the task files listed under "Depends on" from the `completed/` folder
- Verify the implementation correctly builds on top of what those tasks established

## Step 3 — Audit the implementation
Review every file listed under "Files Changed" methodically.

### Correctness
- [ ] Does the implementation do what the task Summary describes?
- [ ] Does it satisfy every Acceptance Criterion in the task file?
- [ ] Are all edge cases mentioned in "Notes & Risks" handled?
- [ ] Are there any logical errors, off-by-one mistakes, or incorrect conditions?
- [ ] Are there missing null / undefined / empty state guards?
- [ ] Are async operations handled correctly — errors caught, race conditions avoided?
- [ ] Are any side effects unintended or out of scope?

### Consistency
- [ ] Does naming follow project conventions exactly?
- [ ] Does folder and file placement match the project structure?
- [ ] Are imports ordered and structured as the rest of the codebase does it?
- [ ] Is error handling consistent with established patterns?
- [ ] Is the code style consistent — no ad-hoc patterns introduced without justification?

### Completeness
- [ ] Are all files from "Files to create" actually created?
- [ ] Are all files from "Files to modify" actually updated?
- [ ] Are all files from "Files to delete" actually removed with no orphaned references?
- [ ] Are new modules correctly wired — exported, registered, routed, or imported where needed?
- [ ] Are there any TODO comments, console logs, debug flags, or placeholder values left behind?

### Security & safety
- [ ] No secrets, tokens or credentials hardcoded anywhere
- [ ] No user input used unsanitised
- [ ] No unsafe operations introduced (e.g. unchecked type assertions, ignored errors)
- [ ] No new external dependencies introduced that were not in the task

### Performance
- [ ] No obviously expensive operations in hot paths
- [ ] No memory leaks introduced (uncleaned subscriptions, event listeners, timers)
- [ ] Data fetching follows the patterns established in the codebase

### Scope
- [ ] No unrelated changes slipped in
- [ ] No existing behaviour altered beyond what the task required

## Step 4 — Compile findings
Categorise every issue found:

**Blocker** — Must be fixed before this task can be completed. Bugs, broken acceptance criteria, security issues, missing wiring that would cause runtime failures.

**Warning** — Should be fixed now as it will cause problems later. Inconsistent patterns, missing edge case handling, performance issues.

**Suggestion** — Nice to fix but not blocking. Minor style inconsistencies, small improvements that do not affect correctness.

If there are zero blockers and zero warnings, proceed directly to Step 6.
If there are any blockers or warnings, proceed to Step 5.

## Step 5 — Fix all blockers and warnings
For each blocker and warning:
- State clearly what the issue is and why it is a problem
- Apply the fix directly to the affected file
- After fixing, re-check the surrounding code to ensure the fix did not introduce a new issue
- Do not fix suggestions unless they are trivially simple — log them instead

After all fixes are applied, re-run the full audit checklist from Step 3 to confirm no new issues were introduced.

## Step 6 — Update the task file
Append a review summary to the task file:

---
status: completed
reviewed_at: [current timestamp]

## Review Summary

### Findings
**Blockers fixed:** [N]
- [Issue description → what was fixed and in which file]

**Warnings fixed:** [N]
- [Issue description → what was fixed and in which file]

**Suggestions (not fixed — logged for future):**
- [Issue description and recommendation]

### Verdict
[One of: "Passed clean" / "Passed with fixes" / "Passed with fixes — follow-up recommended"]

### Follow-up tasks recommended
- [Any new task that should be created as a result of this review, or "none"]
---

## Step 7 — Move to completed
Move the task file from:
  .agents/PRDs/[prd-name]/plans/tasks/ready-to-review/[NNN-task-slug].md
To:
  .agents/PRDs/[prd-name]/plans/tasks/completed/[NNN-task-slug].md

Then report back to the user with:
- Verdict
- A concise list of what was fixed and why
- Any suggestions logged but not applied
- Any follow-up tasks recommended
- Full path of the completed task file
