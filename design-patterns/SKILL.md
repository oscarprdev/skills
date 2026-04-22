---
name: design-patterns
description: |
  Entry point for vanilla JavaScript design pattern skills. Covers creational, structural, and behavioral patterns
  for building maintainable, decoupled applications. Not user-invocable directly — load child skills as needed.
user-invocable: false
license: MIT
metadata:
  author: patterns.dev
  version: "1.0"
---

# Design Patterns

Curated collection of language-agnostic JavaScript design patterns.

## Skill Tree

| Skill | Description | Goal | Location |
|-------|-------------|------|----------|
| singleton-pattern | Share a single global instance throughout your application to manage global state. | Ensure only one instance of a class exists. | skills/singleton-pattern/SKILL.md |
| proxy-pattern | Intercept and control interactions with target objects using JavaScript Proxies. | Add validation, logging, or access control to objects. | skills/proxy-pattern/SKILL.md |
| prototype-pattern | Share properties among many objects of the same type through JavaScript's prototype chain. | Clone and reuse object configurations efficiently. | skills/prototype-pattern/SKILL.md |
| observer-pattern | Use observables to notify subscribers when an event occurs for decoupled event-driven communication. | Build event-driven architectures with pub/sub. | skills/observer-pattern/SKILL.md |
| module-pattern | Split your code into smaller, reusable pieces with proper encapsulation using ES2015 modules. | Encapsulate and organize code into modules. | skills/module-pattern/SKILL.md |
| mixin-pattern | Add functionality to objects or classes without inheritance using mixins. | Compose reusable behaviors across classes. | skills/mixin-pattern/SKILL.md |
| mediator-pattern | Use a central mediator object to handle communication between components instead of direct coupling. | Reduce direct dependencies between components. | skills/mediator-pattern/SKILL.md |
| factory-pattern | Use factory functions to create new objects without the `new` keyword. | Abstract object creation logic. | skills/factory-pattern/SKILL.md |
| flyweight-pattern | Conserve memory by reusing existing instances when working with large numbers of similar objects. | Optimize memory usage for large datasets. | skills/flyweight-pattern/SKILL.md |
| command-pattern | Decouple methods that execute tasks by sending commands to a commander object. | Implement undo/redo, queuing, and macro commands. | skills/command-pattern/SKILL.md |
