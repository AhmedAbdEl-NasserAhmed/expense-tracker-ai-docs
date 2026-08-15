# Architecture Log

## Session 1

### Completed
- Defined product vision
- Defined target user persona
- Established product principles
- Created user journey
- Documented assumptions
- Recorded architectural decisions
- Created glossary

### Key Decisions
- Financial goals are separate from onboarding.
- Personalized guidance requires sufficient financial history; the first three months are primarily an observation period.
- Onboarding builds a financial profile before providing guidance.

---

## Requirements Milestone

### Completed
- Defined onboarding completion behavior.
- Defined current-month spending position.
- Defined dashboard responsibilities.
- Defined expense history and monthly overview.
- Defined recurring expense behavior.
- Defined credit-card liability behavior.
- Defined overspending and savings confirmation behavior.
- Defined missing-day behavior.
- Defined income stream and one-time income behavior.
- Defined profile change and historical-data rules.
- Defined authentication requirements.
- Defined account deletion requirement.
- Explicitly postponed AI from MVP.
- Completed requirements review.

### Key Decisions
- Available spending capacity is the primary current-month financial position metric.
- Daily spending amount is guidance, not a hard limit.
- Financial profile changes apply from an effective date and do not rewrite history.
- No recorded expense is not automatically interpreted as zero spending.
- Credit-card bill payment does not create a duplicate expense.
- Unused spending capacity is not automatically treated as savings.
- The first three months are primarily an observation period.
- One currency is supported per user in MVP.

### Requirements Review Result
**Conditional Pass**

The requirements are coherent enough to begin domain modeling, but financial calculation rules must be resolved before database schema design.

### Critical Open Domain Questions
- Exact treatment of partial-month recurring commitments.
- Exact effective-date rules when income or commitments change inside a month.
- Exact credit-card statement and payment model.
- Exact distinction between fixed commitments and recurring expenses.
- Exact representation of the current-month starting state during mid-month onboarding.
- Exact daily spending guidance calculation.

### Next Focus
- Domain modeling.
- Financial invariants.
- State transitions.
- Temporal/effective-date modeling.
- Core financial calculation rules.
