---
title: literature-notes
---

# literature-notes

**English** | [Português (Brasil)](pt-br/)

Eight agent skills that turn academic sources (articles, dissertations,
theses and books) into a structured, queryable wiki of reading notes. Every
note is anchored to a page, tagged against a controlled glossary, and read
through your research question.

Available on Agensi. Single-user license.

![The workflow](assets/d1.png)

## What it does

- Takes notes from a PDF, one note per concept, in three kinds:
  **authorial** (your own idea), **interpretive** (your reading of the
  author) and **summary** (a neutral account), each with ABNT citation
  metadata.
- Keeps a research scope (`RESEARCH.md`) and a controlled glossary
  (`Glossary.md`) that every note answers to.
- Queries the notes by tag, source, note kind, page, influence links,
  verification status or free text.
- Validates the bundle for broken references: unknown tags, dangling links,
  undefined glossary terms.
- Builds a read-only HTML "second brain" with full-text search, backlinks and
  a link graph.
- Writes in your language. A quoted passage stays in the source's language.

## The eight skills

| Skill | Use it to |
| --- | --- |
| `setup-literature-notes` | One-time setup: scaffold `.literature-notes/` and pick a link style. |
| `literature-notes-scope` | State the research question and the glossary. |
| `literature-notes` | Read a PDF and write the notes. |
| `literature-notes-query` | Search what you already noted. |
| `literature-notes-rescope` | Reconcile pending notes with the scope. |
| `literature-notes-validate` | Check for broken references before a commit. |
| `literature-notes-visualize` | Generate the HTML site. |
| `literature-notes-ask-how` | Ask which skill fits what you are doing. |

## Keep reading

- [How to use it, in diagrams](how-to-use)
- [A worked example](example)
- [FAQ](faq)

## Why a query stays cheap

A query or a validation only brings what matches into the chat, not the whole
bundle. The notes can grow to hundreds of files without each query costing
more.
