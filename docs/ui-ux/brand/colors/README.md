# Color system

The agreement uses blue/cyan/purple gradients, light surfaces, and intentional dark surfaces. The proposed token values follow the approximate palette visible in the original board:

- Primary blue: `#2563EB`.
- Secondary purple: `#8B5CF6`.
- Accent cyan: `#06B6D4`.
- Highlight orange: `#F97316`.
- Dark text/background: `#0F172A`.
- Light background: `#F8FAFC`.

Use primary blue for solid action buttons; branding gradients are reserved for the hero and selected decorative details. Cyan and orange are not body-text colors on white. Theme-specific text tokens provide darker/lightened colors for readability.

Success and error also have text, labels, and icons. Never communicate answer correctness through color alone. The [JSON tokens](../../design-system/tokens/tokens.json) define semantics; [CSS tokens](../../design-system/tokens/tokens.css) mirror them for the prototype. Font and full component accessibility validation remain part of production implementation.
