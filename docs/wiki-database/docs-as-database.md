---
title: "Docs-as-Database"
slug: "docs-as-database"
status: "seed"
section: "Wiki Database"
alises:
  - "Documentation as Data"
  - "Queryable Knowledge Base"
  - "Frontmatter Schema Design"
tag:
  - content-strategy
  - data-modeling
  - documentation
  - technical-writing
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Docs-as-Database

## Definition

Treating documentation files (Markdown, YAML) as a structured database where queries can be run against frontmatter fields like `status`, `section`, `tags`, and `source_tier`.

## Core Concept

Traditional wikis are flat document trees. Docs-as-database treats pages as **records in a table**, enabling filtering: "show me all draft entries in section X that need verification" or "find all canonical prompt macros tagged with security."

## Why It Matters

As the knowledge base grows to 100+ entries, browsing folders becomes impossible. Database-style querying makes the corpus searchable and manageable.

## Real-World Example

**Query:** Find all seed-status entries that need source verification
```bash
git grep -l 'status: "seed"' docs/**/*.md | head -20
```

**Query via MkDocs plugin (mkdocs-macros-plugin):**
Generate a dynamic page listing:
- All draft entries created this month
- Filtered by section = "Frontend–Backend Contracts"
- Sorted by updated date

**Query for reports:**
```sql
-- Conceptual SQL representation of the docs database
SELECT title, status, source_tier 
FROM docs 
WHERE section = 'Prompt Macros' 
  AND status IN ('seed', 'draft') 
ORDER BY created DESC;
```

## Common Mistakes

- Not using consistent frontmatter schemas (inconsistent field names)
- Storing data in prose instead of structured fields (can't query)
- No validation on required fields (status, tags, section)
- Treating the wiki like a blog instead of a knowledge base

## Related Terms

- Content Modeling
- Metadata Schema Design
- Headless CMS Architecture
- Git as Database
- Static Site Generation with Data Layers

## Mental Model

Docs-as-database is **SQL for writers**: you write prose but think in tables.

## Production Notes

Enforce frontmatter schemas using YAML validation (jsonschema or pydantic). Use MkDocs plugins like `mkdocs-macros-plugin` or `mkdocs-github-authors-plugin` to query and display data dynamically. Consider migrating to a proper CMS (Notion, Contentful) only when Git-based querying becomes insufficient.