# Non-Functional Requirements

These requirements capture the quality expectations currently established for the MVP. Technical targets that require architectural decisions will be refined later.

## Usability

- Expense entry should require minimal user input.
- The primary expense flow should be fast enough to encourage daily use.
- Users should be able to catch up on missed days without being forced through one expense flow at a time.
- The application should not overwhelm users with repeated notifications.

## Data Integrity

- Historical financial data must not be rewritten when current profile values change.
- Historical expenses must remain unchanged when recurring expenses are modified or ended.
- The system must distinguish unknown/untracked days from confirmed no-spending days.
- Credit-card bill payments must not double-count the original expense.

## Privacy and Account Control

- Users must explicitly confirm permanent account deletion.
- Financial data must be associated with the authenticated user and isolated from other users.

## Consistency

- Financial calculations for a historical month should use the income, commitments, and other financial conditions applicable to that month.
- The same business definitions must be used consistently across dashboard, history, and monthly overview.

## Scope Constraint

- AI is not part of the MVP.
- The MVP should prefer simple, deterministic financial calculations over complex predictive systems.

## Open Technical Targets

The following are intentionally deferred until architecture and implementation design:

- Exact performance targets.
- Availability targets.
- Scaling targets.
- Backup and disaster-recovery targets.
- Detailed observability requirements.
- Detailed security controls.
