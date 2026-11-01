# Postman-коллекция — HRM System API

| Файл | Назначение |
| --- | --- |
| `HRM_API.postman_collection.json` | 28 запросов с проверками (`pm.test`) |
| `HRM_Local.postman_environment.json` | Окружение: `base_url` |

В названии запроса указан ID тест-кейса из `HRM_Test_Cases.xlsx`. Токены ролей (admin, hr, ivanov, superadmin) сохраняются автоматически в первой папке.

## Запуск
Postman: Import → оба файла → окружение **HRM Local** → Collection Runner (папки по порядку).
Newman: `newman run HRM_API.postman_collection.json -e HRM_Local.postman_environment.json`

## Результат
Все запросы, кроме одного, проходят. Не проходит `[TC-LV-06] EMPLOYEE создаёт status=approved` — это дефект BUG-002.

Запросы создают данные; для повторного прогона пересоздайте БД и выполните `seed_data`.
