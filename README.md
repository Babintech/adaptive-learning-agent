# Adaptive Learning Agent

AI-powered adaptive learning system foundation for a competency-based mathematics platform.

## Stack

- Python 3.12+
- FastAPI
- PostgreSQL
- SQLAlchemy 2.x
- Alembic
- Pydantic v2
- pytest
- Docker / Docker Compose
- uv

## Local development

1. Copy environment variables:

   ```bash
   cp .env.example .env
   ```

2. Install dependencies:

   ```bash
   uv sync --dev
   ```

3. Run the API:

   ```bash
   uv run uvicorn app.main:app --reload
   ```

4. Run tests:

   ```bash
   uv run pytest
   ```

5. Run linting:

   ```bash
   uv run ruff check .
   ```

## Database migrations

Create a migration:

```bash
uv run alembic revision -m "create something"
```

Apply migrations:

```bash
uv run alembic upgrade head
```

## Docker

```bash
docker compose up --build
```

## Health endpoint

- `GET /health` returns `{"status": "ok"}`.
