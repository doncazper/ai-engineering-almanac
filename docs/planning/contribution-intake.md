---
title: "Contribution Intake"
slug: "contribution-intake"
status: "seed"
section: "Project Operating System"
tags:
  - github-issues
  - contributions
  - intake
  - workflow
---

# Contribution Intake

The Almanac should use GitHub Issues as the intake layer for new terms, prompt macros, templates, source notes, corrections, and feature ideas.

## Intake principle

Every reusable idea starts as a captured object before it becomes a canonical page.

```txt
idea -> issue -> draft page -> review -> source verification -> canonical entry
```

## What belongs in issues

- New terms
- Prompt macros
- Workflow phrases
- Source suggestions
- Corrections
- Confusing term pairs
- Missing examples
- Diagrams
- Templates
- Feature ideas
- Research backlog items

## Issue title conventions

```txt
Add term: Field-to-Backend Mapping
Add prompt macro: Extract, Don’t Summarize
Add template: Frontend-Backend Handoff Packet
Clarify: JSON Mode vs Structured Outputs
Add source note: OpenAI Prompt Engineering docs
Build feature: Prompt Finder MVP
Research: Agent Engineering vocabulary batch
```

## Recommended labels

### Type labels

```txt
type: term
type: prompt-macro
type: workflow-phrase
type: template
type: source-note
type: correction
type: feature
type: research
type: diagram
```

### Status labels

```txt
status: seed
status: draft
status: reviewed
status: verified
status: canonical
```

### Section labels

```txt
section: ai-workflow
section: prompt-engineering
section: agents
section: coding-agents
section: frontend-backend
section: conversation-capture
section: rag
section: evals
section: reliability
section: wiki-database
section: prompt-finder
```

### Priority labels

```txt
priority: p0
priority: p1
priority: p2
```

## Intake workflow

### 1. Capture

Create an issue with the rough idea.

### 2. Classify

Add type, status, section, and priority labels.

### 3. Draft

Create or update a Markdown page using the appropriate template.

### 4. Link

Link the issue to the page path.

### 5. Review

Check clarity, examples, related terms, and category fit.

### 6. Verify

Check source quality. Mark newsletters/blogs as discovery sources unless they are the best available source.

### 7. Promote

Use a pull request to promote important pages to `verified` or `canonical`.

## Minimal issue body

```md
## Summary

What should be added or changed?

## Why it matters

Why does this belong in the Almanac?

## Suggested category

Where should it live?

## Draft definition or prompt

Add rough content here.

## Sources

List official docs, papers, standards, vendor docs, newsletters, blogs, or community references.

## Related terms

List related entries or confusing overlaps.
```

## What not to do

- Do not add hundreds of unreviewed entries directly to `canonical`.
- Do not use newsletters as final authority when official docs exist.
- Do not merge source claims without source notes.
- Do not publish private conversation content without redaction.
- Do not treat prompt snippets as useful unless they have context, use cases, and expected outputs.

## Mental model

GitHub Issues are the inbox. Markdown pages are the library. Pull Requests are the quality gate.
