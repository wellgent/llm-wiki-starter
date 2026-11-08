# LLM Wiki starter

The Demo repo of the wellgent.ai workshop [Coordinate agentic work with wayfinder](https://wellgent.ai/workshops/2026-11-12-coordinate-agentic-work-with-wayfinder). It is a context repo with the workshop's wayfinder Setup already applied, and the example it plans is a personal LLM Wiki.

The example itself doesn't matter. It shows the Setup working: how a map forms, how tickets wait on each other, and how one session works one ticket. Registrants find the Setup, step by step, in the wellgent.ai Classroom.

## The example

An [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f), the pattern Andrej Karpathy describes, is a folder of markdown pages an agent writes and keeps current from your notes. This repo starts almost empty on purpose: the map decides its structure.

## What the session shows

1. The kickoff prompt charts the map: the map issue with its Destination, Notes and first tickets, and research starting in the background.
2. On GitHub: the sub-issues, the "blocked by" links and the open edge of the map.
3. A fresh session with `/wayfinder` and the map link claims the next ticket and works one grilling ticket to its decision.
4. The decision on the ticket, the pointer on the map, and the ticket it unblocked.

## Follow along

1. Click **Use this template**, create the repo under your own account, set it to **Private**, and clone it.
2. Ask your agent to create the five `wayfinder:` labels on your copy, as in step 4 of the Setup. A template copy has none, and wayfinder needs them.
3. Start Claude Code or Codex in your copy, type `/wayfinder` (or `$wayfinder` in Codex) and paste the kickoff prompt:

```
The destination is the first MVP of my personal LLM Wiki, built in this repo, following Karpathy's LLM Wiki pattern: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f. My notes and projects are scattered across folders on this computer, and I will point you at them. First research how to set up an LLM Wiki: structure, workflows and tools. Then grill me on what to include. Then plan the tasks that gather and ingest my sources. This map carries execution: its tasks build the wiki in this repo, and it ends when the MVP wiki is in place.
```

4. Work the map one ticket per fresh session with `/wayfinder` and the map's link.

## What is in this repo

- `AGENTS.md` - what this repo is for and how to work in it, with the planning workflow and the agent skills sections. `CLAUDE.md` points Claude Code to it.
- `.agents/skills/` - Matt Pocock's skills the Setup installs: wayfinder, grilling, domain-modeling, research, prototype and setup-matt-pocock-skills, pinned in `skills-lock.json`. `.claude/skills/` links to them, so Claude Code and Codex both load them.
- `docs/agents/` - the issue tracker and domain docs `/setup-matt-pocock-skills` writes for GitHub, plus the Setup's conventions.
