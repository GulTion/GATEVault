---
type: planner
---

## Short Notes
```dataview
TABLE from "notes"
WHERE this.file.frontmatter.ID=file.frontmatter.PID
```

## Questions List
```dataview
TABLE from "questions"
WHERE this.file.frontmatter.ID=file.frontmatter.PID
```