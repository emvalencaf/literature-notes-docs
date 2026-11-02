---
title: FAQ
---

[Home](./) | [How to use it](how-to-use) | [Example](example) | **FAQ**

# FAQ

- [Before you buy](#before-you-buy)
- [Getting started](#getting-started)
- [Citations and pages](#citations-and-pages)
- [Trust and privacy](#trust-and-privacy)
- [Upgrading from an older version](#upgrading-from-an-older-version)

## Before you buy

**What is it, in one line?**
Eight agent skills that turn academic PDFs into a wiki of reading notes, each
note anchored to a page, cited in your norm and read against your research
question.

**Who is it for?**
Anyone who reads many papers or books for one research project: a thesis,
a dissertation, a literature review. It is built around a research scope, so
it fits a project with a question better than casual reading.

**Which AI agents does it work with?**
The skills follow the open `SKILL.md` standard, so they work with compatible
agents such as Claude Code, Codex CLI and Cursor. Behavior depends on the
model your agent runs, so try one PDF in your own setup before you rely on it.

**What is included?**
The 8 skills, two complete example bundles (APA 7 on two machine learning
papers, and ABNT on judicial activism), workflow diagrams, a changelog and the
license.

**What does the license allow?**
A single-user commercial license. You can use the pack for your own research on
your own devices. You cannot copy, resell or redistribute it, and a team needs
one license per user. Purchases through Agensi are also covered by its
money-back guarantee, described in its terms.

**Who owns my notes?**
You do. The license covers the pack, not the notes, research files and
glossaries you create with it.

## Getting started

**What do I need installed?**
Python 3. The skills install `pyyaml` and `pypdf` with `pip` the first time
they run. The notes are plain Markdown, so they work in Obsidian, GitHub or any
editor.

**How do I install it?**
Copy each folder in `skills/` into your agent's skills directory, then run
`/setup-literature-notes` once in your project. See [How to use it](how-to-use).

**Why does `/literature-notes-review` ask for another skill?**
It runs its interview with the free `grilling` skill, which is not bundled.
Without it, the review step does not run. The other seven skills do not need it.

**Can I change my research question after I have started reading?**
Yes. `/literature-notes-review` interviews you, one question at a time, about
notes not yet reconciled with your scope, and updates `RESEARCH.md` and
`Glossary.md` where your answers push them.

**Does it work in my language?**
Notes are written in the language you use with the agent. A quoted passage
stays in the source's own language.

## Citations and pages

**Which citation norms does it support?**
Any formal academic norm: APA, ABNT, MLA, Chicago or another. Setup asks which
one you follow, looks up its rules, shows you a draft and freezes it only
after you approve. Every note and source then carries its citation and
reference in that norm. Official manuals are often paid, so the draft says
which sources it used. Compare it with your own copy of the norm.

**Can I use more than one norm, or switch later?**
Yes. Re-run `/setup-literature-notes` to add or switch a norm. Each norm lives
in its own file, and existing notes keep the citations they already have.

**My book's printed pages differ from the PDF's. Does it handle that?**
Yes. Setup asks whether you cite PDF pages or printed pages, and each source
can carry a page offset.

## Trust and privacy

**Can I trust the generated notes?**
Treat them as drafts that you verify. Each note is marked as generated, and
`/literature-notes-query --verified false` lists the ones nobody has
confirmed. `/literature-notes-validate --check-quotes` also checks that every
quote appears on the PDF page you cited, which catches wrong pages and altered
quotes. It does not replace reading the original source.

**Does it send my PDFs anywhere?**
The pack itself does not upload anything. The text of the pages you ask it to
read goes to whatever model your agent uses, as with any request you make to
that agent. Your notes stay as files in your own project. The optional HTML
viewer loads fonts and libraries from public CDNs when you open it.

## Upgrading from an older version

**I used a version with ABNT-only fields. Do I lose anything?**
No. Re-run `/setup-literature-notes`. It lists the old `abnt_*` fields and
rewrites them only after you confirm.

**Some skills have new names.**
`literature-notes` is now `literature-notes-annotate`, `literature-notes-scope`
is `literature-notes-research-scope`, and `literature-notes-rescope` is
`literature-notes-review`. Re-run `/setup-literature-notes` to refresh the
block it keeps in `CLAUDE.md` and `AGENTS.md`.

**Where do I report a problem?**
Open an issue on this repository.
