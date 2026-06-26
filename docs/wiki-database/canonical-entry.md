---
title: "Canonical Entry"
slug: "canonical-entry"
status: "seed"
section: "Wiki Database"
alises:
  - "Authoritative Definition"
  - "Reference Documentation"
  - "Gold Standard Entry"
tag:
  - documentation
  - knowledge-base
  - content-strategy
  - governance
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Canonical Entry

## Definition

A verified, stable documentation page that serves as the authoritative definition for a term, pattern, or concept within an organization's knowledge base.

## Core Concept

Canonical entries are not drafts or notes — they have passed through review cycles, been fact-checked against Tier 1/2 sources, and approved by subject matter experts. They are **publication-ready** and linkable from external documentation.

## Why It Matters

Without canonical entries, organizations have "drift" where different teams use the same term to mean different things. Canonicalization creates a single source of truth.

## Real-World Example

A canonical entry for "Structured Outputs" includes:
- Precise definition aligned with OpenAI's official documentation
- Code examples (Python, curl) showing API usage
- Comparison table: Structured Outputs vs JSON Mode vs Function Calling
- Migration guide: how to upgrade from legacy patterns
- Source notes citing the official OpenAI docs and relevant RFCs or papers
- Related terms with internal links ("See also: Prompt Macro")

## Common Mistakes

- Marking entries as canonical before source verification
- Allowing multiple "canonical" definitions for the same term in different folders
- Not updating canonical entries when official specs change
- Missing examples or making them too abstract to use

## Related Terms

- Source of Truth
- Authoritative Documentation
- Single Source of Truth (SSOT)
- Golden Record
- Reference Implementation

## Mental Model

A canonical entry is a **published dictionary definition**, not a sticky note on someone's monitor.

## Production Notes

Use YAML frontmatter `status: "canonical"` to mark entries. Protect the folder from direct edits (require PR review). Link to canonical entries from all lower-tier notes.