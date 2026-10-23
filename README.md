# LLM Wiki starter

A starting point for your own LLM Wiki, set up with Claude Code and planned with wayfinder.

## What an LLM Wiki is

An LLM Wiki is a folder of plain markdown pages that an AI agent writes and keeps current for you.
You choose the sources, such as notes, documents, articles and project files.
The agent reads each source and works what it learns into the wiki.
It updates the pages that already exist, links related pages and flags where new information contradicts old.
You read the wiki and ask it questions.
Because the agent does the upkeep, the wiki keeps growing instead of going stale.

Andrej Karpathy describes the pattern in [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).
Read it once before you start.

## Who this is for

This starter is for you if your notes and projects are spread across folders, apps and repos.
Nothing ties them together, so every new agent session starts without knowing your context.

The repo starts almost empty on purpose.
It does not choose a folder layout, tools or what goes in.
You decide that with your agent, through a wayfinder map.
Wayfinder is a planning skill by Matt Pocock.
It turns a big, unclear goal into a list of questions on GitHub Issues and works through them one at a time.
Your map will research how to set up an LLM Wiki, ask you what to include, and then gather and ingest your sources.

## What you need

- A Mac or a Linux computer. On Windows, use [WSL](https://learn.microsoft.com/windows/wsl/install) and run every command in its terminal.
- A GitHub account.
- A paid Claude plan. Claude Code needs Pro, Max, Team or Enterprise. The free plan does not include it.
- [Node.js](https://nodejs.org) 22 or newer, used once to install the skills.

## Steps

### 1. Install Claude Code and the GitHub CLI, and sign in

Install Claude Code:

```sh
curl -fsSL https://claude.ai/install.sh | bash
claude auth login
```

Install the GitHub CLI from [cli.github.com](https://cli.github.com).
On a Mac with Homebrew, that is `brew install gh`.
Then sign in:

```sh
gh auth login
```

### 2. Make your own private copy

At the top of this page, click **Use this template**, then **Create a new repository**.
Pick your own account as the owner and give the repo a name, such as `my-wiki`.
Set it to **Private**.
Your notes will go into this repo, so it must stay private.
Your copy keeps the map's issues too, so leave issues turned on.

### 3. Clone your copy

```sh
gh repo clone <your-account>/my-wiki
cd my-wiki
```

### 4. Install the skills

This installs the exact versions pinned in `skills-lock.json` into `.claude/skills/`:

```sh
npx -y skills@1.7.2 add mattpocock/skills#24fe0ef7737efae15c87225755e9f6f5965e4888 \
  --skill wayfinder --skill grilling --skill domain-modeling \
  --skill research --skill prototype --skill setup-matt-pocock-skills \
  --agent claude-code --yes
```

### 5. Check your setup

```sh
scripts/check-prep
```

Each line says PASS or FAIL.
Every FAIL line comes with the command that fixes it.
Fix them and run the script again until everything passes.

### 6. Open Claude Code in the repo

```sh
claude
```

### 7. Connect the skills to GitHub Issues

In Claude Code, type:

```
/setup-matt-pocock-skills
```

When it asks where issues live, choose GitHub.
Accept the recommended answer for the other questions.
It writes a few small config files, which you can commit.

### 8. Start the map

Type `/wayfinder`, a space, and then paste the kickoff prompt below as one message.

```
The destination is the first MVP of my personal LLM Wiki, built in this repo, following Karpathy's LLM Wiki pattern: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

My notes and projects are scattered across folders on this computer, and I will point you at them.
First research how to set up an LLM Wiki: structure, workflows and tools.
Then grill me on what to include.
Then plan the tasks that gather and ingest my sources.

This map carries execution.
Its tasks build the wiki in this repo, and it ends when the MVP wiki is in place.
```

Claude creates the map as a GitHub issue, with a child issue for each question it can see so far.
It also starts research in the background.

### 9. Work the map

Work the map one ticket at a time.
For each ticket, start a fresh Claude Code session in the repo and type `/wayfinder` followed by the map's issue link.
Claude picks the next open ticket and works it with you.
Grilling tickets need your answers.
Research and many tasks run on their own.

Keep going until the map's last ticket closes and your first wiki is in place.
After that, keep adding sources.

## What is in this repo

- `AGENTS.md` tells the agent what this repo is for and how to work in it. `CLAUDE.md` points Claude Code to it.
- `skills-lock.json` pins the skills to one version of [mattpocock/skills](https://github.com/mattpocock/skills).
- `scripts/check-prep` checks that your machine and your copy are ready.
