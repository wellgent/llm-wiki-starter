# LLM Wiki

This repo is becoming its owner's personal LLM Wiki, after Karpathy's pattern: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

## How the wiki takes shape

A wayfinder map decides the wiki's structure.
Its research tickets find out how to set up an LLM Wiki, its grilling tickets settle with the owner what to include, and its tasks gather and ingest the sources.
The map and its tickets are issues on this repo's GitHub Issues.

Folder layout, including any `raw/` or `wiki/` folders, an index or a log, comes from resolved tickets.
Add structure once a ticket has decided it.
As tickets settle the structure and the ingest, query and upkeep workflows, write them into this file, which is the wiki's schema.

## Sources and secrets

The owner's sources live in folders outside this repo, and the owner points you at them.
Bring material into the repo only as a resolved ticket decides.
Notes often hold passwords, API keys, tokens and other credentials.
Leave every secret out of wiki pages, commits and issues, and tell the owner where you found it.

## Repo

The repo stays private, because it holds personal notes.
Commit and push each finished piece of work.
`scripts/check-prep` checks the tools, sign-ins, GitHub remote, issues and installed skills.
