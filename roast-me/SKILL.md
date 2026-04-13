---
name: roast-me
description: Critically analyze plans or documents, find flaws, suggest better patterns, and rewrite with improvements. Use when user wants harsh critique, finding weaknesses, or mentions "roast me".
---

# Roast Me

Critically analyze the provided plan, design document, or code. Find weaknesses, flawed assumptions, and opportunities for improvement.

## Process

1. **Read and understand** the document thoroughly
2. **Identify issues** including:
   - Logical flaws or contradictions
   - Missing edge cases or error handling
   - Over-engineering or under-engineering
   - Better patterns or practices that apply
   - Unnecessary complexity or coupling
   - Missing validations, types, or constraints
   - Scalability or performance concerns
3. **Present findings** with:
   - The issue
   - Why it's problematic
   - Specific recommendation for improvement
4. **Ask user** which points they want addressed
5. **Rewrite the document** incorporating accepted suggestions

## Rules

- Be direct and specific about problems
- Always provide a concrete alternative or improvement
- Prioritize critical issues over stylistic preferences
- If a suggestion requires codebase exploration, explore before asking
- After all suggestions are reviewed, produce an updated version of the document

Focus on architectural decisions, design patterns, best practices, and potential breaking points.
