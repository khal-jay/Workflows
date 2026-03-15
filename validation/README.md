# Validation

Evidence of results. Did the system produce the outcomes it was designed to produce?

This is the moment of honest assessment. No rationalizing.

## When to add an entry

After the system has been live long enough to collect meaningful data. This could be hours (a quick feature) or weeks (a behavioural change).

## Template

Create a new file: `YYYY-MM-DD-<system-slug>.md`

---

```markdown
# [System Name] — Validation

## Linked Outcomes
`../outcomes/YYYY-MM-DD-<system-slug>.md`

## Validation Date
When was this reviewed?

## Data Collected

| Metric | Baseline | Target | Actual | Delta |
|--------|----------|--------|--------|-------|
| | | | | |

## Did It Work?
- [ ] Yes — hit or exceeded the success threshold
- [ ] Partial — moved the metric but missed the target
- [ ] No — did not move the needle
- [ ] Too early to tell — need more time/data

## What the Data Says
Interpret the numbers. What actually happened?

## What Surprised You
Anything unexpected — positive or negative?

## Decision
- [ ] Ship it — system is working, move to iteration
- [ ] Rework — go back to systems/ with new constraints
- [ ] Kill it — not worth the continued investment

## Next Step
`../iteration/` if shipping, new `../ideas/` entry if reworking.
```
