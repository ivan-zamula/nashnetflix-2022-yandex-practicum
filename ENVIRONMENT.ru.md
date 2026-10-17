# Локальное окружение

[English](ENVIRONMENT.md) | [Русский](ENVIRONMENT.ru.md)

Из корня репозитория скопируйте примеры и заполните значения, необходимые сервису:

```bash
cp yandex_project/env.example yandex_project/.env_defult
cp yandex_project/tests/functional/env.example yandex_project/tests/functional/.env_test
```

Созданные файлы храните локально. Используйте собственные учетные данные для разработки. В `env.example` находятся имена переменных и безопасные примеры значений; настоящие учетные данные задаются в локальной конфигурации.
