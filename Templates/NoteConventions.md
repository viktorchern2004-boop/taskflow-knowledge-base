---
type: guide
created: 2026-11-12
tags:
  - taskflow
  - templates
---

# NoteConventions – правила нотаток

## Структура vault
- Concepts – поняття предметної області.
- Components – програмні модулі.
- Decisions – архітектурні рішення.
- Glossary – термінологія.
- [[MOC-TaskFlow]] – навігаційна карта всіх нотаток.

## Іменування
Назви змістовні й узгоджені зі складовими застосунку, без випадкових скорочень. Усі нотатки містять YAML frontmatter з полями type, created, tags, а зв'язки оформлено wiki-посиланнями на точні назви нотаток.

## Шаблони frontmatter
**Concept**
```yaml
---
type: concept
created: 2026-11-12
tags: [taskflow, concept]
---
```

**Component**
```yaml
---
type: component
created: 2026-11-12
tags: [taskflow, component]
---
```

**Decision**
```yaml
---
type: decision
created: 2026-11-12
tags: [taskflow, decision, adr]
---
```

**Glossary**
```yaml
---
type: glossary
created: 2026-11-12
tags: [taskflow, glossary]
---
```

Починаючи з ПР3, агент отримує доступ до vault тільки через MCP-конектор, а не відкриваючи цю папку як робочу директорію.