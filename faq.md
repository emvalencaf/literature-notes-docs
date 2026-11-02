---
title: FAQ
---

[Home](./) | [How to use it](how-to-use) | [Example](example) | **FAQ**

# FAQ

**Which citation norms does it support?**
Any formal academic norm. Setup asks which one you follow, looks up its rules,
shows you a draft and freezes it after you approve. APA 7 is suggested first,
and ABNT, MLA and Chicago author-date work the same way. Official manuals are
often paid, so the draft says which sources it used, and you should compare it
with your own copy of the norm.

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

**Why does `/literature-notes-review` ask for another skill?**
It runs an interview with the free `grilling` skill, which is not bundled.

**Can I trust the generated notes?**
Treat them as drafts. Every note carries a `generated` mark, and
`/literature-notes-query --verified false` lists the ones you have not checked.
`/literature-notes-validate --check-quotes` also confirms that each quote
appears on the PDF page you cited, which catches wrong pages and altered
quotes. It does not replace reading the original.

**My book's printed pages differ from the PDF pages. Does it handle that?**
Yes. Setup asks whether you cite PDF pages or printed pages, and each source
can carry a page offset.

**I used an older version with ABNT fields. Do I lose anything?**
No. Re-run `/setup-literature-notes` and it lists the old `abnt_*` fields and
migrates them only after you confirm. Three skills were renamed in this
version: `literature-notes` is now `literature-notes-annotate`,
`literature-notes-scope` is `literature-notes-research-scope`, and
`literature-notes-rescope` is `literature-notes-review`.

**What is the license?**
A single-user commercial license. You can use the pack for your own research
on your own devices, and you cannot copy, resell or redistribute it.

**Where do I report a problem?**
Open an issue on this repository.
