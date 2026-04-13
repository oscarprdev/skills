---
name: implement-task
description: Implement a task from the task plan. Reads the task file, moves it to in-progress, implements all codebase changes, self-reviews, then moves to ready-to-review. Use when the user wants to execute a specific task file.
argument-hint: <path to task file or task slug>
---

You are a senior engineer implementing a well-scoped task with full ownership from start to finish.

You will receive a path or slug in $ARGUMENTS pointing to a task file inside:
  .agents/PRDs/[prd-name]/plans/tasks/todo/

## Step 1 — Locate & read the task
- If a full path is given, read it directly
- If a slug or number is given, search `.agents/PRDs/*/plans/tasks/todo/` for a matching file
- Read the task file completely before doing anything else
- Derive [prd-name] from the file path
- Read any tasks listed under "Depends on" and confirm they exist in `completed/` — if they do not, stop and tell the user which dependencies are not yet complete

## Step 2 — Move to in-progress
Move the task file from:
  .agents/PRDs/[prd-name]/plans/tasks/todo/[NNN-task-slug].md
To:
  .agents/PRDs/[prd-name]/plans/tasks/in-progress/[NNN-task-slug].md

Prepend this frontmatter to the file:

---
status: in-progress
started_at: [current timestamp]
---

## Step 3 — Understand the context
Before touching any file:
- Re-read the task's "Files to modify", "Files to create", "Files to delete" sections
- Read each file listed under "Files to modify" in full
- Read neighbouring files to understand conventions, imports and patterns in use
- Check how libraries listed in the task are already used in the codebase
- Do not assume — verify everything against the actual codebase state

## Step 4 — Plan before acting
Internally outline the sequence of changes before making any edit:
- Order changes so dependent pieces come first (types before logic, logic before UI)
- Identify if any files listed in the task no longer exist or have moved — adapt and note it
- Confirm folder structures exist before creating files; create directories if needed

## Step 5 — Implement
Execute all changes described in the task:

### Modifications
- Apply only changes relevant to this task — do not refactor unrelated code
- Follow every convention observed in the existing codebase (naming, structure, error handling, state patterns, import style)
- Match the architectural pattern described in "Technical Detail"
- Honour every item in "Acceptance Criteria" as a checklist guiding the implementation

### Creations
- Place new files exactly where the task specifies
- Follow the project's folder and naming conventions
- Ensure new modules are properly connected to the rest of the system (exports, registrations, routes, etc.)

### Deletions
- Delete files listed under "Files to delete"
- Check for any remaining imports or references to deleted files across the codebase and remove or replace them

### Libraries
- Use only libraries listed in the task
- Do not introduce new dependencies not mentioned in the task — if one is genuinely needed, pause and flag it to the user before continuing

## Step 6 — Self-review
Once implementation is complete, conduct a structured review:

### Correctness
- [ ] Every acceptance criterion in the task file is met
- [ ] No files listed in the task were skipped without a documented reason
- [ ] Deleted files have no remaining references in the codebase

### Consistency
- [ ] Code follows the conventions observed in Step 3
- [ ] Naming is consistent with the rest of the codebase
- [ ] No unrelated changes were introduced

### Completeness
- [ ] New files are properly wired into the system
- [ ] No half-finished logic, placeholder comments or TODO markers left behind
- [ ] All imports resolve correctly

### Risk check
- [ ] No breaking changes introduced beyond the task scope
- [ ] No hardcoded values, secrets or environment-specific assumptions
- [ ] Edge cases noted in the task are handled

If any self-review item fails, fix it before proceeding.

## Step 7 — Update the task file
Append a completion summary to the task file:

---
status: ready-to-review
completed_at: [current timestamp]

## Implementation Notes
- [What was done, any deviations from the original plan and why]
- [Any assumption made during implementation that reviewers should know]
- [Any follow-up task or risk discovered during implementation]

## Files Changed
- Modified: [list]
- Created: [list]
- Deleted: [list]
---

## Step 8 — Move to ready-to-review
Move the task file from:
  .agents/PRDs/[prd-name]/plans/tasks/in-progress/[NNN-task-slug].md
To:
  .agents/PRDs/[prd-name]/plans/tasks/ready-to-review/[NNN-task-slug].md

Then report back to the user with:
- A brief summary of what was implemented
- Any deviations from the task plan
- Any risks or follow-ups discovered during implementation
- The full path of the task file now in ready-to-review/
