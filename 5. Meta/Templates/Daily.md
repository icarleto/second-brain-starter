---
type: daily
date: {{date:YYYY-MM-DD}}
processed: false
---

# {{date:YYYY-MM-DD}}

## Priorities

Live top ten from [[5. Meta/Priority Ranking]]. Reorder there by dragging rows, not here.

```dataviewjs
const text = await dv.io.load("5. Meta/Priority Ranking.md");
const rows = [];
if (text) {
    const lines = text.split("\n");
    const headerIdx = lines.findIndex(l => l.trim().startsWith("|") && l.includes("Project") && l.includes("Area"));
    if (headerIdx !== -1) {
        for (let i = headerIdx + 2; i < lines.length; i++) {
            const line = lines[i];
            if (!line.trim().startsWith("|")) break;
            const cells = line.split("|").slice(1, -1).map(c => c.trim());
            if (cells.length >= 3) rows.push(cells);
            if (rows.length >= 10) break;
        }
    }
}
if (rows.length === 0) {
    dv.paragraph("*Could not load Priority Ranking. Open [[5. Meta/Priority Ranking]] directly.*");
} else {
    dv.table(["Project", "Area", "Why it ranks here"], rows);
}
```

## Notes

Write as you go, one heading per project you actually touched today. Messy is correct here.
Do not sort it and do not decide where anything belongs. That is the job you are handing off.

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
