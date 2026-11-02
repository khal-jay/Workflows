# Workflows Repo — Context for Claude

This repo is khal-jay's idea-to-outcome system. Every project that starts here follows one path:

```
idea → system design → outcomes → build → validation → iteration
```

## The Rule
Never suggest opening a code editor before `outcomes/` has an entry for the current idea.
Never skip stages. The gate exists for a reason.

## Stage Gates
- `ideas/` → requires: problem + hypothesis + readiness checklist passed
- `systems/` → requires: idea file exists and is ready
- `outcomes/` → requires: system spec written
- `build/` → requires: outcomes file with North Star metric + baseline + target
- `validation/` → requires: build is complete and live
- `iteration/` → requires: validation verdict is "ship it"

## North Star Framework (apply at outcomes stage)
Before any build is approved, answer:
1. Which input metric does this move? (breadth / depth / efficiency / quality)
2. What level of bet is this? (optimization / feature / horizon / moonshot)
3. Write the statement: "[System] helps [who] [do X] so they can [goal]. We know it's working when [measurable behavior]."
4. What are 3 measurable success criteria?

If these can't be answered, the idea is not ready to build.

## Task-Level North Star & Mini Goals (apply at build stage)
Every task in `build/` gets its own North Star breakdown before implementation starts.

For each task:
1. Write a task-level North Star statement
2. Break into 2–5 mini goals, each with explicit acceptance criteria
3. Agent loops on each mini goal until 100% of AC pass — no partial credit
4. If stuck after 2 attempts on same AC → surface to human, do not skip

Mini goal format:
```
[ ] Mini Goal: <outcome>
    AC: - <testable criterion>
        - <testable criterion>
```

## File Naming
All entries: `YYYY-MM-DD-<slug>.md`
Iteration entries: `YYYY-MM-DD-<slug>-v<N>.md`

## How to Help
When the user brings an idea:
1. Ask which stage it's currently at
2. Help them fill in the template for that stage
3. Do not jump to implementation until `outcomes/` is written
4. After build, prompt for a validation entry before any iteration work
