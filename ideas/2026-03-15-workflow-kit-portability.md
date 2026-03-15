# Workflow Kit Portability

## The Problem
Every time I move to a new device, I have to rebuild my entire dev workflow from scratch — Claude Code plugins, agents, shell config, MCP servers, gstack tools. It takes hours and things get missed. The workflow only lives on one machine.

## The Hypothesis
If I create a single versioned repo (`workflow-kit`) with all configs symlinked and a one-command bootstrap script, I can restore my full workflow on any new device in under 15 minutes.

## Why Now
I'm actively working across multiple projects. A device failure or migration would set me back a full day. The cost of not having this is too high.

## First Instinct on Approach
Dotfiles-style repo at `~/workflow-kit` with git submodules for gstack, agency-agents, and autoresearch. `bootstrap.sh` handles everything.

## Ready to Move Forward?
- [x] Problem is clearly stated
- [x] Hypothesis is testable
- [x] I know what "working" looks like (roughly)

Next step: `../systems/2026-03-15-workflow-kit-portability.md`
