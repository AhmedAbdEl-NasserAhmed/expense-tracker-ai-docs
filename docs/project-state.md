# Project State

## Current Phase
Requirements

## Status
⚠️ Requirements review complete — conditional pass

## Current Milestone
Requirements Review

## Next Milestone
Domain Modeling

## Completed Deliverables
- Product Vision
- Target User
- Product Principles
- User Journey
- Assumptions
- Product Decisions
- Glossary
- Constraints
- MVP Scope
- Functional Requirements
- Non-Functional Requirements
- Business Rules
- Use Cases
- User Stories
- Acceptance Criteria
- MVP Requirements
- Requirements Review

## Key Current Decisions
- AI is completely postponed from MVP.
- Expense tracking is manual and optimized for low friction.
- Current-month spending capacity is the primary financial position metric.
- Financial profile changes affect future calculations and do not rewrite history.
- Missing days are distinct from confirmed no-spending days.
- Credit-card spending is treated as liability and credit-card bill payment must not double-count the expense.
- Goals are separate from onboarding.
- The first three months are primarily an observation period.

## Open Questions Before Database Design
- Exact treatment of partial-month recurring commitments.
- Exact effective-date rules when income/commitments change inside a month.
- Exact credit-card statement and payment model.
- Exact definition and separation of fixed commitments versus recurring expenses.
- Exact representation of current-month starting state during mid-month onboarding.
- Exact daily spending guidance calculation.
- Detailed security, retention, and deletion implementation.
- Exact statistics and visualization definitions.
- Exact goal model and calculations.

## Next Action
Begin Domain Modeling. Resolve the open financial-domain rules before designing database tables.
