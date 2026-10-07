# Fahmly

An AI-powered cross-platform study assistant that transforms students' learning materials into interactive explanations, summaries, questions, and quizzes, with support for natural conversational Arabic and Libyan dialect.

## Overview

Fahmly is a university graduation project for a four-person team with approximately 12 weeks for development. The MVP will use a modular monolithic backend shared by the Flutter mobile client and the Next.js web client.

This repository currently contains architecture scaffolding, documentation placeholders, and UI/UX design assets. All application features and technologies described below are planned unless explicitly stated otherwise.

## Core Features

Planned capabilities include authentication, study-document upload and processing, AI chat grounded in uploaded materials, summarization, explanations, quiz generation, and quiz results. Arabic and Libyan dialect support will be included in the design and AI evaluation.

## Architecture

```text
Flutter Mobile ----+
                   +-- REST/HTTPS --> FastAPI Backend
Next.js Web -------+                       |
                                           +-- PostgreSQL + pgvector
                                           +-- Object Storage
                                           +-- AI / RAG / LLM
```

- Flutter and Next.js are clients of the same central FastAPI API.
- Business logic lives primarily in the backend; clients do not duplicate AI logic.
- The backend integrates the AI-specific modules in `ai/` within the modular monolith.
- PostgreSQL stores relational data and pgvector supports vector similarity search.
- Original documents belong in Object Storage; document metadata and chunk references belong in the database.
- RAG retrieves relevant document chunks before sending context to the LLM.
- AI providers should remain replaceable where practical, without unnecessary abstractions.
- Keep the MVP simple and maintainable; microservices and additional infrastructure are outside the initial scope.

## Technology Stack

Planned stack:

- Mobile: Flutter / Dart.
- Web: Next.js / TypeScript.
- Backend: Python / FastAPI.
- Database: PostgreSQL with the pgvector extension.
- File storage: Object Storage (provider to be selected).
- AI: document processing, embeddings, RAG, and LLM integration (providers to be selected).
- Development and delivery: Docker, automated testing, and GitHub Actions / CI/CD.

Dependencies, applications, containers, and CI workflows have not been initialized.

## Repository Structure

```text
apps/             Future Flutter and Next.js clients
backend/          Shared FastAPI backend layers and backend unit tests
ai/               RAG modules, prompts, evaluation, and experiments
database/         Future migrations, seeds, and schema assets
infrastructure/   Future Docker and deployment configuration
docs/             Requirements, design, and graduation-project documentation
tests/            Cross-component integration, end-to-end, and AI evaluation tests
scripts/          Future development and maintenance utilities
.github/          Reserved GitHub Actions workflow location
```

Root `.env.example` documents future configuration names, `.gitignore` excludes private and generated files, and `docker-compose.yml` reserves future local orchestration. Empty directories use `.gitkeep` so Git can track them.

The UI/UX directories organize branding and design assets for both clients:

```text
docs/
└── ui-ux/
    ├── brand/
    │   ├── logo/
    │   ├── mascot/
    │   │   ├── default/
    │   │   ├── thinking/
    │   │   ├── success/
    │   │   └── happy/
    │   ├── colors/
    │   ├── typography/
    │   └── brand-guidelines/
    ├── design-system/
    ├── wireframes/
    ├── mobile/
    ├── web/
    └── prototypes/
```

See [the UI/UX index](docs/ui-ux/README.md) for existing assets, design guidance, and the status of each area. Design assets do not indicate that application features are implemented.

The [interactive UI/UX prototype](docs/ui-ux/prototypes/index.html) demonstrates the original approved Rafeeq identity, light/dark themes, English/Arabic layouts, and sample study flows. It runs locally without initializing either client application or connecting to the backend.

## MVP

Planned scope, not implemented functionality:

1. User authentication.
2. Document upload.
3. Document storage.
4. Text extraction.
5. Chunking.
6. Embedding generation.
7. pgvector storage.
8. RAG question answering.
9. Document summarization.
10. AI explanations.
11. Quiz generation.
12. Quiz results.
13. Flutter + Web access through the same backend.

## Development Status

The project is currently under development, at the repository-structure planning stage. No application code, database schema, RAG pipeline, authentication, or CI/CD workflows have been implemented. No dependencies have been installed.

The next step is to plan UI/UX and system requirements before initializing the Flutter, Next.js, and FastAPI applications.

## Team

Fahmly is intended for a four-person university graduation-project team. Team member names, responsibilities, and collaboration practices will be documented as planning progresses.

## Security Notes

- Never commit `.env` files, credentials, API keys, student uploads, or temporary document-processing output.
- Example environment files contain empty placeholders only; real values belong in local configuration or deployment secret management.
- LLM and embedding API keys must remain on the backend and must never be exposed in Flutter, browser code, or public Next.js environment variables.
- Store original student documents in Object Storage with access controls planned alongside authentication and authorization.
- Ignore rules are a safeguard; review changes before committing to ensure private files and secrets are excluded.

## Documentation

See [the documentation index](docs/README.md) for the planned locations of requirements, architecture, database design, API contracts, UI/UX, testing, AI/RAG, deployment, diagrams, and project-management assets.

Component READMEs describe the purpose of each directory. Detailed specifications and implementation will follow the requirements and UI/UX planning phase.

See [the UI/UX documentation](docs/ui-ux/README.md) for branding, mascot assets, design-system guidance, and mobile/web screen designs.
