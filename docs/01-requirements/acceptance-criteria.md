# Acceptance Criteria

## Onboarding

### AC-01 — Complete onboarding
- Given a new authenticated user has provided the required onboarding information
- When the user completes onboarding
- Then the system creates the initial financial profile
- And calculates the applicable current-month spending capacity
- And enables the selected expense categories
- And routes the user to the dashboard
- And prompts the user to record the first expense.

### AC-02 — Mid-month onboarding
- Given the user starts after the beginning of the current month
- When onboarding requests the current-month starting position
- Then the user can provide available spending capacity for the remainder of the month
- And tracking starts from the user's onboarding point without reconstructing prior activity.

## Expenses

### AC-03 — Add expense
- Given the user is on an expense-entry flow
- When the user provides amount, category, payment method, and date
- Then the system creates the expense in the user's history.

### AC-04 — Default transaction date
- Given the user starts a new expense today
- Then the transaction date defaults to today
- And the user can change it before saving.

### AC-05 — Edit/delete expense
- Given an existing expense
- When the user edits or deletes it
- Then future calculations based on the expense reflect the change
- And unrelated historical expenses remain unchanged.

### AC-06 — Multiple expenses
- Given the user needs to catch up on several expenses
- When the user uses the multiple-expense flow
- Then they can enter several expenses before submitting the session.

## Recurring Expenses

### AC-07 — Recurring rule
- Given the user explicitly chooses to create a recurring expense
- When the required recurrence information is provided
- Then a recurring rule is created.

### AC-08 — Change recurring expense
- Given a recurring expense exists
- When the user changes or ends it with an effective date
- Then future calculations use the new rule
- And historical expenses and months remain unchanged.

## Financial Position

### AC-09 — Current capacity
- Given applicable income and commitments exist for the month
- When the dashboard is opened
- Then it shows spending capacity, spent amount, and remaining capacity.

### AC-10 — Daily guidance
- Given the user has positive remaining spending capacity and remaining days
- Then the dashboard can show a daily spending guidance amount based on those values.

### AC-11 — Overspending
- Given the user's spending exceeds available capacity
- Then the system shows the amount exceeded
- And does not block additional spending.

### AC-12 — Funding overspending
- Given overspending requires clarification
- When the user selects savings as the funding source
- Then the system asks for confirmation before changing recorded savings.

## Missing Days

### AC-13 — Unknown day
- Given no expense is recorded for a day
- Then the system does not automatically classify the day as zero spending.

### AC-14 — Confirm no spending
- Given a day has no recorded expenses
- When the user explicitly confirms no spending
- Then the day is recorded as confirmed no spending.

### AC-15 — Catch up later
- Given one or more days are untracked
- When the user visits the history/catch-up experience
- Then they can add expenses, confirm no spending, or leave a day unknown.

## History

### AC-16 — Expense history filters
- Given the user opens expense history
- Then they can filter by month, category, and payment method
- And search expenses.

### AC-17 — Monthly overview
- Given a month has financial data
- When the user opens that month
- Then the system shows the financial information applicable to that month.

## Account

### AC-18 — Password reset
- Given a user has an email/password account and cannot remember the password
- When they request a password reset
- Then the system provides an email-based recovery flow.

### AC-19 — Account deletion
- Given the user requests permanent account deletion
- When they explicitly confirm
- Then the system initiates deletion of the account and associated financial data according to the final data-retention design.
