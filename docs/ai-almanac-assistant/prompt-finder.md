---
title: "Prompt Finder"
slug: "prompt-finder"
status: "seed"
section: "AI Almanac Assistant"
aliases:
  - "Prompt Router"
  - "Prompt Recommender"
  - "Prompt Concierge"
  - "Prompt Librarian"
tags:
  - prompt-engineering
  - retrieval
  - semantic-search
  - rag
  - product-feature
  - ai-assistant
---

# Prompt Finder

## Definition

Prompt Finder is an AI-powered retrieval feature that lets users describe what they want to accomplish and returns the closest prompt macros, workflow phrases, templates, and Almanac entries.

## User story

As a user, I want to type:

```txt
I need a prompt to do XYZ.
```

So the Almanac can:

1. Find the closest reusable prompt macros.
2. Explain why each prompt matched.
3. Generate an adapted copy-paste prompt.
4. Link to the source wiki entries.
5. Suggest related templates and terms.

## Why this matters

A prompt library becomes much more valuable when users can search by intent instead of memorizing exact names.

The user may say:

```txt
I want to avoid debugging frontend/backend integration later.
```

The system should understand that this relates to:

- Backend-Ready Frontend Spec
- Field-to-Backend Mapping
- Frontend-Backend Handoff Packet
- Contract-First Development
- Mock Data Must Match Final API

Even if the user never says those exact words.

## MVP behavior

The first version should return:

- Top 3-5 matching prompt macros.
- Top 3 related wiki entries.
- One adapted copy-paste prompt.
- A short explanation of why the results matched.
- Links back to source entries.

## What it should not be at first

Do not start with a general chatbot over the whole wiki.

Start with a focused finder:

```txt
User intent -> prompt/template matches -> adapted prompt
```

## Retrieval layers

### Layer 1: Keyword search

Good for exact matches such as `backend-ready`, `RAG`, `eval`, or `field mapping`.

### Layer 2: Alias and tag matching

Good for phrases like:

```txt
make the backend match the frontend
```

which should map to:

```txt
frontend-backend contracts
field-to-backend mapping
API contracts
mock data fixture
```

### Layer 3: Semantic search

Good for vague intent, such as:

```txt
I need to make sure my AI answer is grounded in the docs.
```

which should map to:

```txt
RAG
source fidelity
citation grounding
retrieval evaluation
hallucination checks
```

### Layer 4: LLM rerank / adaptation

After retrieval, an LLM can explain why each result matched and compose a customized prompt.

## Suggested API design

```txt
POST /api/prompt-finder/search
POST /api/prompt-finder/adapt
POST /api/prompt-finder/feedback
```

## Search response shape

```json
{
  "query": "I need a prompt to turn my app idea into frontend/backend specs",
  "matches": [
    {
      "id": "backend-ready-frontend-spec",
      "title": "Generate a Backend-Ready Frontend Spec",
      "type": "prompt_macro",
      "score": 0.94,
      "why_matched": "The user wants to convert product intent into implementation-ready frontend/backend requirements.",
      "url": "/prompt-macros/backend-ready-frontend-spec/",
      "tags": ["frontend", "backend", "api-contracts"]
    }
  ]
}
```

## Security rule

Never expose model API keys in frontend JavaScript.

If GitHub Pages hosts the frontend, use a serverless backend for AI calls:

- Vercel Function
- Netlify Function
- Cloudflare Worker
- Supabase Edge Function
- Small API service

## Data sources

Prompt Finder should search:

- `data/prompt_macros.yml`
- `data/terms.yml`
- Markdown frontmatter from `docs/`
- canonical entry content
- aliases
- tags
- examples
- related terms

## First 10 prompt macros to index

1. Generate a Backend-Ready Frontend Spec
2. Extract Conversation Into Durable Knowledge Objects
3. Turn This UI Into Backend Requirements
4. Map Every UI Field to Database and API Fields
5. Define Done
6. Create a Verifier
7. Identify Integration Risks Before Implementation
8. Mock Data Must Match Final API
9. Create a Frontend-Backend Handoff Packet
10. Turn This Repeated Workflow Into a Skill

## Acceptance criteria for MVP

- User can enter a vague task description.
- System returns relevant prompt macros.
- Results include title, score, why matched, tags, and links.
- System generates one adapted prompt.
- No API key is exposed in frontend code.
- The first version works with static docs plus a small backend service.

## Mental model

Prompt Finder is a librarian for reusable AI workflows.

## Long-term version

The long-term version turns the Almanac into a workflow retrieval engine:

```txt
Describe problem -> retrieve closest workflow -> adapt prompt -> execute -> preserve result
```
