# Fahmly Database

This directory is reserved for database-related development assets. The planned primary database is PostgreSQL with pgvector for vector similarity search. Original uploaded documents will be stored in Object Storage rather than directly in PostgreSQL.

- `migrations/`: future versioned database changes.
- `seeds/`: future development seed data using synthetic, non-sensitive examples.
- `schemas/`: future schema definitions and related development assets.

Expected future entities include User, Document, DocumentChunk, Conversation, Message, Quiz, Question, QuizAttempt, and QuizAnswer. Their fields, relationships, and constraints will be determined during requirements and database design.

No final schema, migration, seed data, or database connection has been created. Design documentation and ERDs will belong in `docs/database/` and `docs/diagrams/`.
