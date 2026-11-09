# Motion Design Integration (companion guidance)
Graphify analyzes project relationships. It does not generate animation or replace a frontend renderer.
Use `.agents/skills/graphify-motion-workflow/SKILL.md` alongside a motion-design skill in the consuming website project.
## Safe workflow
Map architecture → select components → storyboard interactions → implement → test → refresh graph.
## Quality criteria
- Functional purpose for each animation; no gratuitous perpetual motion.
- `prefers-reduced-motion` alternative preserving information and navigation.
- Animate transform/opacity where possible; avoid forced synchronous layout.
- Test touch, keyboard, viewport changes, hydration, cleanup and memory.
- Keep a static fallback for WebGL and heavy visual effects.
- Document tradeoffs, dependencies, and benchmark measurements rather than claiming unmeasured FPS.
