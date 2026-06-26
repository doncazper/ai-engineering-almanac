---
title: "Field-to-Backend Mapping"
slug: "field-to-backend-mapping"
status: "seed"
section: "Frontend–Backend Contracts"
alises:
  - "UI-to-API Mapping"
  - "Field Mapping Table"
  - "Frontend Backend Mapping"
tag:
  - frontend
  - backend
  - api-contracts
  - database
  - product-specs
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Field-to-Backend Mapping

## Definition

A table that maps every visible frontend field, button, filter, form input, table column, or UI component to the backend field, database column, API parameter, validation rule, and business logic that supports it.

## Core Concept

Every frontend element should have a known backend responsibility before implementation begins.

## Why It Matters

Without this, teams guess. The frontend sends `fullName`, the backend expects `name`, the database stores `display_name`, and integration becomes painful.

## Real-World Example

| UI Element | Frontend State | API Field | Backend Type | DB Column | Required | Validation | Error State |
|------------|----------------|-----------|--------------|-----------|----------|------------|-------------|
| Project Name Input | projectName | name | string | projects.name | Yes | 2–100 chars, unique per org | "Enter a project name (2–100 characters)" |
| Description Textarea | description | description | text | projects.description | No | Max 500 chars | None |
| Visibility Dropdown | visibility | visibility | enum | projects.visibility | Yes | public\|private\|org | "Select visibility level" |
| Save Button (enabled) | canSave | - | boolean | - | - | name filled + no validation errors | Disabled until valid |

## Common Mistakes

- Frontend field names do not match API names.
- Mock data does not match final API shape.
- Validation rules are undocumented.
- Error states are invented late by the frontend.

## Related Terms

- Backend-Ready Frontend Spec
- API Contract
- Schema-First Development
- Contract-First Development
- Mock Data Fixture

## Mental Model

A field-to-backend mapping is the **wiring diagram** between the product interface and the software system.

## Production Notes

Create this table before writing the backend route, database migration, frontend form, or QA test plan.