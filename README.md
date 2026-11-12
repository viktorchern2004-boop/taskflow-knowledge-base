---
type: documentation
created: 2026-11-12
tags:
  - taskflow
  - documentation
---

# TaskFlow Knowledge Base – Obsidian vault

Окремий репозиторій Markdown-нотаток про застосунок [TaskFlow CLI](https://github.com/viktorchern2004-boop/taskflow-cli). Створено для практичної роботи №2. База знань не є частиною репозиторію застосунку.

**Почніть з:** [[MOC-TaskFlow]] – карта змісту, що веде до всіх змістових нотаток.

## Структура
- `Concepts/` – предметні сутності та правила.
- `Components/` – заплановані компоненти програми.
- `Decisions/` – архітектурні рішення (ADR).
- `Glossary/` – спільні визначення термінів.
- `Templates/` – [[NoteConventions]] з правилами frontmatter.

## Відкрити в Obsidian
1. Завантажити репозиторій на комп'ютер **окремо** від `taskflow-cli` (Git Clone або GitHub → Code → Download ZIP).
2. Розпакувати ZIP у самостійну папку, наприклад `Documents/taskflow-knowledge-base`.
3. У Obsidian вибрати **Open folder as vault** і вказати цю папку.
4. Відкрити [[MOC-TaskFlow]], перейти за wiki-посиланнями й відкрити Graph view.

## Межі доступу для наступних практичних
З ПР3 агентна IDE відкриватиме тільки репозиторій застосунку. Доступ до цього vault здійснюватиметься через окремий MCP-сервер, а не шляхом прямого відкриття папки vault в IDE агента.
