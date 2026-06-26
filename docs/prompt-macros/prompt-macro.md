---
title: "Prompt Macro"
slug: "prompt-macro"
status: "seed"
section: "Prompt Macros"
alises:
  - "Prompt Pattern"
  - "AI Prompting Template"
  - "Prompt Engineering"
tag:
  - prompt-engineering
  - ai-workflow
  - templates
  - llm
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Prompt Macro

## Definition

A reusable, high-leverage phrase or instruction pattern that reliably produces a specific AI behavior when inserted into a prompt.

## Core Concept

Prompt macros are not just "good prompts" — they are atomic units of intent that can be combined, reused across sessions, and versioned. Think of them as functions in the LLM interaction domain: you invoke `<<extract structure>>` or `<<define done>>` without rewriting the underlying logic.

## Why It Matters

Without macros, users reinvent prompt phrasing every session. With macros, teams can share proven patterns like building blocks.

## Real-World Example

**Macro:** `<<no-loss distillation>>`

**Expansion when used in a prompt:**
```
Extract all concrete details, code snippets, definitions, examples, and specific facts from this conversation. Do not summarize or paraphrase. Preserve the exact information density by creating discrete, durable knowledge objects. Capture what was said, not a compressed version.
```

## Common Mistakes

- Treating macros as one-off prompts instead of reusable templates
- Not versioning macro changes (breaking downstream uses)
- Overloading a single macro with multiple intents

## Related Terms

- Workflow Phrase
- System Prompt Pattern
- Few-Shot Template
- Chain-of-Thought Prompting

## Mental Model

A prompt macro is a **macro in the classical computing sense**: text that expands into more complex logic at runtime.

## Production Notes

Store macros in a shared repository (Markdown or YAML). Version them alongside code. Document expansion rules.