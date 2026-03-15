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

## File Naming
All entries: `YYYY-MM-DD-<slug>.md`
Iteration entries: `YYYY-MM-DD-<slug>-v<N>.md`

## How to Help
When the user brings an idea:
1. Ask which stage it's currently at
2. Help them fill in the template for that stage
3. Do not jump to implementation until `outcomes/` is written
4. After build, prompt for a validation entry before any iteration work
