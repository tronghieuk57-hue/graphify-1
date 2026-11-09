---
name: graphify-motion-workflow
description: Map a frontend codebase before adding motion, then verify dependency impact and keep its graph current.
---
# Graphify Motion Workflow
Use when changing an existing interactive website. Graphify is code intelligence, not an animation renderer.
1. Inspect package.json, routes, components, CSS, motion libraries and existing accessibility conventions.
2. If graphify-out/graph.json exists, run `graphify query "Which components own the hero, navigation, scroll behavior, and animation lifecycle?"`. Otherwise use scoped source inspection; build a graph only when the codebase is large or relationships are unclear.
3. Record affected modules and lifecycle boundaries; never overwrite unrelated code or project configuration.
4. Build a motion plan: purpose, trigger, duration, easing, reduced-motion fallback, cleanup, and performance budget.
5. Implement using existing stack; prefer CSS for small interactions, GSAP/ScrollTrigger for timelines, and Three.js only when 3D adds value.
6. Cleanup listeners, animation contexts, RAF loops, observers, and WebGL resources on unmount. Avoid hydration mismatches.
7. Verify mobile and desktop, keyboard focus, reduced motion, console errors, CLS, and interaction responsiveness.
8. After edits, run available tests and `graphify update .` if installed; report untested items explicitly.
Never install packages or execute repository scripts without reviewing them first.
