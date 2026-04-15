---
name: plan-to-tasks
description: Split a plan or PRD into individual, well-defined task documents with clear scope, context, and acceptance criteria. Use when breaking down a plan into tasks, splitting implementation tickets, or creating scoped task documents from a plan/PRD.
---

# Plan to Tasks

Break a plan into individual task documents, each self-contained with enough context to understand and execute without reading the full plan.

## Workflow

1. **Read the plan** - Identify the source file (PRD, plan doc, etc.)
2. **Extract phases/slices** - Identify logical groupings or vertical slices
3. **Create task documents** - Generate one `.md` file per task in `tasks/` directory
4. **Number and link** - Use sequential IDs (T001, T002...) and note dependencies

## Task Document Template

Each task document follows this structure:

```md
# Task: [Short, action-oriented title]

**ID**: T001  
**Status**: Pending  
**Phase**: [Phase name or slice]  
**Dependencies**: [None | T002, T003]

## Context

[2-3 sentences: Why this task exists, how it fits into the overall plan. Include any background needed to understand the problem.]

## Scope

**In scope**:
- [Specific deliverable or action]
- [Another specific item]

**Out of scope**:
- [Explicitly excluded item]
- [What will be handled in another task]

## Technical Details

- **Files**: [Paths to create/modify]
- **Approach**: [Key technical decisions, patterns to follow]
- **Interfaces**: [APIs, types, data structures if relevant]

## Acceptance Criteria

- [ ] [Clear, testable condition]
- [ ] [Another condition]
- [ ] [Definition of done]

## Notes

[Any caveats, open questions, or references to docs/decisions.]
```

## Guidelines

### Keep tasks scoped

- **One responsibility** - Each task should deliver one clear outcome
- **Independent context** - Reader shouldn't need the full plan to understand what to do
- **Vertical slice** - Prefer end-to-end functionality over layer-by-layer work

### Write clear acceptance criteria

- Use **observable outcomes** ("User can upload file" not "Implement upload logic")
- Include **edge cases** where relevant
- Make them **testable** - someone should be able to verify yes/no

### Capture dependencies accurately

- Only list **hard dependencies** (must be done before), not nice-to-haves
- If tasks can be parallelized, don't mark them as dependent
- Note **data dependencies** (e.g., "requires API from T002")

### Provide enough technical detail

- List **exact file paths** when known
- Reference **existing patterns** to follow (e.g., "Use same pattern as `src/features/auth/`")
- Include **type signatures or schemas** if they constrain the implementation

## Output

Create a `tasks/` directory with one file per task:

```
tasks/
├── T001-setup-project-structure.md
├── T002-implement-auth-api.md
├── T003-build-login-page.md
└── ...
```

File naming: `T[NNN]-[kebab-case-slug].md`

After creating all tasks, generate a summary:

```md
# Task Breakdown Summary

| ID    | Title                  | Phase      | Dependencies | Status  |
|-------|------------------------|------------|--------------|---------|
| T001  | Setup project structure| Foundation | None         | Pending |
| T002  | Implement auth API     | Foundation | T001         | Pending |
```

## Quality Checklist

Before presenting tasks, verify:

- [ ] Each task has a single, clear responsibility
- [ ] Acceptance criteria are testable and specific
- [ ] Dependencies are accurate (no false dependencies)
- [ ] Technical details include file paths or patterns
- [ ] Context explains why this task matters
- [ ] Out of scope items prevent scope creep
- [ ] Summary table is complete and accurate
