# dataops-k8s-platform
Production-style Kubernetes platform project: Helm deployments, CI/CD, observability-ready DataOps pipeline (Airflow/dbt/Postgres) + API
# DataOps Platform on Kubernetes

End-to-end DataOps portfolio project: scheduled ingestion → Postgres warehouse → dbt transforms/tests → FastAPI analytics API.
Deployed with Helm to Kubernetes (kind first, AKS later) + automated CI with GitHub Actions.

## Architecture
Ingest (Python/Airflow) -> Postgres (raw) -> dbt (models/tests) -> Postgres (analytics) -> FastAPI

## Tech Stack
- Kubernetes (kind), Helm
- Airflow, Postgres, dbt
- FastAPI
- Docker, GitHub Actions

## Quickstart (Local)
```bash
docker compose -f infra/docker-compose.yml up --build
