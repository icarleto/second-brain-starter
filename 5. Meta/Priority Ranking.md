---
type: meta
status: reference
tags: [meta]
---

# Priority Ranking

One ordered list of everything active, so the daily note and the dashboards agree about what
matters instead of each having an opinion.

**This is a view, not a list you maintain by hand.** The order comes from the `priority:` number in
each project's own frontmatter. To reorder, change the number on the project. Editing this note
does nothing.

That indirection is deliberate. A hand-maintained ranking here would be a second copy of
information that already exists, and the two would disagree within a week.

```dataview
TABLE priority AS "#", area AS "Area", status AS "Status"
FROM "3. Projects"
WHERE type = "project" AND status = "active"
SORT priority ASC
```

## Projects with no priority set

These will not appear above. Give them a `priority:` number or accept that they are invisible to
every ranked view.

```dataview
TABLE area AS "Area"
FROM "3. Projects"
WHERE type = "project" AND status = "active" AND !priority
```
