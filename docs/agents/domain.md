# Domain docs

This repo is an LLM Wiki, and the wiki's pages are the domain model.
There is no `GLOSSARY.md`, no `docs/adr/` and no `src/`.
The skills' domain-doc conventions map onto the pages.

## Before exploring, read these

- `AGENTS.md`, the wiki's schema: the folder layout, the page types and the workflows that tickets have settled.
- The pages on the subject you are about to work on.

The wiki starts almost empty, and pages appear as tickets decide them.
Where none exist yet, proceed without flagging their absence.

## Where the vocabulary lives

Each subject's terms and mental models live on its pages.
A skill that says "use the glossary's vocabulary" uses the terms already on the relevant pages.
Search the pages before inventing a term.
When `/domain-modeling` resolves a term, write it onto the page it belongs to, not into a `GLOSSARY.md`.

## Where decisions live

There is no separate ADR store.
A durable decision lands on its subject page, with a citation of the ticket that settled it, for example `[Source: <owner>/<repo> issue #<n>, YYYY-MM-DD]`.
A skill that says "record an ADR" or "respect the ADRs in the area" writes or reads the subject page instead.

If your output contradicts a page, say so explicitly rather than overriding the page silently.
