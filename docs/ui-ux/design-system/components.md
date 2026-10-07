# Shared component language

## Foundation

Light mode uses a slate-white canvas, white cards, restrained borders, and pale blue/purple hero gradients. Dark mode uses navy canvas and distinct opaque navy surfaces with brighter text; it is not a color inversion. Use the reference gradients for identity rather than covering every component in gradients.

Cards use 20–28 px radius and 20–32 px padding. Body text stays 16 px or larger in learning content. Action targets are at least 44 px; primary buttons are 48 px tall. Visible focus rings and reduced-motion behavior are required.

## Buttons and inputs

Primary actions use solid blue with white text. Secondary actions use bordered theme surfaces. Icon-only controls have accessible names. Forms have persistent labels. Loading disables repeated submission and announces status; errors include retry. The upload preview only reads a filename; no file bytes are processed or sent.

## Navigation

Desktop: sidebar, global document search, theme/language controls, and student profile. Home, Chat, My Documents, Quizzes, and Profile are active review destinations. Subjects, Notes, and Calendar are disabled and marked Later. Mobile: Home, Chat, central Upload, Quizzes, and Profile bottom navigation. Keep all targets usable in RTL.

## Documents

Document cards show file type, title, page count, and processing status. Ready items open summary, key points, and topics, then contextual chat or a quiz. Processing exposes state and progress; failed or empty states have an action. Citation controls take the student back to the referenced document summary.

## Chat

Use a document context card, starter suggestions, distinct user/assistant messages, a labelled composer, and source chips. AI content uses readable paragraphs. Rafeeq's state reflects the operation; never label a server as online simply because a UI was rendered. Prototype replies are scripted examples.

## Quiz and results

Quiz setup identifies source document, question count, and language. The player has a progress label, question, four answer buttons, and a next action. Grade feedback includes a label and explanation alongside color. Results show score, per-question review, retry, and a document-study action. Use success for a correct response and encouraging for a wrong response.

## Rafeeq

Use the central registry and four approved images. Keep their original white backgrounds in a light tile; do not fabricate transparent/vector exports. Compact contexts use 48–72 px tiles; hero contexts use 220–300 px. Motion is subtle and stopped for reduced motion. Error/offline states include text and recovery controls.

## Responsive and Arabic

Collapse desktop navigation below 900 px, use one-column learning content below 600 px, and retain bottom navigation. Arabic mirrors component layout but preserves the direction of technical terms. Sticky controls must not obscure content at narrow widths or browser zoom.
