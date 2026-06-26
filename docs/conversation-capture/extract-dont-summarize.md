---
title: "Extract, Don't Summarize"
slug: "extract-dont-summarize"
status: "seed"
section: "Conversation Capture"
alises:
  - "Extraction over Compression"
  - "Detail Preservation"
  - "Atomic Extraction"
tag:
  - knowledge-management
  - ai-workflow
  - information-architecture
  - documentation
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Extract, Don't Summarize

## Definition

A principle for processing AI conversations: prefer extracting discrete facts, definitions, code snippets, and examples over producing compressed summaries that lose precision.

## Core Concept

Summaries are useful for quick scanning but terrible for reference. Extraction keeps the **information density** of the original while organizing it into searchable chunks.

## Why It Matters

When you summarize a technical conversation about API design, you might say "we discussed authentication." When you extract, you capture: OAuth 2.0 flow steps, token expiration times (1h access, 7d refresh), endpoint paths (`/oauth/token`), and error codes (401 vs 403).

## Real-World Example

**Summary approach:**
> "Discussed prompt injection mitigation strategies including delimiters and role assignment."

**Extraction approach:**
- **Delimiter Technique**: Wrap user input in XML tags `<user_input>...</user_input>` to separate it from system instructions.
- **Role Assignment**: Explicitly tell the model: "You are a code translator. Only output JSON." (limits interpretation space)
- **Validation Step**: Schema-validate all LLM outputs before executing them as code or SQL.
- **Example Prompt**: Full verbatim example showing delimiters in action.

## Common Mistakes

- Defaulting to "summarize this" prompts when archiving conversations
- Losing specific parameter values, URLs, and error codes during summarization
- Not tagging extracted items by type (definition vs. code vs. decision)

## Related Terms

- No-Loss Distillation
- Information Extraction
- Atomic Note-Taking
- RAG Chunking Strategy

## Mental Model

Extraction is **mining** (pull out the ore). Summarization is **smelting** (melt it down to a simpler form, losing impurities and trace elements).

## Production Notes

When using AI to process transcripts, ask for "extraction into categories" not "summary." Then manually review extracted items for accuracy.