---
type: concept
created: 2026-11-12
tags:
  - taskflow
  - concept
---

# Task – завдання

Основна сутність TaskFlow CLI: конкретна робота, яку користувач хоче виконати.

## Поля
| Поле | Тип | Обмеження |
| --- | --- | --- |
| id | UUID у вигляді рядка | унікальний |
| title | рядок | не порожній |
| description | рядок | необов'язковий |
| status | перелік | [[TaskStatus]], початковий todo |
| priority | перелік | [[TaskPriority]], початковий medium |
| due_date | дата або null | [[DueDate]] |
| created_at | ISO 8601 | дата створення |
| updated_at | ISO 8601 | дата останньої зміни |

## Життєвий цикл
Користувач створює завдання через [[CLI]]. [[TaskService]] перевіряє дані за правилами [[TaskModel]] та передає їх у [[JsonStorage]]. Після перезапуску дані залишаються доступними.