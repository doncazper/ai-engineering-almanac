---
title: "Frontend–Backend Contract Engineering"
slug: "frontend-backend-contract-engineering"
status: "seed"
section: "Frontend–Backend Contracts"
alises:
  - "API Contract Design"
  - "Contract-First Development"
  - "Interface Specification"
tag:
  - api-design
  - contracts
  - architecture
  - integration
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Frontend–Backend Contract Engineering

## Definition

The discipline of designing explicit agreements (contracts) between frontend and backend teams regarding data structures, API endpoints, error codes, validation rules, and behavioral expectations.

## Core Concept

Contract engineering treats the boundary between frontend and backend as a **formal interface** that can be versioned, tested, and enforced — not an informal understanding.

## Why It Matters

Without contracts, "it works on my machine" becomes the default state. With contracts, integration failures are caught at build time or in CI, not during UAT.

## Real-World Example

A contract document includes:

```yaml
contract_version: "1.0.0"
service: "Projects API"
endpoints:
  - path: "/api/v1/projects"
    method: "GET"
    request:
      query_params:
        page: integer (default: 1)
        limit: integer (default: 20, max: 100)
        status: enum[active,archived] (optional)
    response_200:
      type: array
      items:
        id: uuid
        name: string
        slug: string
        status: enum[active,archived]
        created_at: iso8601
    errors:
      400: "Invalid query parameters"
      401: "Unauthorized"
      429: "Rate limit exceeded"
```

## Common Mistakes

- Assuming contracts are implied by code (they're not)
- Not versioning contracts alongside APIs
- Changing backend schemas without bumping contract versions
- Frontend hardcoding assumptions about field existence

## Related Terms

- API Contract Testing
- Pact (Contract Testing Tool)
- OpenAPI Specification
- Schema Registry
- Backend-for-Frontend (BFF)

## Mental Model

Contract engineering is **treaty negotiation between sovereign nations** (frontend and backend), not family dinner conversation.

## Production Notes

Use tools like Pact, Spring Cloud Contract, or Dredd to enforce contracts in CI. Generate client SDKs from OpenAPI specs so both sides use the same source of truth.