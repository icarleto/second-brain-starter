---
type: area
area: "[[Discipline]]"
review: weekly
tags: [area]
---

# Discipline

Health, fitness, sleep, habits, and the standards you are holding yourself to. Concrete and numeric beats aspirational.

**Rename or replace this area if it is not one of yours.** Five ship with the template as a
starting point. Adjust the list once, then close it: see the Areas rule in `.claude/CLAUDE.md`.

## Current state

FILL IN: two or three lines on where this area stands right now. Keep it current. History goes in
the log at the bottom, not here.

## Projects

```dataview
TABLE priority AS "#", status AS "Status"
FROM "3. Projects"
WHERE contains(area, "Discipline")
SORT priority ASC
```

## Open tasks

Tasks tagged `#discipline`.

```dataview
TASK
FROM "1. Journal" OR "3. Projects"
WHERE !completed AND contains(lower(text), "#discipline")
SORT file.name DESC
```

## Notes/Log

Newest first. One dated entry per thing worth remembering.
