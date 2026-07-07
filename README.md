# HADR Monitor

Starter repository for a three-day course in which you build an **autonomous
monitoring agent for humanitarian assistance and disaster response (HADR)**
using Claude Code.

This repo is a template: it contains feed documentation, empty scaffolding and
conventions — but no working code. You (and the agent you direct) write
everything else over the three days.

## What you will build

An agent that:

- **watches live disaster feeds** — GDACS, USGS and ReliefWeb (endpoint notes
  and open questions for each are in `feeds/`)
- **filters and assesses** — separates signal from noise, then works out what
  happened, where, how severe it is, and who is affected
- **publishes a morning situation report** — a rendered `dashboard.html`,
  refreshed at 08:30 Singapore time
- **runs unattended** — on a schedule, without supervision, and stays quiet
  when nothing has changed

How it does any of that is deliberately not specified anywhere in this
repository. Deciding the how — the pipeline, the data model, the judgement
calls — is the course.

## The three days

1. **Plan** — interrogate the feeds, write the PRD, cut it into vertical slices
2. **Autonomy** — build the first slice, write a skill, wire up the 08:30
   routine, launch the overnight loop
3. **Trust** — review code you didn't write, harden the pipeline, demo

## Repository layout

| Path | Purpose |
|------|---------|
| `feeds/` | Documentation for the three live feeds: endpoints, example responses, and open questions your design must answer |
| `scripts/` | Deterministic checks — anything that must give the same answer twice does not belong in a prompt |
| `skills/` | Skills you write on Day 2, one folder per skill |
| `docs/solutions/` | One learning per file — fixes that cost more than ten minutes go here so no future session pays twice |
| `implementation-notes.md` | Kept by the agent, reviewed by you: decisions, open questions, deviations |
| `CLAUDE.md` | Project instructions for the agent — fill this in before your first prompt |

## Artefacts expected by the end

`prd.html` · `system-view.html` · `implementation-notes.md` · `dashboard.html`
· `goal.md` · at least one skill

## Day 1 setup

1. Sign in to Claude Code with your Team seat
2. Create your own repository from this template, then clone it
3. Run `/install-github-app` so @claude reviews your pull requests from Day 2
4. Install OpenCode and sign in with your Go key

Fill in `CLAUDE.md` before your first prompt.
