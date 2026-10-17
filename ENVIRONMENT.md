# Local environment

[English](ENVIRONMENT.md) | [Русский](ENVIRONMENT.ru.md)

Copy the example files from the repository root, then fill in the values required by the service:

```bash
cp yandex_project/env.example yandex_project/.env_defult
cp yandex_project/tests/functional/env.example yandex_project/tests/functional/.env_test
```

Keep the resulting files local. Use your own development credentials. `env.example` contains variable names and safe sample defaults; real credentials belong in the local configuration.
