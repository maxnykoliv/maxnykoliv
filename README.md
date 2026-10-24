# Hi, I'm Maksym Nykoliv

**Python Backend Developer** · Lviv, Ukraine · open to remote

I build backend services with Python: REST APIs, relational data modelling,
caching and background jobs, with tests and CI from the first commit. I care
about correctness under concurrency, clear error contracts and code that the
next person can read.

## Tech stack

**Languages:** Python, SQL, JavaScript<br>
**Frameworks:** FastAPI, Django, Django REST Framework, Pydantic, SQLAlchemy 2 (async)<br>
**Data:** PostgreSQL, Redis, Alembic<br>
**Tooling:** Docker, Docker Compose, GitHub Actions, pytest, ruff, Git, Linux

## Featured projects

### [Task Management API](https://github.com/maxnykoliv/TaskManagementAPI)
Async REST API for team task tracking built with FastAPI, SQLAlchemy 2 and PostgreSQL.
- Status workflow enforced as a state machine; business rules live in a service layer.
- Race-free per-user task limit using `SELECT … FOR UPDATE` row locks.
- JWT auth with Argon2 and timing-safe login; a background worker auto-cancels overdue tasks.
- 54 tests against real PostgreSQL at 97% coverage; CI checks migrations against the models.

### [RepoRadar](https://github.com/maxnykoliv/RepoRadar)
Full-stack GitHub search: a Django REST Framework API in front of the GitHub Search API, with a React client.
- Redis cache with normalized keys and a TTL; it degrades to uncached instead of failing when Redis is down.
- GitHub failures mapped to meaningful statuses (429 + `Retry-After`, 422, 502, 504).
- JWT accounts and race-safe saved favorites; CI runs the integration tests against real Redis.

### [Location Popularity](https://github.com/maxnykoliv/locationpopularity)
Django REST API for a catalogue of places with reviews, ratings and popularity ranking.
- Popularity score weighs average rating, review count and 7-day views (deduplicated per viewer).
- Versioned Redis keys for list caching, invalidated on commit.
- CSV/JSON export with protection against CSV formula injection.

## Contact

[LinkedIn](https://www.linkedin.com/in/maksym-nykoliv-4877b1433/) ·
[Telegram](https://t.me/necromastery0) ·
[maxnykoliv@gmail.com](mailto:maxnykoliv@gmail.com)
