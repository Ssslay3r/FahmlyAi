# Fahmly Backend

This directory is reserved for the shared Python / FastAPI backend used by both Flutter and Next.js clients. The MVP will be a modular monolith; business logic and access to database, storage, and AI modules will be coordinated here.

## Directory Purposes

- `app/api/`: future FastAPI routers and endpoints.
- `app/core/`: configuration, security, authentication settings, and application configuration.
- `app/models/`: database / ORM models.
- `app/schemas/`: Pydantic request and response schemas.
- `app/services/`: business logic and coordination of storage and AI operations.
- `app/repositories/`: database access layer.
- `app/utils/`: reusable helper utilities.
- `tests/`: backend unit tests; broader system tests belong in the root `tests/` directory.

`requirements.txt` is a placeholder for future Python dependencies. `.env.example` records future backend configuration names with empty values only. The root example lists the same names for repository-wide reference; configuration loading will be decided during backend initialization.

No endpoints, authentication, database connections, Python packages, or application entry point have been implemented. The backend will integrate `ai/` without creating a separate AI service or duplicating logic in clients.
