# Requirements Review

## Review Status

Requirements discovery is complete, but the requirements are **not yet ready for architecture design**.

The requirements are strong enough to establish the product direction, but several financial-domain rules need clarification before domain modeling and database design.

## Findings

### 1. Observation period is inconsistent

Earlier product decisions stated that recommendations could begin after one month, while the later product decision established a three-month observation period for saving behavior.

**Resolution:** Use three months as the minimum observation period for personalized financial-behavior guidance in the MVP. AI recommendations remain out of scope.

The earlier one-month rule should no longer be treated as authoritative.

### 2. Spending capacity calculation needs one authoritative definition

The requirements currently refer to:

- Applicable income
- Fixed commitments
- Remaining recurring commitments
- A user-provided remainder-of-month starting capacity

These concepts can overlap and could cause double counting.

Before architecture, define exactly how monthly spending capacity is calculated for:

- A normal month
- A user onboarding mid-month
- A commitment that starts mid-month
- A commitment that ends mid-month
- A one-time income event

### 3. Fixed commitments vs recurring expenses need clearer semantics

A recurring expense and a fixed commitment are not necessarily the same thing.

The domain model must explicitly define:

- Fixed commitment
- Recurring expense
- Whether one can be both
- Whether either one is included in spending-capacity calculations

### 4. Credit-card liability is underspecified

The requirements correctly distinguish a credit-card purchase from the later payment, but the MVP does not yet define the actual liability lifecycle.

Before implementation, define:

- How a credit-card liability is represented
- Whether multiple credit cards are supported
- How a bill/payment is recorded
- How partial payments work, if supported
- How the liability is shown in monthly views

Do not design a full banking system unless the product requires it.

### 5. Mid-month onboarding needs one authoritative source of truth

The current requirements allow the user to provide a starting spending capacity for the remainder of the month while also collecting income and commitments.

The system must avoid calculating a second capacity from the same information and accidentally double counting it.

The architecture should distinguish between:

- The user's normal financial profile
- The current month's starting state

### 6. Goals are in MVP, but personalized goal guidance is not

The MVP includes goal creation, while personalized guidance requires sufficient financial history and advanced recommendations are outside MVP.

This is acceptable, but the requirement should be explicit:

> Goal creation is available in MVP, but goal analysis/recommendations are limited until sufficient history exists.

### 7. Savings has two concepts that must remain separate

The requirements distinguish recorded savings from unused spending capacity, which is correct.

Before domain modeling, define:

- Current recorded savings balance
- User-confirmed savings events/changes
- Whether savings withdrawals are tracked as events
- How the current balance is derived

The system must not infer savings simply from unused capacity.

### 8. Historical data needs temporal modeling

The requirement that profile changes affect future calculations without rewriting history is important.

This applies to:

- Income streams
- Fixed commitments
- Recurring expenses
- Savings state

The architecture must preserve effective dates and historical applicability.

### 9. "Daily spending guidance" needs a business rule

The requirements say the value is derived from remaining capacity and remaining days, but do not define whether it includes today, how zero/negative capacity is handled, or what happens when future commitments exist.

This should be defined before implementation.

### 10. Missing-day model is strong and should be preserved

The distinction between:

- Spending recorded
- Confirmed no spending
- Unknown/untracked

is valuable and should remain a first-class business concept.

### 11. Account deletion needs a final data policy

The product requires deletion, but exact retention, deletion timing, backups, audit records, and third-party authentication data are intentionally deferred.

This is acceptable for now and should be resolved during security/data architecture.

## Architecture Gate Result

**Status: CONDITIONAL PASS**

The requirements are good enough to proceed to a focused **Domain Modeling** phase, but the financial calculation rules listed above must be resolved before database schema design or implementation.

## Recommended Next Phase

Do not start with database tables.

Start with:

1. Domain concepts
2. Relationships
3. Financial invariants
4. State transitions
5. Temporal/effective-date behavior
6. Core calculation rules

Only after those are stable should the database model be designed.
