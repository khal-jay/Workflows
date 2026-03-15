# Workflows — Idea to Outcome

This repo is a system-building workspace. Every folder represents one stage of taking an idea from raw thought to a working system with measurable results.

## The Flow

```
idea → system design → outcomes → build → validation → iteration
```

Each stage has its own folder. Work moves forward in order — no skipping.
`build/` doesn't open until `outcomes/` is written. `validation/` doesn't open until the build is live. `iteration/` doesn't open until validation gives a "ship it" verdict.

## Folder Map

| Folder | Purpose |
|--------|---------|
| `ideas/` | Raw idea capture. Unfiltered. Problem + hypothesis only. |
| `systems/` | Formal system specs. Architecture, components, data flow. |
| `outcomes/` | Measurable success criteria. North Star metric + input metrics. |
| `build/` | Implementation artifacts. Code, configs, integrations, notes. |
| `validation/` | Evidence of results. Did the system do what it was supposed to? |
| `iteration/` | What changed and why. Log of improvements over time. |

## The Rule

**Never build before you can state what success looks like.**

If you can't write an entry in `outcomes/` first, the idea isn't ready to build yet.

## File Naming

Use `YYYY-MM-DD-<idea-name>.md` for all entries. This keeps everything chronological and findable.

Example: `2026-03-15-cod-reconciliation-speed.md`
