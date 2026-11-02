---
title: A worked example
---

[Home](./) | [How to use it](how-to-use) | **Example** | [FAQ](faq)

# A worked example, in APA 7

A researcher is reading two papers on language models: *Attention Is All You
Need* (Vaswani et al.) and *BERT* (Devlin et al.), and cites them in APA 7.

```bash
# 1. One-time setup: link style and citation norm
/setup-literature-notes --link-style obsidian --citation-style apa7

# 2. State the scope (a conversation, not a flag)
/literature-notes-research-scope

# 3. Read a source against that scope
/literature-notes-annotate ~/papers/vaswani-2023-attention-is-all-you-need.pdf \
  --pages 2-6 --focus "how attention replaces recurrence and convolution"

# 4. Find what you noted so far
/literature-notes-query --tag attention

# 5. Reconcile notes with the scope
/literature-notes-review

# 6. Before committing .literature-notes/ changes
/literature-notes-validate --check-quotes
```

## What step 3 produces

A source record, with its reference in the chosen norm, and a note with its
citation. This is the source:

```markdown
---
type: Reference
author: Vaswani, Ashish; Shazeer, Noam; Parmar, Niki; ...
kind: article
title: Attention Is All You Need
year: 2023
pdf_path: ~/papers/vaswani-2023-attention-is-all-you-need.pdf
page_offset: 0
references:
  apa7:
    text: Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2023). *Attention is all you need*. arXiv. https://doi.org/10.48550/arXiv.1706.03762
tags: [transformer, attention]
---
```

And this is one note, a summary, anchored to page 5:

```markdown
---
type: Reading Note
source_id: '[[vaswani-2023]]'
page: 5
note_kind: summary
tags: [attention, transformer]
citations:
  apa7:
    text: (Vaswani et al., 2023, p. 5)
---

> "Multi-head attention allows the model to jointly attend to information
> from different representation subspaces at different positions."

## Configuration used

- h = 8 parallel attention heads.
- dk = dv = dmodel / h = 64 per head, so the total cost is similar to
  single-head attention at full dimensionality.
```

The full pack includes two complete example bundles: this one, in APA 7, with
two sources and seven notes, and another in ABNT on judicial activism, with a
review interview and a decision record. Both validate cleanly with the pack's
own scripts.
