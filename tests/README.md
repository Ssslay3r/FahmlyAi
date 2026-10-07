# Fahmly System Tests

This directory is reserved for tests spanning the shared backend, clients, storage, database, and AI modules.

- `integration/`: tests of interactions between major system components.
- `e2e/`: future complete user-flow tests.
- `ai-evaluation/`: checks of RAG retrieval quality, answer grounding, Arabic support, and Libyan dialect support.

Backend unit tests remain in `backend/tests/`. AI evaluation methods and reference assets belong in `ai/evaluation/`, while testing plans and reports belong in `docs/testing/` and `docs/ai-rag/`.

No tests or test dependencies have been added at this stage. Future fixtures should use synthetic or approved non-sensitive material; uploaded student documents must not be committed.
