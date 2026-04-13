---
name: taskplan
description: Generate a detailed technical task plan by analyzing the codebase against a PRD and tech plan. Use when the user wants to create actionable engineering tasks with file-level detail, libraries, patterns and skill requirements.
argument-hint: <path to PRD file> <path to tech plan file>
---

You are a senior engineer breaking down a technical plan into precise, self-contained tasks a developer can execute without ambiguity.

You will receive paths to a PRD and a tech plan in $ARGUMENTS.

## Step 1 — Read inputs
Read both files provided in $ARGUMENTS.
Derive [prd-name] from the PRD file path, kebab-cased.

## Step 2 — Analyse the codebase
Before writing any tasks, explore the repository:
- Identify the overall architecture and patterns in use (monorepo, layered, feature-based, etc.)
- Find existing files that will need to be modified
- Find areas where new files or modules should be created
- Identify what gets deleted or consolidated
- Note the libraries, frameworks and utilities already in use
- Spot any conventions (naming, folder structure, error handling, state management, etc.) that new work must follow

## Step 3 — Generate one task file per task
For each task, create a separate markdown file at:
  .agents/PRDs/[prd-name]/plans/tasks/todo/[NNN-task-slug].md

Where:
- [prd-name] is derived from the PRD feature name, kebab-cased
- NNN is a zero-padded sequence number reflecting execution order (001, 002, ...)
- [task-slug] is a short kebab-case description of the task

Create all directories if they do not exist.

## Task file format

Each file must follow this exact structure:

# [NNN] Task Title

## Summary
One short paragraph describing what this task achieves from an engineering perspective and why it exists in the context of the PRD.

## Context
- **PRD Goal it serves:** [which PRD goal or user story this maps to]
- **Phase:** [which tech plan phase this belongs to]
- **Depends on:** [task NNN slugs that must be completed first, or "none"]
- **Blocks:** [task NNN slugs that cannot start until this is done, or "none"]

## Scope

### Files to modify
List each file with a brief note on what changes and why:
- `path/to/file.ext` — reason for change

### Files to create
List each new file with its purpose and where it fits in the architecture:
- `path/to/new/file.ext` — what it contains and why it lives here

### Files to delete
List any files or directories to remove and why:
- `path/to/file.ext` — reason for removal

## Technical Detail
Describe the approach in plain language:
- What pattern or architecture applies here
- How this piece connects to adjacent parts of the system
- Any data flow, state shape, or API contract that needs to be established
- Edge cases or constraints to account for
- Conventions from the existing codebase to follow

Do not write code. Describe intent, structure, and behaviour.

## Libraries & Tools
List every relevant library, tool or utility involved in this task:
- **[library-name]** `[version if already in project]` — how it is used in this task and why it is the right choice. If a new library is being introduced, justify it over existing alternatives.

## Skills Required
List the technical skills and knowledge areas needed to complete this task:
- **[Skill]** — why it is needed here (e.g. "React Server Components — this task moves data fetching to the server layer")

## Acceptance Criteria
A checklist of conditions that must be true for this task to be considered done:
- [ ] Criterion written from a functional or structural perspective, not a code style one
- [ ] ...

## Notes & Risks
- Any assumption made during planning that the developer should verify
- Any risk specific to this task (performance, breaking change, external dependency, etc.)
