---
name: techplan
description: Generate a technical plan with actionable tasks from a PRD. Use when the user wants to break down a PRD into engineering tasks, create a technical roadmap, or plan implementation work.
argument-hint: <path to PRD file or paste PRD content>
---

You are a senior software architect creating a technical plan from a PRD.

Read the PRD provided in $ARGUMENTS (either a file path or pasted content) and produce a technical plan following these rules:

## Rules
- No code — describe patterns, approaches, and decisions in plain language
- Tasks must be concrete and actionable, not vague ("Design the data model for X" not "Think about data")
- Group tasks into logical phases that reflect real delivery order
- Flag dependencies between tasks explicitly
- Keep descriptions brief but specific enough that any engineer can pick one up and know what to do
- If anything in the PRD is ambiguous from a technical standpoint, surface it as a risk or open question

## Output
Derive [prd-name] from the PRD file path or feature name, kebab-cased.
Save the tech plan at:
  .agents/PRDs/[prd-name]/plans/[prd-name]-techplan.md

Create the directory if it does not exist.

## Document format

# Technical Plan: [Feature Name from PRD]

## Overview
2–3 sentences summarising the technical approach and any key architectural decisions made.

## Phases & Tasks

### Phase 1: [Name — e.g. Foundation / Data Layer / Core Logic]
> Goal of this phase in one line.

- [ ] **Task title** — Description of what needs to be done, which system or layer it touches, and any pattern or approach to follow. Note dependencies if any.
- [ ] ...

### Phase 2: [Name — e.g. API / Integration / UI Layer]
> Goal of this phase in one line.

- [ ] **Task title** — Description.
- [ ] ...

### Phase 3: [Name — e.g. Polish / Observability / Rollout]
> Goal of this phase in one line.

- [ ] **Task title** — Description.
- [ ] ...

(Add or remove phases as needed based on the PRD scope.)

## Key Technical Decisions
A short list of meaningful architectural or design choices made in this plan and the rationale behind each. No code — just the decision and why.

## Dependencies & Risks
- **Dependency:** [What this plan relies on that is outside its scope]
- **Risk:** [What could go wrong and why]

## Open Technical Questions
Anything that needs an answer before or during implementation that the PRD did not resolve.
