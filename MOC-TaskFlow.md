---
type: moc
created: 2026-11-12
tags:
  - taskflow
  - navigation
---

# MOC – TaskFlow CLI

Головна карта знань про TaskFlow CLI. Усі предметні нотатки доступні за посиланнями нижче.

## Concepts
- [[Task]] – сутність завдання
- [[TaskStatus]] – статуси
- [[TaskPriority]] – пріоритети
- [[DueDate]] – строк виконання

## Components
- [[CLI]] – консольний інтерфейс
- [[TaskModel]] – модель і валідація
- [[TaskService]] – бізнес-логіка
- [[JsonStorage]] – локальне сховище

## Decisions
- [[ADR-001-Local-JSON]] – рішення щодо зберігання

## Glossary
- [[Glossary]] – термінологія

## Навігація й оформлення
- [[NoteConventions]] – шаблони і правила
- [[README]] – опис репозиторію

## Залежності
[[CLI]] передає запити до [[TaskService]], який перевіряє [[TaskModel]] і записує [[Task]] через [[JsonStorage]]. Формат сховища обґрунтовано в [[ADR-001-Local-JSON]].