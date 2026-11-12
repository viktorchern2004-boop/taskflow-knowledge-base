---
type: component
created: 2026-11-12
tags:
  - taskflow
  - component
---

# TaskModel – модель даних

**Запланований файл:** src/taskflow/models.py.

Описує структуру [[Task]] та її інваріанти незалежно від [[CLI]] та [[JsonStorage]].

## Правила
- Унікальний id не змінюється.
- title не порожній після видалення пробілів.
- status належить [[TaskStatus]].
- priority належить [[TaskPriority]].
- due_date має відповідати [[DueDate]] або бути null.
- created_at задається один раз; updated_at оновлюється при редагуванні.

Модель має тестуватися окремо від консольного інтерфейсу.