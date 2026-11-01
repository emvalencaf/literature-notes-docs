---
title: FAQ
---

[Home](./) | [How to use it](how-to-use) | [Example](example) | **FAQ**

# FAQ

**Which agents does it work with?**
The skills follow the open `SKILL.md` standard, so they work with compatible
agents such as Claude Code, Codex CLI and Cursor. Test it in yours before
relying on it.

**What do I need installed?**
Python 3. The skills install `pyyaml` and `pypdf` with `pip` on first use.

**Does it send my PDFs anywhere?**
The pack itself does not. The text of the pages you ask it to read goes to
whatever model your agent uses, as with any request you make to that agent.
The HTML viewer loads fonts and libraries from public CDNs when opened.

**Who owns the notes?**
You do. The license covers the pack, not the notes you create with it.

**Why does `/literature-notes-rescope` ask for another skill?**
It runs an interview with the free `grilling` skill, which is not bundled.

**Can I trust the generated notes?**
Treat them as drafts. Every note carries a `generated` mark, and
`/literature-notes-query --verified false` lists the ones you have not checked.
Always compare a quote and its page with the original source.

**What is the license?**
A single-user commercial license. You can use the pack for your own research
on your own devices, and you cannot copy, resell or redistribute it.

**Where do I report a problem?**
Open an issue on this repository.
