# AI Engineering Almanac

A public, source-aware, Markdown-first knowledge base for AI engineering terms, workflow phrases, prompt macros, implementation templates, and production patterns.

This project is not just a glossary. It is a practical engineering almanac designed to answer:

- What does this term mean?
- How is it used in production?
- What is it commonly confused with?
- What prompt phrase makes this workflow faster?
- What template turns the concept into implementation?
- Which sources should define it canonically?
- How do we preserve useful AI conversations without losing information?

## One-sentence direction

The AI Engineering Almanac is a public operating manual for AI-assisted engineering: part glossary, part prompt library, part systems playbook, part interactive workflow engine.

## North-star experience

Eventually, a user should be able to ask:

```txt
I need a prompt to do XYZ.
```

The Almanac should find the closest prompt macros, templates, and wiki entries, explain why they match, and generate a customized copy-paste prompt.

## Project model

```txt
GitHub repo        = public source of truth
Markdown docs      = human-readable knowledge base
YAML frontmatter   = machine-readable metadata
GitHub Issues      = intake queue
Pull Requests      = review and verification workflow
GitHub Pages       = public docs site
Future AI layer    = Prompt Finder over prompt macros, terms, templates, and examples
Optional Obsidian  = private workshop for drafting and research
```

## Core doctrine

> Use newsletters and explainers for vocabulary discovery. Use official docs, research papers, and standards for canonical definitions.

Discovery sources help us find emerging vocabulary. Canonical sources help us define terms accurately.

## Content types

- **Canonical Terms** — source-backed definitions and production notes.
- **Prompt Macros** — reusable phrases that trigger high-leverage AI workflows.
- **Workflow Phrases** — short commands that make AI-assisted work faster.
- **Implementation Templates** — copy/paste specs, handoff packets, checklists, schemas, and capture forms.
- **Research Batches** — raw candidate terms and source notes before canonicalization.
- **Session Captures** — durable knowledge objects extracted from AI conversations.
- **Visuals / Diagrams** — graphics that explain workflows, mappings, or architecture.
- **Machine-Readable Indexes** — YAML files used later for search, graphing, and Prompt Finder.

## Initial pillars

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
11. AI Almanac Assistant / Prompt Finder

## Start here

1. [Project Direction](docs/project-direction.md)
2. [Source Strategy](docs/source-strategy.md)
3. [Status Pipeline](docs/planning/status-pipeline.md)
4. [Milestone 0.1 — Public Skeleton](docs/planning/milestone-0-1-public-skeleton.md)
5. [Prompt Finder](docs/ai-almanac-assistant/prompt-finder.md)
6. [Research Batch 01](docs/research/research-batch-01.md)
7. [Backend-Ready Frontend Spec](docs/frontend-backend-contracts/backend-ready-frontend-spec.md)
8. [Session-to-Wiki Compiler](docs/conversation-capture/session-to-wiki-compiler.md)

## Entry status pipeline

```txt
seed -> draft -> reviewed -> verified -> canonical
```

Supporting labels:

```txt
source-reported
needs-source
needs-example
needs-diagram
needs-production-notes
```

## First milestone

Milestone 0.1 is the public skeleton.

Done means:

- [ ] README explains the project.
- [ ] Project Direction exists.
- [ ] Roadmap exists.
- [ ] Source Strategy exists.
- [ ] Status Pipeline exists.
- [ ] First 15 canonical-entry skeletons exist.
- [ ] Prompt Finder plan exists.
- [ ] Issue templates exist.
- [ ] Pull request checklist exists.
- [ ] GitHub Pages can publish the site.

## Repository philosophy

Start as a Markdown database. Publish as a docs site. Later, generate an interactive wiki and AI-assisted Prompt Finder from the same frontmatter and file tree.
