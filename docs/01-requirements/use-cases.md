# Use Cases

## UC-01 — Create Account

**Actor:** User

The user creates an account using email/password or Google authentication.

**Outcome:** An authenticated user account exists.

## UC-02 — Complete Onboarding

**Actor:** User

The user provides the financial information required to establish the initial financial profile.

**Outcome:** The profile is created, current-month spending capacity is established, selected categories are available, and the user is routed to the dashboard to record the first expense.

## UC-03 — Add Expense

**Actor:** User

The user records an amount, category, payment method, and transaction date.

**Outcome:** The expense becomes part of the user's financial history and affects applicable calculations.

## UC-04 — Catch Up Expenses

**Actor:** User

The user reviews missing days and records one or more historical expenses.

**Outcome:** Previously unknown days become financially represented by the user's entered data.

## UC-05 — Confirm No Spending

**Actor:** User

The user explicitly marks a missing day as having no spending.

**Outcome:** The day is distinguished from an unknown/untracked day.

## UC-06 — Manage Recurring Expense

**Actor:** User

The user creates, edits, or ends a recurring expense.

**Outcome:** Future financial calculations reflect the current recurring rule without rewriting historical expenses.

## UC-07 — Review Current Month

**Actor:** User

The user opens the dashboard.

**Outcome:** The user sees current spending capacity, spending, daily guidance, category consumption, and recent expenses.

## UC-08 — Review Expense History

**Actor:** User

The user searches and filters detailed expense history.

**Outcome:** The user can inspect, edit, or delete historical expenses.

## UC-09 — Review Monthly Overview

**Actor:** User

The user selects a month.

**Outcome:** The system presents the financial information and outcome for that month.

## UC-10 — Manage Financial Profile

**Actor:** User

The user updates income, savings, commitments, recurring expenses, categories, or other profile information.

**Outcome:** Future calculations reflect the change from its effective date while historical data remains intact.

## UC-11 — Handle Overspending

**Actor:** User

The user exceeds available spending capacity.

**Outcome:** The system shows the excess without blocking spending and may ask how the difference was funded.

## UC-12 — Confirm Savings Change

**Actor:** User

The system proposes changing recorded savings based on a financial event.

**Outcome:** Savings are changed only after user confirmation.

## UC-13 — Receive Daily Reminder

**Actor:** User / System

No expense is recorded for the day.

**Outcome:** The system may send one reminder asking whether the user spent anything.

## UC-14 — Create Goal

**Actor:** User

The user creates a future financial goal outside onboarding.

**Outcome:** A goal exists and can later be evaluated against the user's financial history.

## UC-15 — Delete Account

**Actor:** User

The user explicitly confirms permanent account deletion.

**Outcome:** The user's account and associated financial data are deleted according to the eventual data-retention policy.
