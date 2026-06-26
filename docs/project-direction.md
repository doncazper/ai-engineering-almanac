---
title: "Project Direction"
slug: "project-direction"
status: "seed"
section: "Project Operating System"
tags:
  - project-direction
  - roadmap
  - product-strategy
  - knowledge-system
---

# Project Direction

## One-sentence direction

The AI Engineering Almanac is a public, source-aware, Markdown-first knowledge base and future interactive wiki for AI engineering terms, workflow phrases, prompt macros, production patterns, implementation templates, and conversation-capture systems.

## The core idea

Most engineering glossaries define nouns. This project should also define the practical phrases, patterns, and reusable prompts that make AI-assisted engineering faster.

The Almanac should answer questions like:

- What does this term mean?
- How is it used in production?
- What is it commonly confused with?
- What prompt phrase makes this workflow faster?
- What template turns this concept into implementation?
- Which sources are strong enough to define it canonically?
- How do we preserve useful AI conversations without losing information?

## What this is

- A public AI/software engineering almanac.
- A glossary of canonical terms.
- A prompt macro library.
- A workflow phrase dictionary.
- A frontend-backend contract engineering playbook.
- A conversation-to-wiki capture system.
- A source-aware research database.
- A future AI-powered prompt finder and workflow retrieval engine.

## What this is not

- Not a random prompt dump.
- Not a private notebook.
- Not a newsletter archive.
- Not a list of buzzwords without source discipline.
- Not just definitions without examples.
- Not a finished encyclopedia on day one.

## Editorial doctrine

> Use newsletters and explainers for vocabulary discovery. Use official docs, research papers, and standards for canonical definitions.

Discovery sources help us find emerging language. Canonical sources help us define terms accurately.

## First major pillars

1. Core AI Workflow Taxonomy
2. Prompt Engineering and Prompt Macros
3. Agent Engineering Terms
4. Coding Agent / AI Development Workflow Terms
5. Frontend-Backend Contract Engineering
6. Conversation Capture & Knowledge Distillation
7. RAG, Retrieval, and Knowledge Systems
8. Evaluation, Guardrails, and Reliability
9. Engineering Reliability, Systems, and Backend Terms
10. Wiki / Public Database Schema Vocabulary
11. High-Leverage Prompt Phrases
12. AI Almanac Assistant / Prompt Finder

## The differentiator

A normal glossary says:

```txt
RAG means Retrieval-Augmented Generation.
```

This Almanac should also say:

```txt
Use this prompt when you need to ground an LLM response in private docs.
Use this checklist to avoid retrieval bugs.
Use this template to design the source corpus.
Use this eval to detect hallucinated citations.
```

The project is strongest when every concept connects to a production pattern, prompt macro, template, or quality checklist.

## North-star user experience

A user should eventually be able to ask:

```txt
I need a prompt to turn a rough app idea into frontend/backend specs.
```

The Almanac should return:

1. Closest prompt macros.
2. Related wiki entries.
3. Why each result matched.
4. A customized copy-paste prompt.
5. Templates and checklists to execute the workflow.

## Product architecture

```txt
GitHub repo        = public source of truth
Markdown docs      = human-readable knowledge base
YAML frontmatter   = machine-readable metadata
GitHub Issues      = intake queue for terms, prompts, corrections, and sources
Pull Requests      = review and status promotion workflow
GitHub Pages       = public docs site
Future AI layer    = Prompt Finder over prompt macros, terms, templates, and examples
Optional Obsidian  = private workshop for drafting and research
```

## Content object types

- Canonical Term
- Prompt Macro
- Workflow Phrase
- Implementation Template
- Pattern Catalog Entry
- Source Note
- Research Batch
- Session Capture
- Durable Knowledge Object
- Visual / Diagram
- Data Index Entry

## Status pipeline

```txt
seed -> draft -> reviewed -> verified -> canonical
```

### seed

A captured idea, phrase, source, term, template, or example. Useful but not trusted yet.

### draft

A structured page exists and uses the relevant template.

### reviewed

The page has been checked for clarity, duplication, category fit, examples, and related terms.

### verified

The page has been checked against strong sources where possible.

### canonical

The entry is stable enough to be treated as an official Almanac definition or pattern.

## First public milestone

Milestone 0.1 is the public skeleton.

Done means:

- README explains the project.
- Project Direction exists.
- Roadmap exists.
- Source Strategy exists.
- Status Pipeline exists.
- First 15 canonical-entry skeletons exist.
- Prompt Finder plan exists.
- Issue templates exist.
- Pull request checklist exists.
- GitHub Pages can publish the site.

## First canonical-entry set

The first entries should define the project’s unique worldview:

1. Prompt Macro
2. Workflow Phrase
3. Backend-Ready Frontend Spec
4. Field-to-Backend Mapping
5. Frontend-Backend Contract Engineering
6. Frontend-Backend Handoff Packet
7. Session-to-Wiki Compiler
8. Durable Knowledge Object
9. No-Loss Distillation
10. Extract, Don’t Summarize
11. Mock Data Must Match Final API
12. Define Done
13. Source Tiering
14. Canonical Entry
15. Docs-as-Database

## Long-term product vision

The Almanac should become a workflow retrieval engine:

```txt
Describe a problem -> find the closest prompt/template/pattern -> adapt it -> execute the workflow -> preserve the result as structured knowledge.
```

That makes it more than a wiki. It becomes a public operating manual for AI-assisted engineering.
