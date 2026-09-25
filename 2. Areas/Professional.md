---
type: area
area: "[[Professional]]"
review: weekly
tags: [area]
---

# Professional

All work and income, across every employer, client and side venture. One area, however many sources.

**Rename or replace this area if it is not one of yours.** Five ship with the template as a
starting point. Adjust the list once, then close it: see the Areas rule in `.claude/CLAUDE.md`.

## Current state

FILL IN: two or three lines on where this area stands right now. Keep it current. History goes in
the log at the bottom, not here.

## Projects

```dataview
TABLE status AS "Status"
FROM "3. Projects"
WHERE contains(area, "Professional")
SORT file.name ASC
```

## Open tasks

Tasks tagged `#professional`.

```dataview
TASK
FROM "1. Journal" OR "3. Projects"
WHERE !completed AND contains(lower(text), "#professional")
SORT file.name DESC
```

## Notes/Log

Newest first. One dated entry per thing worth remembering.
