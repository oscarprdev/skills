---
name: frontend-performance
description: |
  Entry point for all frontend performance and rendering optimization skills. Covers bundle optimization,
  loading strategies, rendering patterns (SSR, ISR, islands), and runtime JavaScript performance.
  Not user-invocable directly — load child skills as needed.
user-invocable: false
license: MIT
metadata:
  author: various
  version: "1.0"
---

# Frontend Performance

Curated collection of performance skills for faster loads, smaller bundles, and smoother interactions.

## Skill Tree

| Skill | Description | Goal | Location |
|-------|-------------|------|----------|
| vite-bundle-optimization | Vite-specific bundle optimization patterns. | Configure builds, code splitting, manage dependencies, troubleshoot slow Vite builds. | skills/vite-bundle-optimization/SKILL.md |
| tree-shaking | Reduce bundle size by eliminating dead code that is never used in your application. | Ensure only used code is included in production bundles. | skills/tree-shaking/SKILL.md |
| static-rendering | Deliver pre-rendered HTML content that was generated at build time for fast, cacheable pages. | Implement static site generation (SSG). | skills/static-rendering/SKILL.md |
| streaming-ssr | Stream server-rendered HTML to the client in chunks for faster Time to First Byte and First Contentful Paint. | Optimize SSR delivery with streaming. | skills/streaming-ssr/SKILL.md |
| server-side-rendering | Generate HTML on the server in response to user requests for faster initial page loads and SEO. | Implement traditional SSR for SEO and performance. | skills/server-side-rendering/SKILL.md |
| progressive-hydration | Delay loading JavaScript for less important parts of the page to improve Time to Interactive. | Hydrate components selectively by priority. | skills/progressive-hydration/SKILL.md |
| static-import | Import code that has been exported by another module using static ES2015 import syntax. | Understand static imports and their impact on bundles. | skills/static-import/SKILL.md |
| preload | Inform the browser of critical resources before they are naturally discovered to speed up loading. | Use `<link rel="preload">` for critical assets. | skills/preload/SKILL.md |
| prefetch | Fetch and cache resources that may be requested soon to reduce future loading times. | Use `<link rel="prefetch">` for next-route assets. | skills/prefetch/SKILL.md |
| prpl | Optimize initial load through precaching, lazy loading, and minimizing roundtrips using the PRPL pattern. | Apply PRPL (Push, Render, Pre-cache, Lazy-load). | skills/prpl/SKILL.md |
| incremental-static-rendering | Update static content after you have built your site using Incremental Static Regeneration (ISR). | Implement ISR for stale-while-revalidate pages. | skills/incremental-static-rendering/SKILL.md |
| islands-architecture | Render small, focused chunks of interactivity within server-rendered web pages to reduce JavaScript overhead. | Build apps with minimal client-side JS using islands. | skills/islands-architecture/SKILL.md |
| import-on-visibility | Load non-critical components when they become visible in the viewport. | Defer loading with Intersection Observer. | skills/import-on-visibility/SKILL.md |
| import-on-interaction | Load non-critical resources when a user interacts with UI requiring it. | Defer loading until user interaction. | skills/import-on-interaction/SKILL.md |
| dynamic-import | Import parts of your code on demand using dynamic import() to reduce initial bundle size. | Implement route-level and component-level code splitting. | skills/dynamic-import/SKILL.md |
| bundle-splitting | Split your code into smaller bundles to reduce initial load time and improve performance. | Configure manual and automatic code splitting. | skills/bundle-splitting/SKILL.md |
| compression | Reduce the time needed to transfer JavaScript over the network using compression techniques like Gzip and Brotli. | Enable and verify asset compression. | skills/compression/SKILL.md |
| web-perf | Analyzes web performance using Chrome DevTools MCP. Measures Core Web Vitals and identifies bottlenecks. | Audit, profile, debug, or optimize page load performance. | skills/web-perf/SKILL.md |
| client-side-rendering | Render your application's UI entirely on the client using JavaScript. | Understand CSR trade-offs and when to use it. | skills/client-side-rendering/SKILL.md |
| js-performance-patterns | JavaScript runtime performance patterns for hot paths, loops, DOM operations, caching, and data structures. | Optimize JS execution performance. | skills/js-performance-patterns/SKILL.md |
| virtual-lists | Optimize rendering of large lists by only displaying items visible in the viewport (windowing). | Implement windowing for long lists. | skills/virtual-lists/SKILL.md |
| view-transitions | Animate page transitions using the View Transitions API for smooth visual DOM changes. | Add native view transition animations. | skills/view-transitions/SKILL.md |
| loading-sequence | Optimize the loading sequence of critical resources to improve Core Web Vitals like FCP, LCP, and FID. | Prioritize and sequence resource loading. | skills/loading-sequence/SKILL.md |
