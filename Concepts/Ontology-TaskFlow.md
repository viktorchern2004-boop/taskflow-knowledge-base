---
type: concept
created: 2026-11-12
tags: [taskflow, ontology, concept]
---

# Онтологія TaskFlow CLI

Легковагу онтологію описано папками Obsidian, типами нотаток у YAML та типізованими зв'язками між ними.

## Типи сутностей
| Тип | Папка | Приклади |
| --- | --- | --- |
| concept | Concepts | [[Task]], [[TaskStatus]], [[TaskPriority]], [[DueDate]] |
| component | Components | [[CLI]], [[TaskService]], [[TaskModel]], [[JsonStorage]] |
| decision | Decisions | [[ADR-001-Local-JSON]], [[ADR-PR3-MCP]] |
| glossary | Glossary | [[Glossary]] |

Комітні нотатки `Commit-...` з ПР3 мають тип `concept` за технічною схемою MCP, але описують події GitHub, а не предметні сутності.

## Типізовані відношення
- `depends_on` – залежність між компонентами: [[CLI]] → [[TaskService]]; [[TaskService]] → [[TaskModel]].
- `implements` – реалізація архітектурного рішення: [[JsonStorage]] → [[ADR-001-Local-JSON]].
- `validates` – перевірка значень предметного поняття: [[TaskModel]] → [[TaskStatus]], [[TaskPriority]], [[DueDate]].
- `persists_to` – запис через сховище: [[TaskService]] → [[JsonStorage]].

## Конвенція запису зв'язків

Тип відношення зберігається як окреме YAML-поле, значення – масив **рядків**, що містять wiki-посилання:

```yaml
---
type: component
depends_on:
  - "[[TaskModel]]"
persists_to:
  - "[[JsonStorage]]"
---
```

Wiki-посилання у тексті забезпечує навігацію, а типізоване поле дає агенту семантику відношення. Поля внесено до [[CLI]], [[TaskService]], [[TaskModel]] і [[JsonStorage]].
