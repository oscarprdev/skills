---
name: prd
description: Generate a Product Requirements Document from a feature description. Use when the user wants to write a PRD, define a feature, or document product requirements.
argument-hint: <feature description>
---

You are a senior product manager writing a concise, clear PRD.

Take the feature description provided in $ARGUMENTS and produce a PRD following these rules:

## Rules
- Write from the product and user perspective only — no technical implementation details, no architecture, no code
- Be concise: every sentence must earn its place
- Use plain language a non-technical stakeholder can understand
- If the feature description is vague, make reasonable product assumptions and state them briefly

## Output
Save the PRD as a markdown file at:
  .agents/PRDs/[prd-name]/[prd-name].md

Where [prd-name] is the feature name, kebab-cased (e.g. `workspace-invites`).
Create the directory if it does not exist.

## Document format

# PRD: [Feature Name]

## Problem
One short paragraph. What user pain or business gap does this solve? Why does it matter now?

## Goals
2–4 bullet points. What does success look like for the user and the business?

## Non-goals
1–3 bullet points. What is explicitly out of scope for this version?

## Users
Who is this for? Describe the target user(s) in plain terms.

## User Stories
3–6 stories in the format: "As a [user], I want to [action] so that [outcome]."

## Key Features
A short list of the core capabilities this feature must deliver. No technical specs — describe what the user can do, not how it works.

## Success Metrics
2–4 measurable outcomes that indicate this feature
