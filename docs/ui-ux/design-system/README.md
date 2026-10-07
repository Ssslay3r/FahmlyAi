# Fahmly Design System — reference-aligned redesign

The original brand board and four approved Rafeeq images define the identity. The tokens and screen specifications translate that identity into a reusable language for the future Flutter and Next.js clients.

- [Semantic JSON tokens](tokens/tokens.json): palette, themes, type, spacing, radius, shadows, sizing, breakpoints, and motion.
- [CSS tokens](tokens/tokens.css): a manually maintained mirror used by the offline prototype.
- [Components](components.md): behavior and visual rules.
- [Rafeeq state model](../brand/mascot/README.md): shared semantic states and approved-expression fallbacks.
- [Interactive preview](../prototypes/index.html): review in light/dark and English/Arabic; use the Design system screen to inspect the four expressions and all twelve states.

No framework packages, generated Flutter app, Next.js app, or application themes are installed. Production clients should consume equivalent tokens after the design is reviewed. Avoid importing the old token generator or old mascot assets from the superseded kit.
