# Workflow Kit Portability — Spec

## Linked Idea
`../ideas/2026-03-15-workflow-kit-portability.md`

## What This System Does
A versioned dotfiles-style repo that restores the complete dev workflow (Claude agents, skills, shell config, MCP servers) on any new machine with one command.

## Components
- `~/workflow-kit/` — local git repo (the single source of truth)
- `claude/CLAUDE.md` — global rules file, symlinked to `~/.claude/CLAUDE.md`
- `claude/agents/` — 12 globally-scoped agents, symlinked to `~/.claude/agents/`
- `claude/settings.json` — permissions + plugins, symlinked to `~/.claude/settings.json`
- `shell/.zshrc`, `.gitconfig`, `.npmrc` — symlinked to `~/`
- `tools/gstack/` — git submodule, `./setup` builds binary + symlinks skills
- `tools/agency-agents/` — git submodule, 144+ specialist personas
- `tools/autoresearch/` — git submodule (GPU PC only)
- `bootstrap.sh` — one-command setup for new machine
- `.env` — all secrets (gitignored)
- `plugins.txt` — list of Claude Code plugins to install

## Data Flow
New machine → clone repo → run `bootstrap.sh` → script loads `.env`, inits submodules, creates symlinks, installs plugins, runs `gstack/setup` → `~/.claude/` is fully populated → open any project in Claude Code → all tools active

## Interfaces
- **Exposes:** `~/.claude/CLAUDE.md`, `~/.claude/agents/`, `~/.claude/skills/`, `~/.claude/settings.json`
- **Depends on:** Claude Code installed, Homebrew, git, Bun (for gstack build)

## Edge Cases
- `.env` not filled in → bootstrap warns and exits
- gstack `./setup` fails → Bun not installed; bootstrap should check
- Agency-agents subdir structure changes → cp command may miss folders; handle with wildcard

## Out of Scope (v1)
- MCP API keys (too sensitive — set up manually per machine)
- Supabase plugin (project-scoped, install per-project)
- autoresearch model outputs (GPU-machine only, large files)
- Remote git hosting (local-only for now)

## Open Questions
- None — spec is complete

## Ready to Build?
- [x] Every component is named
- [x] Data flow is clear
- [x] Edge cases are handled or deferred
- [x] Outcomes defined in `../outcomes/2026-03-15-workflow-kit-portability.md`
