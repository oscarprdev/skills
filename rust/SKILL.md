---
name: rust
description: |
  Entry point for Rust programming skills. Covers language fundamentals, domain-specific patterns,
  ecosystem tooling, and advanced topics. Not user-invocable directly — load child skills as needed.
user-invocable: false
license: MIT
metadata:
  author: rust-community
  version: "1.0"
---

# Rust

Curated collection of Rust programming skills, from ownership basics to domain-specific patterns.

## Skill Tree

| Skill | Description | Goal | Location |
|-------|-------------|------|----------|
| coding-guidelines | Use when asking about Rust code style or best practices. | Enforce Rust coding style and naming conventions. | skills/coding-guidelines/SKILL.md |
| domain-cli | Use when building CLI tools. | Build command-line applications with argument parsing and TUI. | skills/domain-cli/SKILL.md |
| domain-cloud-native | Use when building cloud-native apps. | Develop microservices, containers, and cloud-native Rust apps. | skills/domain-cloud-native/SKILL.md |
| domain-embedded | Use when developing embedded/no_std Rust. | Write firmware and bare-metal code for microcontrollers. | skills/domain-embedded/SKILL.md |
| domain-fintech | Use when building fintech apps. | Implement financial systems with correct decimal precision. | skills/domain-fintech/SKILL.md |
| domain-iot | Use when building IoT apps. | Connect sensors and devices using IoT protocols. | skills/domain-iot/SKILL.md |
| domain-ml | Use when building ML/AI apps in Rust. | Run machine learning models and training pipelines in Rust. | skills/domain-ml/SKILL.md |
| domain-web | Use when building web services. | Create HTTP services, REST APIs, and web backends. | skills/domain-web/SKILL.md |
| m01-ownership | CRITICAL: Use for ownership/borrow/lifetime issues. | Resolve borrow checker errors and lifetime issues. | skills/m01-ownership/SKILL.md |
| m02-resource | CRITICAL: Use for smart pointers and resource management. | Choose and use smart pointers for heap data. | skills/m02-resource/SKILL.md |
| m03-mutability | CRITICAL: Use for mutability issues. | Fix borrow conflicts with interior mutability. | skills/m03-mutability/SKILL.md |
| m04-zero-cost | CRITICAL: Use for generics, traits, zero-cost abstraction. | Apply generics and traits for zero-cost abstractions. | skills/m04-zero-cost/SKILL.md |
| m05-type-driven | CRITICAL: Use for type-driven design. | Use type states and newtypes to prevent invalid states. | skills/m05-type-driven/SKILL.md |
| m06-error-handling | CRITICAL: Use for error handling. | Propagate errors with Result, anyhow, and thiserror. | skills/m06-error-handling/SKILL.md |
| m07-concurrency | CRITICAL: Use for concurrency/async. | Write safe async/multi-threaded code without deadlocks. | skills/m07-concurrency/SKILL.md |
| m09-domain | CRITICAL: Use for domain modeling. | Model business domains with entities and aggregates. | skills/m09-domain/SKILL.md |
| m10-performance | CRITICAL: Use for performance optimization. | Profile and optimize Rust programs. | skills/m10-performance/SKILL.md |
| m11-ecosystem | Use when integrating crates or ecosystem questions. | Integrate crates and manage dependencies. | skills/m11-ecosystem/SKILL.md |
| m12-lifecycle | Use when designing resource lifecycles. | Design RAII-based resource cleanup and connection pools. | skills/m12-lifecycle/SKILL.md |
| m13-domain-error | Use when designing domain error handling. | Categorize errors and implement retry/fallback strategies. | skills/m13-domain-error/SKILL.md |
| m14-mental-model | Use when learning Rust concepts. | Build intuition for ownership and the borrow checker. | skills/m14-mental-model/SKILL.md |
| m15-anti-pattern | Use when reviewing code for anti-patterns. | Identify and refactor unidiomatic Rust code. | skills/m15-anti-pattern/SKILL.md |
| meta-cognition-parallel | EXPERIMENTAL: Three-layer parallel meta-cognition analysis. | Run three-layer parallel meta-cognition analysis. | skills/meta-cognition-parallel/SKILL.md |
| rust-call-graph | Visualize Rust function call graphs using LSP. | Visualize function call hierarchies. | skills/rust-call-graph/SKILL.md |
| rust-code-navigator | Navigate Rust code using LSP. | Jump to definitions and find references. | skills/rust-code-navigator/SKILL.md |
| rust-daily | CRITICAL: Use for Rust news and daily/weekly/monthly reports. | Fetch Rust community news and updates. | skills/rust-daily/SKILL.md |
| rust-deps-visualizer | Visualize Rust project dependencies as ASCII art. | Render project dependencies as ASCII art. | skills/rust-deps-visualizer/SKILL.md |
| rust-learner | Use when asking about Rust versions or crate info. | Look up crate versions, features, and Rust releases. | skills/rust-learner/SKILL.md |
| rust-refactor-helper | Safe Rust refactoring with LSP analysis. | Safely rename and move symbols. | skills/rust-refactor-helper/SKILL.md |
| rust-skill-creator | Use when creating skills for Rust crates or std library documentation. | Generate new skills from crate or std docs. | skills/rust-skill-creator/SKILL.md |
| rust-symbol-analyzer | Analyze Rust project structure using LSP symbols. | List structs, traits, and functions in a project. | skills/rust-symbol-analyzer/SKILL.md |
| rust-trait-explorer | Explore Rust trait implementations using LSP. | Discover trait implementations. | skills/rust-trait-explorer/SKILL.md |
| unsafe-checker | CRITICAL: Use for unsafe Rust code review and FFI. | Review unsafe code and FFI boundaries for soundness. | skills/unsafe-checker/SKILL.md |
