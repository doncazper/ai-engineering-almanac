---
title: "Workflow Phrase"
slug: "workflow-phrase"
status: "seed"
section: "Prompt Macros"
alises:
  - "Semantic Trigger"
  - "Intent Phrase"
  - "AI Command"
tag:
  - prompt-engineering
  - ai-workflow
  - conversational-ai
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Workflow Phrase

## Definition

A natural-language phrase that encodes an entire workflow pattern, used to trigger specific AI behaviors without spelling out every step.

## Core Concept

Workflow phrases are **semantic triggers**. Instead of writing "please analyze this code for bugs, suggest improvements, check for security vulnerabilities, and then generate tests," you say `<<code review mode>>` if that phrase has been defined as a macro.

They bridge the gap between natural language intent and structured AI operations.

## Why It Matters

Long prompts are error-prone and hard to maintain. Workflow phrases let you build a vocabulary of trusted patterns.

## Real-World Example

| Phrase | Expands To |
|--------|------------|
| `<<extract structure>>` | "Identify all entities, relationships, data models, and architectural components in this text. Output as a structured schema or diagram." |
| `<<define done>>` | "Specify the acceptance criteria, exit conditions, and completion gates for this task. What must be true before we consider this finished?" |
| `<<backend ready spec>>` | "Create a frontend specification that includes complete backend contracts: data models, API endpoints, validation rules, error states, and database schemas." |

## Common Mistakes

- Using phrases too loosely (losing the association with specific workflows)
- Not documenting what each phrase actually triggers
- Creating too many overlapping phrases

## Related Terms

- Prompt Macro
- Intent Classification
- Workflow Orchestration
- Semantic Trigger

## Mental Model

A workflow phrase is a **shortcut key for your brain**, mapped to LLM behavior instead of IDE actions.

## Production Notes

Curate a small set (5–10) of high-value phrases. Test them across multiple sessions to ensure consistency before adopting as standard.