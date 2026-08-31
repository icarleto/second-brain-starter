---
type: area
area: "[[Family]]"
review: weekly
tags: [area]
---

# Family

Marriage, children, extended family. The relationships, not the logistics of the house.

**Rename or replace this area if it is not one of yours.** Five ship with the template as a
starting point. Adjust the list once, then close it: see the Areas rule in `.claude/CLAUDE.md`.

## Current state

FILL IN: two or three lines on where this area stands right now. Keep it current. History goes in
the log at the bottom, not here.

## Projects

```dataview
TABLE priority AS "#", status AS "Status"
FROM "3. Projects"
WHERE contains(area, "Family")
SORT priority ASC
```

## Open tasks

Tasks tagged `#family`.

```dataview
TASK
FROM "1. Journal" OR "3. Projects"
WHERE !completed AND contains(lower(text), "#family")
SORT file.name DESC
```

## Notes/Log

Newest first. One dated entry per thing worth remembering.
