# Systems

Formal system specs. This is where an idea becomes a design. You write this before writing any code.

## When to add an entry

After an idea in `../ideas/` has passed its readiness checklist.

## Template

Create a new file: `YYYY-MM-DD-<system-slug>.md`

---

```markdown
# [System Name] — Spec

## Linked Idea
`../ideas/YYYY-MM-DD-<idea-slug>.md`

## What This System Does
One clear sentence.

## Components
List every piece: UI screens, API endpoints, data stores, integrations, background jobs.

## Data Flow
How does data move through the system? Start → middle → end.

## Interfaces
What does this system expose? What does it depend on?

## Edge Cases
What can go wrong? How does the system behave?

## Out of Scope (v1)
What are you explicitly NOT building yet?

## Open Questions
Anything unresolved that could block implementation.

## Ready to Build?
- [ ] Every component is named
- [ ] Data flow is clear
- [ ] Edge cases are handled or deferred
- [ ] Outcomes defined in `../outcomes/`

Next step: define success criteria in `../outcomes/` before opening a code editor.
```
