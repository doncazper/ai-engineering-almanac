# Project Direction

The AI Engineering Almanac is a public, source-aware, Markdown-first knowledge base and future interactive wiki for AI engineering terms, workflow phrases, prompt macros, production patterns, implementation templates, and conversation-capture systems.

The full direction document lives here:

- [Project Direction](docs/project-direction.md)

## Core doctrine

> Use newsletters and explainers for vocabulary discovery. Use official docs, research papers, and standards for canonical definitions.

## Current product model

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

## North-star experience

A user should eventually be able to ask:

```txt
I need a prompt to do XYZ.
```

The Almanac should find the closest prompt macros, templates, and related entries, then generate a customized copy-paste prompt.
