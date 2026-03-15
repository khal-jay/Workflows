# How to Use This Repo (Day to Day)

## The Golden Rule

**Never open a code editor before you've written an entry in `outcomes/`.**

If you can't state what success looks like, you're not ready to build.

---

## Starting a New Idea

1. Create `ideas/YYYY-MM-DD-<slug>.md`
2. Fill in: the problem, the hypothesis, why now
3. Check the readiness checklist at the bottom
4. If all boxes are checked → move to step 2

## Designing the System

1. Create `systems/YYYY-MM-DD-<slug>.md`
2. Name every component, define the data flow, list edge cases
3. Write out what's explicitly out of scope for v1
4. If the spec is solid → move to step 3

## Defining Success

1. Create `outcomes/YYYY-MM-DD-<slug>.md`
2. Write the North Star statement
3. Set a specific, measurable target with a baseline
4. Define what "failure" looks like too
5. If you have a measurement plan → you're ready to build

## Building

1. Create `build/YYYY-MM-DD-<slug>.md`
2. Link it to the spec and outcomes
3. Log key decisions made during implementation
4. Note anything deferred — don't let it disappear
5. When the core is done → validate

## Validating

1. Create `validation/YYYY-MM-DD-<slug>.md`
2. Fill in the actual numbers vs targets
3. Make a clear decision: ship / rework / kill
4. No ambiguity — one of those three, always

## Iterating

1. Create `iteration/YYYY-MM-DD-<slug>-v<N>.md`
2. State what changed, why, and what you expect
3. Set a review date
4. Repeat

---

## Weekly Habit (5 minutes)

Every week, ask:
1. Do any ideas in `ideas/` have all their readiness boxes checked but no system spec yet?
2. Do any systems in `systems/` have no outcomes file yet?
3. Are any builds waiting for validation data?
4. Is any validated system overdue for an iteration review?

If yes to any — do that first before starting anything new.

---

## File Naming

Always: `YYYY-MM-DD-<short-descriptive-slug>.md`

The date is when you created the entry, not when the work is done. This makes the folder chronological and auditable.
