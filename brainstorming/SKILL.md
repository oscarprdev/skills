---
name: brainstorming
description: Expands user ideas into structured proposals with alternatives, facilitates decision-making, and produces a comprehensive PRD markdown document. Use when the user wants to brainstorm, explore an idea, evaluate options, or create a requirements/ design document from a concept.
---

# Brainstorming

## Quick start

User: "I want a feature that lets users schedule emails."

Agent:
1. Expand: who triggers it, what inputs, edge cases, integrations.
2. Propose alternatives: A) Cron-based queue, B) External scheduler API, C) In-app delayed job.
3. Ask user to pick or refine.
4. On confirmation, ask for target file name and folder, then write the PRD with summary, decision, Mermaid diagrams, and next steps.

## Workflows

### 1. Expand the idea

Given a user idea, explore at least these dimensions:
- **Goal**: What problem does it solve?
- **Actors**: Who initiates or is affected?
- **Inputs / Outputs**: Data going in and out.
- **Constraints**: Time, budget, tech stack, compliance.
- **Edge cases**: Failure modes, abuse, scale.

Summarize findings in 3-5 bullet points before proposing alternatives.

### 2. Propose alternatives

Generate 3-5 distinct approaches. For each provide:
- **Name**: Short label.
- **Description**: 2-3 sentences.
- **Pros / Cons**: At least two of each.
- **Effort**: T-shirt size (S, M, L) or rough time estimate.

Present options to the user and ask:
> "Which alternative do you prefer? Would you like to combine elements, or should I explore a new direction?"

### 3. Confirm output location

Before writing the PRD, ask the user:
> "Where would you like me to save the PRD? Please provide the folder path and file name (e.g., `docs/email-scheduler-prd.md`)."

If the user does not specify, default to the current working directory with a slugified file name (e.g., `email-scheduler-prd.md`).

### 4. Write the PRD document

Create a single markdown file with this structure:

```markdown
# PRD: [Idea Title]

## 1. Overview
One-paragraph summary of the idea and its purpose.

## 2. Expanded Analysis
Detailed findings across the dimensions explored in Step 1.

## 3. Alternatives Considered
| Alternative | Pros | Cons | Effort |
|-------------|------|------|--------|
| ...         | ...  | ...  | ...    |

## 4. Decision & Rationale
State the selected alternative and why it was chosen.

## 5. Diagrams
Include at least one Mermaid diagram:
- System architecture
- User flow
- Decision tree

## 6. Stakeholder Impact
List affected teams or user types and how they are impacted.

## 7. Risks & Mitigations
| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| ...  | ...        | ...    | ...        |

## 8. Next Steps / Action Items
- [ ] Task 1
- [ ] Task 2

## 9. Open Questions
List any unresolved items that need future clarification.
```

**Diagram rules**: Use Mermaid syntax. Choose diagram types that best fit (flowchart, sequence, architecture, gantt). Keep diagrams readable; split into multiple blocks if they exceed 15 nodes.

## Advanced features

- **Iteration**: If the user is unsure, loop back to Step 2 with a hybrid or new alternative instead of forcing a decision.
