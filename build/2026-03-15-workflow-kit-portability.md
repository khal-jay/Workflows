# Workflow Kit Portability — Build Log

## Linked Spec
`../systems/2026-03-15-workflow-kit-portability.md`

## Linked Outcomes
`../outcomes/2026-03-15-workflow-kit-portability.md`

## Implementation Location
`~/workflow-kit/` — local git repo

## What Was Built
- `~/workflow-kit/` — versioned dotfiles repo, git initialized
- `claude/CLAUDE.md` — global rules file (workflow order, North Star framework, agent roster, slash commands)
- `claude/agents/` — 12 globally-scoped, merged agents (see agent list below)
- `claude/settings.json` — copied from current `~/.claude/settings.json`
- `shell/.zshrc` — sanitized (tokens load from `.env`, not hardcoded)
- `shell/.gitconfig`, `shell/.npmrc` — copied and sanitized
- `tools/gstack` — git submodule (garrytan/gstack) — 8 slash commands
- `tools/agency-agents` — git submodule (msitarzewski/agency-agents) — 144+ specialists
- `tools/autoresearch` — git submodule (karpathy/autoresearch) — GPU overnight ML
- `bootstrap.sh` — one-command restore for new machine
- `.env` / `.env.example` / `.gitignore` / `plugins.txt`
- Symlinks created: `~/.claude/CLAUDE.md`, `~/.claude/settings.json`, all 12 agents

## 12 Global Agents Built

| Agent | Based On | Key Change |
|-------|----------|------------|
| orchestrator | Wakkytails orchestrator | Removed Wakkytails-specific file refs |
| product-manager | Wakkytails PM + Syncoria TPM | Merged planning + feasibility + North Star gate |
| system-architect | Wakkytails architect | Removed product-specific services |
| senior-fullstack-engineer | Syncoria fullstack | Kept as-is (Opus model) |
| backend-engineer | Wakkytails backend | Generalized away from Paystack/Wakkytails |
| code-reviewer | Global codereviewer + Wakkytails reviewer | Added scope-discipline guardrail |
| security-analyst | Wakkytails security | Generalized to any payment gateway |
| qa-engineer | Wakkytails QA + global mobile-app-tester | Merged mobile test tiers |
| product-designer | Global productdesigner + Wakkytails design-agent | Added UX state + token audit |
| devops-engineer | Wakkytails devops | Generalized to any deploy platform |
| code-analyst | Syncoria codeanalyst | Kept as-is |
| research-agent | Wakkytails research | Generalized, added North Star statement work |

## Key Decisions Made During Build
- Used symlinks (not copies) for `~/.claude/` — any edit to `~/workflow-kit/` is instantly live
- `.env` holds all tokens — `.zshrc` sources it at startup — no hardcoded secrets anywhere
- Agency-agents copied (not symlinked) to `~/.claude/agents/` since they're read-only reference files
- Old global agents (`codereviewer.md`, `mobile-app-tester.md`, `productdesigner.md`) left in place — they'll be superseded by the new ones but don't conflict

## What Was Deferred
- Running `gstack/setup` to build the browser binary (requires Bun — can run manually: `cd tools/gstack && ./setup`)
- MCP server key setup (manual per machine — Figma, GitHub, Expo)
- Removing old project-level agent folders from Wakkytails and SYNCORIA (clean-up task, low priority)

## Known Issues
- `ls ~/.claude/agents/ | wc -l` shows 28 entries (not 150+) because agency-agents installs directories, not individual files. The agents inside those dirs are still accessible by Claude.

## Build Complete?
- [x] Core functionality implemented
- [x] Edge cases handled or explicitly deferred
- [x] Ready for validation
