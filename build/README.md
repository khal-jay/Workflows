# Build

Implementation artifacts. Code lives in project repos — this folder holds context, decisions, and notes about what was built and why.

## When to add an entry

When you start building. Create one file per system being implemented.

## Template

Create a new file: `YYYY-MM-DD-<system-slug>.md`

---

```markdown
# [System Name] — Build Log

## Linked Spec
`../systems/YYYY-MM-DD-<system-slug>.md`

## Linked Outcomes
`../outcomes/YYYY-MM-DD-<system-slug>.md`

## Implementation Location
Where does this live? (repo path, branch, PR link)

## Key Decisions Made During Build
What changed from the spec? Why?

## What Was Deferred
Anything kicked to v2 during implementation?

## Known Issues
Bugs or rough edges left for after validation.

## Build Complete?
- [ ] Core functionality implemented
- [ ] Edge cases handled (or explicitly deferred)
- [ ] Ready for validation
```
