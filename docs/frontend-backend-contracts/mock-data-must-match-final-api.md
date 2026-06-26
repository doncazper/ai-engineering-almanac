---
title: "Mock Data Must Match Final API"
slug: "mock-data-must-match-final-api"
status: "seed"
section: "Frontend–Backend Contracts"
alises:
  - "Production-Ready Mocks"
  - "API-Accurate Test Data"
  - "Schema-Aware Mocking"
tag:
  - testing
  - mock-data
  - frontend-development
  - api-contracts
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Mock Data Must Match Final API

## Definition

A development discipline requiring that frontend mock data (used during UI development before the real API exists) structurally matches the final backend response shape, field names, and validation constraints.

## Core Concept

Frontend developers often mock random JSON (`{ id: 1, name: "Test" }`) because the backend isn't ready. If the real API returns `{ userId: "uuid", displayName: string, createdAt: iso8601 }`, the frontend breaks during integration.

## Why It Matters

Mismatched mock data forces refactoring after UI work is complete. Matching mocks mean the frontend is production-ready when the backend ships.

## Real-World Example

**Wrong (random mocks):**
```json
{
  "users": [
    { "id": 1, "name": "Alice", "email": "alice@test.com" }
  ]
}
```

**Right (API-contract mocks):**
```json
{
  "data": [
    {
      "userId": "550e8400-e29b-41d4-a716-446655440000",
      "profile": {
        "displayName": "Alice Smith",
        "avatarUrl": "https://cdn.example.com/avatars/..."
      },
      "emailAddress": "alice@company.com",
      "createdAt": "2024-01-15T10:30:00Z",
      "roles": ["editor", "admin"]
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 47
  }
}
```

## Common Mistakes

- Using sequential integers (1, 2, 3) instead of UUIDs when the real API uses UUIDs
- Missing nested objects or arrays that exist in production
- Forgetting metadata fields (`createdAt`, `updatedAt`, pagination)
- Not including error response examples (400, 401, 500 payloads)

## Related Terms

- Contract Testing
- OpenAPI Mock Server
- Prisma Mocking
- JSON Schema Validation
- Test Data Management

## Mental Model

Mock data must match final API like **flight simulators match real planes**: same controls, same physics, same edge cases.

## Production Notes

Generate mock data from the OpenAPI spec or database schema. Use tools like Prism (mock server from OpenAPI), MSW (Mock Service Worker), or Prisma Mocking.