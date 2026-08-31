---
type: daily
date: {{date:YYYY-MM-DD}}
processed: false
---

# {{date:YYYY-MM-DD}}

## Priorities

Active projects, highest priority first. Reorder by editing the `priority:` number in a
project's own frontmatter, not here. This table is a view, never a place to type.

```dataview
TABLE priority AS "#", area AS "Area", file.mtime AS "Touched"
FROM "3. Projects"
WHERE type = "project" AND status = "active"
SORT priority ASC
LIMIT 10
```

## Notes

Write as you go, one heading per project you actually touched today. Messy is correct here.
Do not sort it, do not decide where anything belongs. That is the job you are handing off.

###

## Tasks

- [ ]

---

## Open tasks everywhere

```dataview
TASK
FROM "1. Journal" OR "3. Projects"
WHERE !completed
SORT file.name DESC
```
