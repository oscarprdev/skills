# AI Agent Skills Repository

A curated collection of AI agent skills for Claude Code, Qwen Code, and other AI coding assistants. These skills provide specialized capabilities and domain knowledge for software development tasks.

## Overview

This repository contains reusable skills that enhance AI coding assistants with specialized knowledge in various domains including frontend development, cloud infrastructure, testing, planning, and more. Each skill is a self-contained module with references, decision trees, and best practices.

## Quick Start

### Installation

**For Claude Code:**
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/skills.git

# Skills are located in the root directory
cd skills
```

**For Qwen Code:**
Skills can be installed from this repository by referencing the skill directories.

### Usage

Each skill is designed to be loaded by AI coding assistants when specific tasks are detected. Skills contain:
- `SKILL.md` - Main skill definition with decision trees and references
- `references/` - Detailed reference documentation (if applicable)
- `.skillfish.json` - Skill metadata for skillfish package manager (if applicable)

## Available Skills

### Cloud & Infrastructure

| Skill | Description |
|-------|-------------|
| [cloudflare](cloudflare/) | Comprehensive Cloudflare platform covering Workers, Pages, storage (KV, D1, R2), AI, networking, security, and IaC |
| [durable-objects](durable-objects/) | Cloudflare Durable Objects for stateful coordination, RPC, SQLite storage, alarms, WebSockets |
| [workers-best-practices](workers-best-practices/) | Cloudflare Workers production best practices, streaming, observability, secrets management |
| [wrangler](wrangler/) | Cloudflare Workers CLI for deploying, developing, and managing Workers and resources |

### Frontend Development

| Skill | Description |
|-------|-------------|
| [react-best-practices](react-best-practices/) | React and Next.js performance optimization guidelines from Vercel Engineering |
| [react-useeffect](react-useeffect/) | React useEffect best practices from official docs, state management, and data fetching |
| [frontend-development](frontend-development/) | Modern frontend development patterns and best practices |
| [typescript](typescript/) | TypeScript best practices, advanced types, and type-safe patterns |
| [nothing-design](nothing-design/) | Nothing design system implementation guidelines |

### Testing & Quality

| Skill | Description |
|-------|-------------|
| [e2e-testing](e2e-testing/) | Playwright E2E testing patterns, Page Object Model, configuration, CI/CD integration |
| [test-frontend-unit](test-frontend-unit/) | Frontend Unit Testing Guide with testing libraries and component testing |
| [test-driven-development](test-driven-development/) | Test-driven development methodology and practices |
| [review-task](review-task/) | Code review guidelines and checklists for task completion |

### Planning & Architecture

| Skill | Description |
|-------|-------------|
| [writing-plans](writing-plans/) | Writing effective technical plans and specifications |
| [executing-plans](executing-plans/) | Executing implementation plans with review checkpoints |
| [taskplan](taskplan/) | Generate detailed technical task plans from PRDs and tech plans |
| [techplan](techplan/) | Generate technical plans with actionable tasks from PRDs |
| [implement-task](implement-task/) | Implement tasks from task plans with proper state management |
| [architecture-patterns](architecture-patterns/) | Common architecture patterns and patterns for scalable applications |

### Product & Requirements

| Skill | Description |
|-------|-------------|
| [prd](prd/) | Generate Product Requirements Documents from feature descriptions |
| [write-prd](write-prd/) | Create PRDs through user interview, codebase exploration, and module design |
| [write-a-skill](write-a-skill/) | Create new agent skills with proper structure and progressive disclosure |

### Specialized Skills

| Skill | Description |
|-------|-------------|
| [web-perf](web-perf/) | Web performance analysis using Chrome DevTools, Core Web Vitals, Lighthouse |
| [grill-me](grill-me/) | Stress-test plans and designs through rigorous questioning |
| [claude-code-atelier](claude-code-atelier/) | Claude Code specific patterns and workflows |

## Skill Structure

Each skill follows a standard structure:

```
skill-name/
├── SKILL.md              # Main skill definition
├── references/           # Detailed reference docs (optional)
│   └── ...
└── .skillfish.json       # Skill metadata (optional)
```

### SKILL.md Format

```markdown
---
name: skill-name
description: Brief description of the skill
references:
  - reference-name
---

# Skill Title

Description and usage guidelines.

## Decision Trees

When to use this skill and how to navigate it.

## References

Links to detailed documentation.
```

## Contributing

Contributions are welcome! To add a new skill:

1. Create a new directory under the root with the skill name
2. Add a `SKILL.md` file with the skill definition
3. Add reference documentation in a `references/` subdirectory if needed
4. Follow the existing skill structure and formatting
5. Test the skill with your AI coding assistant

### Skill Development Guidelines

- Keep skills focused on specific domains or tasks
- Use decision trees to guide AI assistants
- Reference official documentation rather than embedding all knowledge
- Keep SKILL.md concise and actionable
- Test skills in real workflows before submitting

## License

[Specify your license here]

## Acknowledgments

Skills in this repository are sourced from various community contributors and official sources. Each skill may have its own attribution requirements.

---

**Note**: This repository is designed to work with AI coding assistants like Claude Code and Qwen Code. Skills should be loaded according to your AI assistant's configuration.
