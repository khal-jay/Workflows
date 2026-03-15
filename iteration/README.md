# Iteration

How the system improves over time. Every change you make to a validated system lives here.

This is your changelog for decisions — not for code diffs, but for *why* things changed.

## When to add an entry

Every time you improve a validated system. Even small changes.

## Template

Create a new file: `YYYY-MM-DD-<system-slug>-v<N>.md`

---

```markdown
# [System Name] — Iteration v[N]

## Linked Validation
`../validation/YYYY-MM-DD-<system-slug>.md`

## What Changed
Describe the improvement. One paragraph.

## Why This Change
What signal triggered it? (metric drop, user feedback, new constraint)

## Hypothesis
If I make this change, [metric] will move from [X] to [Y].

## What Was Kept
What worked and shouldn't be touched?

## New Success Threshold
Updated target for this iteration.

## Review Date
When will you evaluate if this change worked?
```

---

## Iteration Rhythm

A healthy system improves on a regular cadence. Suggested review schedule:

| System Type | Review Cadence |
|-------------|---------------|
| Live product feature | Weekly for first month, then monthly |
| Internal tool or workflow | Monthly |
| Research / ML experiment | After each run |
| Foundational infrastructure | Quarterly |
