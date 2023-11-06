# Инструкция для запуска сервисов с использованием docker-compose

Если отказали сервисы, то чтобы продолжить разработку мы запускаем локльно основные сервисы при помощи [docker-compose](./docker-compose.development.yml)

### Настройка

1. Запустить команду `yarn start:compose`.
2. Если нужно вести разработку на клиенте, то нужно внести изменения в файл [apps/s3/configs/env.json](./apps/s3/configs/env.json).

| Свойство     | Необходимо задать                   |
| ------------ | ----------------------------------- |
| newSergekUrl | `http://localhost:3001/api/main/v2` |

### Список сервисов

| Наименование | | Порт |
| ------------------- | | ---- |
| main |
| worker | | 3002 |
| events-receiver |
| telegram-bot | | - |
| anomaly-monitoring | | - |
| black-list-receiver | | - |
| pc-sender | | 3004 |
| redis-storage | | - |
| cron | | - |
| logger | | - |
| external-system | | 3005 |
| pre-processing | | 3006 |
| mobile | | 3007 |
| violation-process | | 3008 |
| violator-warnings | | 3009 |
