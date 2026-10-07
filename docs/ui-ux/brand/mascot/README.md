# Rafeeq — identity and state behavior

Rafeeq is the approved AI study companion: the rounded speech-bubble robot, cyan/blue/purple gradients, purple graduation cap, white face, and expressive blue eyes. The original images are the identity; do not replace them with another robot or redraw them as an approximate SVG.

Four official expressions exist: [default](default/rafeeq-default.png), [thinking](thinking/rafeeq-thinking.png), [success](success/rafeeq-success.png), and [happy](happy/rafeeq-happy.png).

## One semantic state model for both clients

Use `idle`, `greeting`, `listening`, `thinking`, `reading`, `explaining`, `working`, `quiz`, `success`, `encouraging`, `error`, and `offline`. The future Flutter and Next.js implementations should share the same concepts and use their respective state-management tools; the prototype demonstrates the behavior in one local JavaScript controller.

Each state selects an expression, status text, accessible description, and motion policy through a central registry. Screen components must not duplicate asset-path decisions.

## Asset mapping and fallbacks

- Default: `idle`, `listening`, `explaining`, `quiz`.
- Happy: `greeting`, `encouraging`.
- Thinking: `thinking`, `reading`, `working`.
- Success: `success`.
- Default with explicit text and a recovery action: `error`, `offline`.

Only four expressions are approved. Reading, working, explaining, listening, quiz, error, and offline therefore use documented fallbacks; no new character expressions are invented. See [the machine-readable registry](states.json).

## Transitions

- Home: greeting, then idle.
- Typing: listening; submitting: thinking; responding: explaining.
- Upload demonstration: working, then reading, then success.
- Summarization: reading, then explaining.
- Quiz generation: thinking, then quiz.
- Correct answer: success. Incorrect answer: encouraging with an explanation.
- Request failure: error with retry. Lost connection: offline with reconnect.

One operation owns the temporary transitions. Navigating away cancels its timers so an earlier task cannot overwrite the current screen's state. Motion stays subtle and honors reduced-motion preferences. Status text remains available without animation or color.
