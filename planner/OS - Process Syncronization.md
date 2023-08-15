---
type: planner
Planner_Type: Revision
subject: OS
Topic:
  - Process Syncronization
Source: UaNotes
ID: 4
---

## Stack
1. Notes

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