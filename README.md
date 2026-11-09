# LLM Wiki starter

The Demo repo of the wellgent.ai workshop [Coordinate agentic work with wayfinder](https://wellgent.ai/workshops/2026-11-12-coordinate-agentic-work-with-wayfinder): a context repo with the workshop's wayfinder setup already applied.

In the session, a wayfinder map is charted for a personal [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f), Andrej Karpathy's pattern of markdown pages an agent keeps current from your notes.
The wiki is the example, and wayfinder is the subject.
The repo starts almost empty on purpose, since the map decides its structure.
Registrants find the setup, step by step, in the wellgent.ai Classroom.

## What the session shows

1. The kickoff with `/wayfinder` charts the map and its first tickets and starts research in the background, all visible on GitHub.
2. Each fresh session with `/wayfinder` and the map link claims the next ticket and works it to a decision.
3. Each decision lands on its ticket and on the map, and unblocks the tickets waiting on it.

## Follow along

1. Click **Use this template**, create the repo under your own account, set it to **Private**, and clone it.
2. Ask your agent to create the five `wayfinder:` labels on your copy, as in step 4 of the setup. The copy already has the skills, the docs and the conventions, but GitHub copies no labels from a template.
3. Start Claude Code or Codex in your copy and paste the kickoff prompt. In Codex, type `$wayfinder` in place of `/wayfinder`.

```
/wayfinder I want to build my own LLM Wiki in this repo, after Karpathy's pattern: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f. Help me work out what it should hold and how to set it up, and then let's build a first version together.
```

4. Work the map one ticket per fresh session with `/wayfinder` and the map's link.

## What is in this repo

- `AGENTS.md` - What this repo is for and how to work in it, with the planning workflow and the agent skills sections. `CLAUDE.md` points Claude Code to it.
- `.agents/skills/` - The eight skills from Matt Pocock that the setup installs: wayfinder, grilling, domain-modeling, research, prototype, setup-matt-pocock-skills, wizard and writing-for-agents, recorded in `skills-lock.json`. `.claude/skills/` links to them, so Claude Code and Codex both load them.
- `docs/agents/` - The issue tracker and domain docs for a wiki on GitHub Issues, with the setup's conventions.
- `research/` - Research records, one per research ticket, in the shape its `README.md` gives.
