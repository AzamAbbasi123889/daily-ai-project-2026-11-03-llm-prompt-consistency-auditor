# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] POST /prompts returns 201 and a prompt_id
- [ ] Responses from all configured models are stored within 5 seconds
- [ ] At least 100 prompts can be processed without error
- [ ] Metric computation completes <2 seconds per prompt
- [ ] Cosine similarity and edit distance are persisted in the DB
- [ ] GET /prompts/{id}/metrics returns JSON with similarity, edit distance, latency
- [ ] Metrics are exported to OpenTelemetry collector
- [ ] UI loads in <2 seconds locally
- [ ] Dashboard updates when new prompts are added
- [ ] Set up repo, Docker Compose, CI pipeline
- [ ] Define DB schema and apply migrations
- [ ] Implement POST /prompts and LangGraph workflow for two LLMs
- [ ] Store raw responses
- [ ] Unit tests for each FastAPI route using pytest‑asyncio
- [ ] Integration tests with mocked LLM clients (responses fixture)
- [ ] Load test 100 concurrent POST /prompts using locust (target RPS≥20)
- [ ] Security test: ensure no SQL injection via prompt text
- [ ] OpenTelemetry sanity check: traces appear in local collector
- [ ] Docker Compose for local dev (api, db, redis, otel‑collector, grafana)
- [ ] GitHub Actions builds multi‑arch images and pushes to Docker Hub
- [ ] Deploy to Render/ Railway with managed Postgres, enable HTTPS
- [ ] Configure Grafana dashboards for latency and consistency alerts

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
