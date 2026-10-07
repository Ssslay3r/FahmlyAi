# Fahmly UI/UX — approved identity

This redesign follows the agreement in the project chat **ملخص مشروع التخرج**: the original Rafeeq references, blue/cyan/purple gradients, rounded cards, light and dark themes, and an Arabic experience designed alongside English.

The previous exported kit used a different mascot and is superseded by the files here. A recoverable ZIP copy is kept on the original development machine at `.local-backups/ui-ux-before-redesign.zip`. The ZIP is excluded from Git and is not included in GitHub clones.

## Review the design

Open [the interactive prototype](prototypes/index.html) in a browser. It is a local design demonstration using fictional documents and scripted responses, not a Flutter or Next.js application. No backend, AI provider, or upload service is connected.

The preview supports desktop and phone layouts, light/dark themes, English/Arabic with RTL, onboarding, home, documents, document summary, cited chat, quiz setup/player/results, profile, and a design-system view. Navigation and example interactions work locally.

## Visual source of truth

- [Original brand board](brand/brand-guidelines/approved-brand-board.jpeg): overall identity and layout direction.
- [Default Rafeeq](brand/mascot/default/rafeeq-default.png): normal and ready states.
- [Thinking Rafeeq](brand/mascot/thinking/rafeeq-thinking.png): question processing.
- [Success Rafeeq](brand/mascot/success/rafeeq-success.png): completion and achievement.
- [Happy Rafeeq](brand/mascot/happy/rafeeq-happy.png): greeting and encouragement.

These five files are byte-for-byte copies of the original approved attachments. Their white backgrounds are retained; the prototype uses light mascot tiles in both themes instead of inventing transparent or vector versions.

## Directory guide

- `brand/logo/`: logo composition guidance using the approved Rafeeq identity.
- `brand/mascot/`: original expressions and the shared semantic state specification.
- `brand/colors/`: palette roles and theme guidance.
- `brand/typography/`: Latin and Arabic type guidance.
- `brand/brand-guidelines/`: the original board and identity rules.
- `design-system/`: reusable component specifications and semantic tokens.
- `wireframes/`: user flows and screen structure.
- `mobile/`: mobile design behavior and screen coverage.
- `web/`: desktop, tablet, and mobile-web design behavior.
- `prototypes/`: the self-contained interactive review artifact.

## Scope and status

Design assets and the local prototype are prepared for review; production application features remain unimplemented. The original references define the identity. New screen details, responsive behavior, and accessibility decisions are proposed extensions of that identity and still need review before implementation.

Notes, Calendar, and Subjects appear as disabled future destinations in the desktop reference layout; they do not add functionality to the MVP. Both future clients will use the same FastAPI backend. Mock responses and scores in this prototype make no claims about real AI or persistence.
