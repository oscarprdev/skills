---
name: vue-patterns
description: |
  Entry point for all Vue-related pattern skills. Provides a curated tree of Vue best practices,
  component patterns, Composition API techniques, and state management strategies.
  This skill is not user-invocable directly — load child skills as needed.
user-invocable: false
license: MIT
metadata:
  author: patterns.dev
  version: "1.0"
---

# Vue Patterns

Curated collection of Vue patterns, component architecture guides, and Composition API techniques.

## Skill Tree

| Skill | Description | Goal | Location |
|-------|-------------|------|----------|
| components | Self-contained modules that couple markup (HTML), logic (JS), and styles (CSS) as the building blocks of Vue apps. | Understand component structure, composition, and reuse in Vue. | skills/components/SKILL.md |
| composables | Functions that encapsulate and reuse stateful logic among multiple components using the Composition API. | Extract and share reactive logic across components. | skills/composables/SKILL.md |
| script-setup | Compile-time syntactic sugar for a more concise Composition API syntax in Vue single-file components. | Write cleaner Vue SFCs with `<script setup>`. | skills/script-setup/SKILL.md |
| provide-inject | Have nested components access data without prop drilling using Vue's provide/inject mechanism. | Share data across deeply nested component trees. | skills/provide-inject/SKILL.md |
| renderless-components | Components that don't render their own markup, providing logic to children via scoped slots. | Separate logic from presentation in reusable components. | skills/renderless-components/SKILL.md |
| dynamic-components | Dynamically switch between components using Vue's special `<component>` element with the `is` attribute. | Conditionally render different components at runtime. | skills/dynamic-components/SKILL.md |
| async-components | Optimize web app performance by loading components asynchronously only when they are needed. | Implement lazy loading for Vue components. | skills/async-components/SKILL.md |
| render-functions | Create component templates programmatically with JavaScript using Vue's `h()` render function or JSX. | Build components with programmatic rendering. | skills/render-functions/SKILL.md |
| state-management | Manage application-level state between components using stores, Pinia, or the Composition API. | Choose and implement the right state management approach. | skills/state-management/SKILL.md |
| container-presentational | Enforce separation of concerns by separating the view from the application logic in Vue components. | Split data handling from UI rendering in Vue. | skills/container-presentational/SKILL.md |
| data-provider | Utilize renderless components for managing and providing data to child components via scoped slots. | Centralize data fetching without coupling to UI. | skills/data-provider/SKILL.md |
