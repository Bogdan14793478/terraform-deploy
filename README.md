# Terraform Deploy

Запуск Terraform з параметрами

## Описание

Проект для запуска Terraform с параметрами через Jenkins.

## Параметры

- `TERRAFORM_PATH` - путь к Terraform коду (по умолчанию: ./terraform)
- `AUTO_APPROVE` - флаг для auto-apply (по умолчанию: false)
- `ENVIRONMENT` - окружение: dev, stage, prod (по умолчанию: dev)

## Использование

Этот проект автоматически сканируется Jenkins Multibranch Pipeline каждые 5 минут.

