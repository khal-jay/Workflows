# Ideas

Raw idea capture. Write fast, don't filter. The goal here is to get the problem out of your head and onto paper.

## When to add an entry

Any time you have an idea worth exploring. Even half-formed ones. Especially half-formed ones.

## Template

Create a new file: `YYYY-MM-DD-<idea-slug>.md`

---

```markdown
# [Idea Name]

## The Problem
What's broken, slow, painful, or missing? Who feels it?

## The Hypothesis
If I build [X], then [Y] will improve because [Z].

## Why Now
What makes this worth solving at this moment?

## First Instinct on Approach
One sentence. Don't overthink it yet.

## Ready to Move Forward?
- [ ] Problem is clearly stated
- [ ] Hypothesis is testable
- [ ] I know what "working" looks like (roughly)

Next step: create a file in `../systems/` to design the solution.
```

---

## Example

```markdown
# COD Reconciliation Speed

## The Problem
Operators spend 15+ minutes closing end-of-day books because COD
status tracking is manual and scattered across WhatsApp and spreadsheets.

## The Hypothesis
If I build a single reconciliation view with status transitions
(expected → collected → remitted), operators can close books in under 5 minutes.

## Why Now
Payment errors are creating trust issues with delivery partners.

## First Instinct on Approach
A reconciliation screen in the Syncoria app with bulk status update.

## Ready to Move Forward?
- [x] Problem is clearly stated
- [x] Hypothesis is testable
- [x] I know what "working" looks like (roughly)
```
