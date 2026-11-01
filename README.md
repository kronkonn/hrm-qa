> Тестируемый проект: [hrm-django](https://github.com/kronkonn/hrm-django)

# QA-документация — HRM System

| Файл / папка | Содержимое |
| --- | --- |
| `HRM_Test_Plan.xlsx` | Тест-план и чек-лист Smoke |
| `HRM_Test_Cases.xlsx` | 55 тест-кейсов с результатами, RTM, баг-репорты, статистика |
| `HRM_Test_Summary_Report.docx` | Итоговый отчёт о тестировании |
| `bugs/` | Описания дефектов с шагами и скриншотами |
| `known-issues.md` | Дополнительные замечания, найденные при тестировании |
| `postman/` | Коллекция Postman для API-проверок |
| `screenshots/` | Скриншоты ручных UI-кейсов (имя файла = ID кейса) |

## Итоги
Выполнено 54 из 55 кейсов: 51 Passed, 3 Failed; 1 Not Run (кроссбраузерность). Дефектов в наборе: 3 (1 Blocker, 2 Critical).

## Как воспроизвести
1. Поднять backend и frontend, выполнить `python manage.py seed_data` (см. BUG-001 для чистой БД).
2. UI-кейсы пройти по шагам из `HRM_Test_Cases.xlsx`.
3. API-кейсы — коллекция из `postman/` (Collection Runner или Newman).
