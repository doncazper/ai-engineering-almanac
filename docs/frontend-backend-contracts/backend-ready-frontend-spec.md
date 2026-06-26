---
id: backend-ready-frontend-spec
title: Backend-Ready Frontend Spec
category: frontend-backend-contracts
status: draft
aliases:
  - backend-ready UI spec
  - frontend-to-backend implementation spec
tags:
  - frontend
  - backend
  - api-design
  - product-spec
related:
  - field-to-backend-mapping
  - api-contract
  - contract-first-development
  - frontend-backend-handoff-packet
---

# Backend-Ready Frontend Spec

## Definition

A frontend feature specification detailed enough for backend implementation before the frontend is fully wired.

## Core Concept

The backend should be built against a stable product contract, not against guesses from a half-finished UI.

## Why It Matters

A backend-ready frontend spec reduces integration bugs by making fields, endpoints, validation, permissions, and states explicit before implementation begins.

## Prompt Macro

```md
Generate a backend-ready frontend spec for this feature.

Include mock screenshots, user flows, field-to-backend mappings, API endpoints, request/response payloads, database schema, validation rules, loading states, empty states, error states, permission rules, analytics events, mock data fixtures, and test cases.
```

## Related Terms

- Field-to-Backend Mapping
- API Contract
- Contract-First Development
- Integration-Ready Backend
- Mock API
- Fixture Fidelity
