---
id: session-to-wiki-compiler
title: Session-to-Wiki Compiler
category: conversation-capture
status: draft
aliases:
  - conversation-to-wiki compiler
  - session capture workflow
  - conversation distillation workflow
tags:
  - knowledge-capture
  - prompt-macros
  - documentation
related:
  - durable-knowledge-object
  - no-loss-distillation
  - extract-dont-summarize
---

# Session-to-Wiki Compiler

## Definition

A workflow that converts an AI conversation into durable knowledge objects: canonical terms, prompt macros, decisions, templates, artifacts, source notes, open questions, and follow-up wiki entries.

## Core Concept

A conversation is not just chat history. It is raw material for a knowledge base.

## Prompt Macro

```md
Extract this conversation into durable knowledge objects:
- canonical terms
- prompt macros
- decisions
- templates
- artifacts
- open questions
- source notes
- follow-up wiki entries

Preserve details first, then create a concise session digest.
```

## Production Notes

- Keep raw transcripts private by default.
- Publish redacted session digests.
- Mark extracted ideas as `seed` until reviewed.
- Convert high-value repeated phrases into prompt macros.
- Convert terms into canonical entries only after source verification.
