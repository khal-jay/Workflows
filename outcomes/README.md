# Outcomes

Measurable success criteria. Written before building starts. This is what "done" actually means.

Without this file, you have no way to know if the system worked.

## When to add an entry

After `../systems/` is written, before anything in `../build/` is created.

## Template

Create a new file: `YYYY-MM-DD-<system-slug>.md`

---

```markdown
# [System Name] — Success Criteria

## Linked System
`../systems/YYYY-MM-DD-<system-slug>.md`

## North Star Statement
[Product/system] helps [who] [do X] so they can [goal].
We know it's working when [specific measurable behavior].

## North Star Metric
One number. What moves when the system is succeeding?

## Input Metrics
The levers that drive the North Star. (3-5 max)

| Metric | Current Baseline | Target | How Measured |
|--------|-----------------|--------|--------------|
| | | | |

## What Level of Bet Is This?
- [ ] Optimization — low risk, fast validation
- [ ] Feature bet — improves existing workflow
- [ ] Horizon bet — new capability
- [ ] Moonshot — changes the model

## Success Threshold
What's the minimum result that proves this was worth building?

## Failure Signal
What would tell you to stop and rethink?

## Measurement Plan
How will you collect this data? When will you review it?

## Ready to Build?
- [ ] North Star metric defined
- [ ] Baseline measured
- [ ] Target is specific and time-bound
- [ ] Measurement plan is in place
```
