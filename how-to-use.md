---
title: How to use it
---

[Home](./) | **How to use it** | [Example](example) | [FAQ](faq)

# How to use it

## Install

The pack ships 8 skills under `skills/`. Copy each folder in `skills/` into
your agent's skills directory (for Claude Code, `~/.claude/skills/` for all
projects or `.claude/skills/` for one project). Then run
`/setup-literature-notes` once in your research project.

Requirements: Python 3. The skills install `pyyaml` and `pypdf` with `pip` the
first time they run. `literature-notes-rescope` also uses the free third-party
`grilling` skill. The HTML viewer loads its fonts and libraries from public
CDNs when you open it in a browser.

## 1. The workflow

Run `/setup-literature-notes` once. After that you loop through scope, read,
query and reconcile, and validate before you commit.

![The workflow](assets/d1.png)

## 2. What lives on disk

Everything the skills create sits in `.literature-notes/` inside your project.

![The .literature-notes layout](assets/d2.png)

## 3. The three note kinds

![Authorial, interpretive and summary notes](assets/d3.png)

## 4. Which skill do I need?

![A skill chooser](assets/d4.png)

## Step by step

1. `/setup-literature-notes`: once per project. Asks whether cross-references
   are Obsidian wikilinks or plain Markdown links.
2. `/literature-notes-scope`: state the research question, what is out of
   scope, and the terms worth pinning down.
3. `/literature-notes <pdf-path>`: read a source or a page range, filtered by
   that scope. This is the step you run most.
4. `/literature-notes-query`: search what you already noted. Run it often.
5. `/literature-notes-rescope`: now and then, batch the notes nobody has
   reconciled with the scope.
6. `/literature-notes-validate`: before every commit.

Not sure where you are? Run `/literature-notes-ask-how`.
