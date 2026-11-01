---
title: A worked example
---

[Home](./) | [How to use it](how-to-use) | **Example** | [FAQ](faq)

# A worked example

A researcher is studying the limits of judicial activism at Brazil's Supreme
Court (STF).

```bash
# 1. One-time setup
/setup-literature-notes --link-style obsidian

# 2. State the scope (a conversation, not a flag)
/literature-notes-scope

# 3. Read a source against that scope
/literature-notes ~/papers/dworkin-1986-taking-rights-seriously.pdf \
  --pages 45-60 --focus "how judicial discretion is theorized"

# 4. Find what you noted so far
/literature-notes-query --note-kind interpretive --tag regra-vs-principio

# 5. Reconcile notes with the scope
/literature-notes-rescope

# 6. Before committing .literature-notes/ changes
/literature-notes-validate
```

## What step 3 produces

A source record and a note. This is one interpretive note, written in the
researcher's language, with the quote kept in the original:

```markdown
---
type: "Reading Note"
source_id: "[[dworkin-1986]]"
page: 52
note_kind: interpretive
tags: [regra-vs-principio]
abnt_citation: "(DWORKIN, 1986, p. 52)"
---

> "Rules are applicable in an all-or-nothing fashion. If the facts a rule
> stipulates are given, then either the rule is valid, in which case the
> answer it supplies must be accepted, or it is not."

Dworkin's rule/principle distinction is what makes room for
[[Glossary#Judicial Activism]] in the first place: a rule alone can't decide
a case where competing principles are in play, and it's exactly that gap
courts fill when weighing principles against each other.
```

The full pack includes a complete example bundle, with two sources, three
notes of all three kinds, a research scope, a glossary and a decision record,
that validates cleanly with the pack's own scripts.
