---
title: "Obsidian-to-GitHub Publishing Pipeline"
slug: "obsidian-to-github-publishing-pipeline"
status: "seed"
section: "Knowledge System"
aliases:
  - "Obsidian to GitHub Workflow"
  - "Private Workshop to Public Library"
tags:
  - obsidian
  - github
  - publishing
  - knowledge-management
  - workflow
---

# Obsidian-to-GitHub Publishing Pipeline

## Definition

A knowledge workflow where Obsidian is used for private capture, linking, and drafting, while GitHub is used as the public, version-controlled source of truth.

## Core concept

Separate messy thinking from public canonical knowledge.

```txt
Obsidian = workshop
GitHub   = library
```

## Why it matters

The Almanac will generate messy material:

- raw conversation captures;
- half-formed term ideas;
- newsletter notes;
- source clippings;
- prompt fragments;
- diagrams;
- private project ideas;
- unverified definitions.

Not all of that should go public immediately.

## Recommended setup

```txt
AI Almanac Lab/                 # private Obsidian vault
  00 Inbox/
  01 Durable Knowledge Objects/
  02 Research Batches/
  03 Maps of Content/
  04 Draft Entries/
  05 Ready for GitHub/

ai-engineering-almanac/         # public GitHub repo
  docs/
  data/
  templates/
  README.md
  mkdocs.yml
```

## Promotion workflow

```txt
Capture in Obsidian
-> extract durable knowledge objects
-> draft an entry
-> source-check
-> move into GitHub docs
-> open issue or PR
-> publish through GitHub Pages
```

## What belongs in Obsidian

- Raw notes.
- Messy thoughts.
- Private source clips.
- Conversation extractions before redaction.
- Drafts that are not ready for public review.
- Maps of content.
- Personal research trails.

## What belongs in GitHub

- Public canonical entries.
- Prompt macros.
- Templates.
- Source strategy.
- Roadmap.
- Research batches safe to publish.
- GitHub issue templates.
- Machine-readable YAML indexes.

## Public Markdown rule

Use standard Markdown links in public docs.

Prefer:

```md
[Prompt Macro](../prompt-macros/prompt-macro.md)
```

Avoid Obsidian-only links in public docs:

```md
[[Prompt Macro]]
```

## Privacy rule

Before moving a session capture from Obsidian to GitHub, run a redaction pass.

Remove:

- private credentials;
- personal contact details;
- private business plans not meant for publication;
- proprietary code;
- sensitive conversation details;
- anything that should not be indexed publicly.

## Mental model

Obsidian is where knowledge is refined. GitHub is where knowledge is published and governed.
