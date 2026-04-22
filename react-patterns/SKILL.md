---
name: react-patterns
description: |
  Entry point for all React-related pattern skills. Provides a curated tree of React best practices,
  architectural patterns, rendering optimizations, and modern stack guidance. This skill is not
  user-invocable directly — load child skills as needed.
user-invocable: false
license: MIT
metadata:
  author: patterns.dev
  version: "1.0"
---

# React Patterns

Curated collection of React patterns, best practices, and optimization techniques.

## Skill Tree

| Skill | Description | Goal | Location |
|-------|-------------|------|----------|
| react-2026 | A comprehensive guide to building React apps with a modern 2026 stack, covering frameworks, build tools, routing, state management, and AI integration. | Choose the right React stack and understand the modern ecosystem. | skills/react-2026/SKILL.md |
| react-best-practices | React and Next.js performance optimization guidelines from Vercel Engineering. | Write, review, or refactor React/Next.js code for optimal performance. | skills/react-best-practices/SKILL.md |
| react-composition-2026 | Modern React composition patterns for 2025/2026. | Design component APIs, build shared UI libraries, refactor prop-heavy components. | skills/react-composition-2026/SKILL.md |
| react-data-fetching | Modern React data fetching patterns. | Implement caching, deduplication, optimistic updates, or parallel loading. | skills/react-data-fetching/SKILL.md |
| react-render-optimization | React rendering performance patterns. | Reduce re-renders, optimize memoization, state design, or review React performance. | skills/react-render-optimization/SKILL.md |
| react-selective-hydration | Combine streaming server-side rendering with selective hydration for faster interactivity in React 18+. | Optimize hydration strategy for React 18+ apps. | skills/react-selective-hydration/SKILL.md |
| react-server-components | Render components on the server without sending their JavaScript to the client, dramatically reducing bundle sizes. | Implement React Server Components effectively. | skills/react-server-components/SKILL.md |
| react-useeffect | React useEffect best practices from official docs. | Write/review useEffect, useState for derived values, data fetching, or state synchronization. | skills/react-useeffect/SKILL.md |
| hooks-pattern | Use functions to reuse stateful logic among multiple components throughout the app. | Extract and share stateful logic via custom Hooks. | skills/hooks-pattern/SKILL.md |
| hoc-pattern | Pass reusable logic down as props to components using Higher Order Components. | Compose components with shared logic via HOCs. | skills/hoc-pattern/SKILL.md |
| render-props-pattern | Pass JSX elements to components through props for flexible, reusable component composition. | Share code between components using render props. | skills/render-props-pattern/SKILL.md |
| presentational-container-pattern | Enforce separation of concerns by separating the view from the application logic. | Split data-fetching logic from UI rendering. | skills/presentational-container-pattern/SKILL.md |
| provider-pattern | Make data available to multiple child components without prop drilling using React Context. | Share global data (themes, auth, locale) across the component tree. | skills/provider-pattern/SKILL.md |
| compound-pattern | Create multiple components that work together to perform a single task by sharing implicit state. | Build dropdowns, tabs, menus with related sub-components. | skills/compound-pattern/SKILL.md |
| route-based | Dynamically load components based on the current route to reduce initial bundle size. | Implement route-level code splitting. | skills/route-based/SKILL.md |
| ai-ui-patterns | Design patterns for building AI-powered interfaces like chatbots and intelligent assistants in React. | Integrate LLMs and streaming into React UIs. | skills/ai-ui-patterns/SKILL.md |
