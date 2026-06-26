---
title: "Define Done"
slug: "define-done"
status: "seed"
section: "Prompt Macros"
alises:
  - "Acceptance Criteria Definition"
  - "Exit Conditions"
  - "Completion Gates"
tag:
  - agile
  - project-management
  - quality-assurance
  - prompt-engineering
source_tier: "mixed"
created: "2026-06-25"
updated: "2026-06-25"
---

# Define Done

## Definition

An explicit specification of acceptance criteria, exit conditions, and completion gates for a task, feature, or project — stated before work begins.

## Core Concept

Without "define done," teams argue about whether something is finished. With it, the criteria are objective and agreed upon upfront.

## Why It Matters

"Done" drifts: frontend thinks they're done when UI works; backend thinks they're done when API returns 200; QA says not done until edge cases tested. Explicit definition prevents rework and scope disputes.

## Real-World Example

**Task:** Implement user login

**Define Done:**
1. **Functional**: Users can log in with email/password or SSO (Google, GitHub)
2. **Security**: Passwords hashed with bcrypt cost 12; rate limiting 5 attempts/min; HTTPS only
3. **Error States**: "Invalid credentials" message shown; password reset link works; account lockout after 5 failures
4. **Testing**: Unit tests for auth logic; integration test for login flow; load test (100 concurrent logins)
5. **Documentation**: API docs updated; runbook for locked accounts; monitoring dashboard shows failed login rate
6. **Accessibility**: Form works with screen readers; keyboard navigation functional; contrast ratios pass WCAG AA

## Common Mistakes

- Defining done only as "code written" (not tested, not documented)
- Different stakeholders having different definitions of done
- Adding criteria after work has started (moving goalposts)
- Not including non-functional requirements (performance, security, accessibility)

## Related Terms

- Acceptance Criteria (Agile)
- Definition of Done (Scrum)
- Exit Criteria
- Quality Gates
- Proof of Correctness

## Mental Model

Define done is a **contract with your future self** about what "finished" means.

## Production Notes

Write Define Done in the ticket/issue description before development starts. Check each item off during the PR review.