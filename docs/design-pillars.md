# Product Design Pillars

These are the four pillars that guide our product design.

---

## Design Excellence

- Every product is documented extensively
- All parameters are categorized, include descriptions and defaults, and are clamped to sane input ranges
- All code follows SOLID design principles
- Every product goes through multiple QA passes before being listed

---

## Style-Agnostic by Design

AWL widgets are built to adapt to your game’s visual language, not impose their own.

- Hybrid grayscale textures and parameterized materials form the foundation
- Retheming is handled through materials, styles, and parameters—not asset replacement
- Texture stacks (grunge, noise, background, stencils) reduce custom art requirements

---

## Material-Driven Flexibility

Visual behavior is controlled through materials and parameters, not hardcoded logic or baked assets.

- All visual properties are animatable via Sequencer
- Effect intensity, textures, and colors are fully exposed and tunable
- Procedural effects live in materials, not Blueprint logic

---

## Composable, Modular Architecture

Widgets are building blocks, not sealed products.

- Designed to slot cleanly into existing UIs
- Modular structure supports reparenting, extension, and recomposition
- Common UI styles are treated as first-class citizens
- Encourages reuse, consistency, and rapid iteration  
