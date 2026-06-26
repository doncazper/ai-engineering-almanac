---
title: "Source Tiering"
slug: "source-tiering"
status: "seed"
section: "Wiki Database"
alises:
  - "Source Authority Levels"
  - "Reference Hierarchy"
  - "Evidence Classification"
tag:
  - research
  - epistemology
  - knowledge-management
  - verification
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Source Tiering

## Definition

A classification system for knowledge sources based on authority, reliability, and verifiability — distinguishing between canonical references (official docs, standards) and discovery sources (blogs, newsletters, conversations).

## Core Concept

Not all information is equal. A term discovered in a newsletter is not "verified" until checked against an official spec or paper. Source tiering tracks the **provenance chain** from discovery to verification.

## Why It Matters

Without tiering, teams treat Reddit comments and RFC specifications as equally authoritative. With it, you know what needs fact-checking before becoming canonical documentation.

## Real-World Example

| Tier | Source Type | Examples | Trust Level |
|------|-------------|----------|-------------|
| **Tier 1 (Canonical)** | Official specs, standards bodies, vendor docs | OpenAPI Spec, RFC 6749 (OAuth), MDN Web Docs, NIST guidelines | Verified truth. Citable as reference. |
| **Tier 2 (Strong)** | Peer-reviewed papers, technical books, official blog posts from core teams | ACM Digital Library, O'Reilly books, engineering blogs by platform creators (e.g., Stripe Engineering) | High trust but may be opinionated or time-bound. |
| **Tier 3 (Discovery)** | Newsletters, Twitter/X threads, Stack Overflow, conference talks, internal wikis | The Neuron, Lenny's Newsletter, personal blogs, HackerNews comments | Vocabulary and idea sources only. Must verify with Tier 1/2 before citing. |
| **Tier 4 (Ephemeral)** | Chat logs, meeting recordings, AI hallucinations | Slack threads, Zoom transcripts, unsourced AI responses | Raw material only. Not citable. |

## Common Mistakes

- Citing a newsletter as if it were an official spec
- Treating "everyone says" (Tier 3 consensus) as verification
- Not recording where Tier 3 discoveries originated (can't verify later)
- Using AI-generated content as a source without checking its references

## Related Terms

- Evidence-Based Documentation
- Citation Hierarchy
- Authority Ranking
- Epistemic Status Tagging
- Provenance Tracking

## Mental Model

Source tiering is **geological strata**: recent sediment (Tier 4) sits on top of bedrock (Tier 1). You mine ideas from the top but build foundations on the bottom.

## Production Notes

Tag every wiki entry with `source_tier: mixed`, `verified`, or `canonical`. Link to Tier 1 sources in the "Source Notes" section. Never cite a Tier 3 source as proof — use it only to justify that research was done.