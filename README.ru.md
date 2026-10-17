# Киноплатформа NashNetflix (Yandex Practicum, 2022)

[English](README.md) | [Русский](README.ru.md)

Киноплатформа с админкой Django, поисковым сервисом FastAPI, PostgreSQL, Elasticsearch, Redis и ETL-процессом.

Учебные материалы программы Middle Python Developer Яндекс Практикума.


## Получение кода

```bash
git clone https://github.com/ivan-zamula/nashnetflix-2022-yandex-practicum.git
cd nashnetflix-2022-yandex-practicum
```

## Код и материалы

- [yandex_project/app](yandex_project/app)
- [yandex_project/fastapi-solution](yandex_project/fastapi-solution)
- [yandex_project/postgres_to_es](yandex_project/postgres_to_es)
- [yandex_project/tests](yandex_project/tests)

## Возможности

NashNetflix, аналог Netflix, созданный во время обучения в Яндекс Практикуме. Исходный основной репозиторий: [psgaiduk/Async_API_sprint_1](https://github.com/psgaiduk/Async_API_sprint_1).

- Админка Django для фильмов, жанров и персон.
- Синхронизация новых и измененных записей из базы админки в Elasticsearch каждые 10 секунд.
- API для фильмов, жанров и персон.

Основной каталог: [yandex_project](yandex_project). В нем находятся админка Django, база PostgreSQL, кеш Redis, поиск и индексация Elasticsearch, ETL из PostgreSQL в Elasticsearch и сервис FastAPI.

## Адреса сервисов

Замените `{host}` на адрес сервера:

- Админка: `http://{host}/admin`
- Документация API: `http://{host}:81/api/openapi`

## Сборка и запуск

Установите Docker Compose и Make, настройте локальное окружение и выполните команды из `yandex_project`:

```bash
cd yandex_project
make build
make up
```

При первом запуске соберите статические файлы, создайте миграции и суперпользователя, заполните базу данных:

```bash
make first_start
```

## Переменные окружения

| Переменная | Назначение |
| --- | --- |
| `DB_NAME` | Имя базы PostgreSQL |
| `DB_USER` | Пользователь PostgreSQL |
| `DB_PASSWORD` | Пароль PostgreSQL |
| `DB_HOST` | Имя хоста сервиса PostgreSQL |
| `DB_PORT` | Порт подключения PostgreSQL |
| `SECRET_KEY` | Секретный ключ Django |
| `DEBUG` | Режим отладки |
| `ALLOWED_HOSTS` | Разрешенные хосты админки |
| `INTERNAL_IPS` | Внутренние IP-адреса для админки |
| `ES_PORT` | Порт Elasticsearch |
| `ES_HOST` | Имя хоста Elasticsearch |
| `REDIS_HOST` | Имя хоста Redis |
| `REDIS_PORT` | Порт Redis |
| `DJANGO_SUPERUSER_USERNAME` | Пользователь админки Django |
| `DJANGO_SUPERUSER_PASSWORD` | Пароль админки Django |
| `DJANGO_SUPERUSER_EMAIL` | Email администратора Django |

## Тесты

Из каталога `yandex_project`:

```bash
make build_tests
make start_tests
```

## Команда

- Pavel Gaiduk
- Ivan Zamula
- Kirill Bondar, до 29 июля 2022 года

Настройка локального окружения: [English](ENVIRONMENT.md) | [Русский](ENVIRONMENT.ru.md). Используйте шаблоны `env.example`, а рабочие файлы храните локально.
