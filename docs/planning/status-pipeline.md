---
title: "Status Pipeline"
slug: "status-pipeline"
status: "seed"
section: "Project Operating System"
tags:
  - governance
  - workflow
  - source-quality
  - publishing
---

# Status Pipeline

The Almanac uses a status pipeline so captured ideas can become trusted public entries without pretending that every note is canonical on day one.

```txt
seed -> draft -> reviewed -> verified -> canonical
```

## seed

A captured idea, phrase, source, term, template, or example.

### Requirements

- Has a title.
- Has a rough definition or reason for inclusion.
- Can come from conversation, newsletter, blog, documentation, paper, repo, or observation.
- Is not yet trusted as an official definition.

### Example

```yaml
status: "seed"
source_tier: "discovery"
```

## draft

A structured page exists.

### Requirements

- Uses the relevant entry template.
- Has a definition.
- Has a core concept.
- Has at least one example.
- Has aliases and tags.
- Lists related terms.

## reviewed

The page has been checked for clarity and fit.

### Requirements

- Terminology is clear.
- Duplicate or overlapping entries are noted.
- Related terms are cross-linked.
- Examples are useful.
- Common misconceptions are included where relevant.

## verified

The page has been checked against strong sources where possible.

### Requirements

- Official docs, standards, research papers, or vendor docs are used where possible.
- Newsletters and blogs are marked as discovery sources, not canonical sources.
- Misconceptions and edge cases are addressed.
- Source notes are included.

## canonical

The page is stable enough to be treated as an official Almanac entry.

### Requirements

- Accurate definition.
- Clear examples.
- Production notes.
- Related terms.
- Common mistakes.
- Source notes.
- No unresolved major open questions.

## Required frontmatter

Every public entry should include:

```yaml
---
title: "Example Term"
slug: "example-term"
status: "seed"
section: "Example Section"
aliases: []
tags: []
source_tier: "unknown"
created: "YYYY-MM-DD"
updated: "YYYY-MM-DD"
---
```

## Source tiers

```txt
canonical       = official docs, standards, papers, specifications
vendor          = vendor/product docs or official engineering blogs
discovery       = newsletters, explainers, community posts, trend sources
community       = forums, discussions, social posts
internal-session = extracted from an AI conversation or project discussion
unknown         = needs source review
```

## Promotion rule

Do not promote an entry to `canonical` in a drive-by edit.

Use a pull request for status promotion.

The pull request should explain:

- What changed.
- What sources were used.
- Why the entry is ready for promotion.
- What open questions remain, if any.

## Label mirror

Issue labels should mirror the page status when possible:

```txt
status: seed
status: draft
status: reviewed
status: verified
status: canonical
```

## Mental model

The status pipeline is quality control for a public knowledge base.

It lets the Almanac move fast without confusing discovery notes with trusted definitions.
