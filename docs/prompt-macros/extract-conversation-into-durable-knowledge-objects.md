---
id: extract-conversation-into-durable-knowledge-objects
title: Extract Conversation Into Durable Knowledge Objects
type: prompt-macro
category: prompt-macros
status: draft
tags:
  - conversation-capture
  - knowledge-distillation
  - documentation
related_terms:
  - session-to-wiki-compiler
  - durable-knowledge-object
  - no-loss-distillation
---

# Extract Conversation Into Durable Knowledge Objects

## Use When

Use this when a conversation produced ideas, terms, decisions, prompts, templates, or artifacts that should not be lost.

## Prompt

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

## Why It Works

It asks for structured extraction instead of a lossy summary.
