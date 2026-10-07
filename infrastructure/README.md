# Fahmly Infrastructure

This directory is reserved for future Docker configuration, deployment configuration, and environment-specific infrastructure assets.

- `docker/`: future container configuration after applications are initialized.
- `deployment/`: future deployment and environment configuration.

The root `docker-compose.yml` contains an empty service placeholder only. No Dockerfiles, running services, or deployment configuration exist yet.

The MVP will remain a modular monolith with the shared FastAPI backend. Kubernetes, Kafka, Redis, and microservices are outside this initialization scope.
