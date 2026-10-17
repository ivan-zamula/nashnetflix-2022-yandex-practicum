# NashNetflix movie platform (Yandex Practicum, 2022)

[English](README.md) | [Русский](README.ru.md)

A movie platform combining a Django administration app, a FastAPI search service, PostgreSQL, Elasticsearch, Redis and ETL code.

Course work from Yandex Practicum's Middle Python Developer program.


## Get the code

```bash
git clone https://github.com/ivan-zamula/nashnetflix-2022-yandex-practicum.git
cd nashnetflix-2022-yandex-practicum
```

## Code and resources

- [yandex_project/app](yandex_project/app)
- [yandex_project/fastapi-solution](yandex_project/fastapi-solution)
- [yandex_project/postgres_to_es](yandex_project/postgres_to_es)
- [yandex_project/tests](yandex_project/tests)

## Features

NashNetflix is a Netflix-style project developed during Yandex Practicum training. The original main repository is [psgaiduk/Async_API_sprint_1](https://github.com/psgaiduk/Async_API_sprint_1).

- A Django admin panel for movies, genres and people.
- Synchronization of new and changed records from the admin database to Elasticsearch every 10 seconds.
- An API for movies, genres and people.

The main directory is [yandex_project](yandex_project). It contains the Django admin service, PostgreSQL database, Redis cache, Elasticsearch search and indexing, a PostgreSQL-to-Elasticsearch ETL process and a FastAPI service.

## Service addresses

Replace `{host}` with the deployment host:

- Admin panel: `http://{host}/admin`
- API documentation: `http://{host}:81/api/openapi`

## Build and run

Install Docker Compose and Make, configure the local environment, then run from `yandex_project`:

```bash
cd yandex_project
make build
make up
```

On the first start, collect static files, create migrations and a superuser, and populate the database:

```bash
make first_start
```

## Environment variables

| Variable | Purpose |
| --- | --- |
| `DB_NAME` | PostgreSQL database name |
| `DB_USER` | PostgreSQL username |
| `DB_PASSWORD` | PostgreSQL password |
| `DB_HOST` | PostgreSQL service hostname |
| `DB_PORT` | PostgreSQL connection port |
| `SECRET_KEY` | Django secret key |
| `DEBUG` | Debug mode |
| `ALLOWED_HOSTS` | Allowed admin panel hosts |
| `INTERNAL_IPS` | Internal IP addresses for the admin panel |
| `ES_PORT` | Elasticsearch port |
| `ES_HOST` | Elasticsearch hostname |
| `REDIS_HOST` | Redis hostname |
| `REDIS_PORT` | Redis port |
| `DJANGO_SUPERUSER_USERNAME` | Django admin username |
| `DJANGO_SUPERUSER_PASSWORD` | Django admin password |
| `DJANGO_SUPERUSER_EMAIL` | Django admin email |

## Tests

From `yandex_project`:

```bash
make build_tests
make start_tests
```

## Team

- Pavel Gaiduk
- Ivan Zamula
- Kirill Bondar, until 29 July 2022

Local environment setup: [English](ENVIRONMENT.md) | [Русский](ENVIRONMENT.ru.md). Use the `env.example` templates and keep working configuration files local.
