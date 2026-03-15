# Workflow Kit Portability — Success Criteria

## Linked System
`../systems/2026-03-15-workflow-kit-portability.md`

## North Star Statement
workflow-kit helps khal-jay restore his complete dev environment on any new device so he can start productive work immediately.
We know it's working when a full environment restore takes under 15 minutes on a new machine.

## North Star Metric
**Time to first productive Claude Code session on a new machine** (target: ≤15 min)

## Input Metrics

| Metric | Current Baseline | Target | How Measured |
|--------|-----------------|--------|--------------|
| Setup time on new device | ~4 hours (manual) | ≤15 min | Timed dry run |
| % of tools restored automatically | ~30% | 100% | Checklist after bootstrap |
| Steps requiring manual action | ~20 | ≤3 (tokens + MCP keys) | Count during dry run |
| Agents available after bootstrap | 3 (global) | 12 + 144 agency | `ls ~/.claude/agents/ \| wc -l` |

## What Level of Bet Is This?
- [x] Optimization — solves a real pain with low implementation risk

## Success Threshold
On a fresh machine: run `bootstrap.sh`, open Claude Code in any project, and `/plan-ceo-review` + all 12 agents are available within 15 minutes. Only tokens and MCP keys require manual entry.

## Failure Signal
Bootstrap takes >30 minutes, or more than 3 manual steps are required beyond filling in `.env`.

## Measurement Plan
Dry run: use a second user account on this Mac to simulate a new machine. Time the full bootstrap. Check agent count and skill availability. Review date: immediately after first build.

## Ready to Build?
- [x] North Star metric defined
- [x] Baseline measured
- [x] Target is specific and time-bound
- [x] Measurement plan is in place
