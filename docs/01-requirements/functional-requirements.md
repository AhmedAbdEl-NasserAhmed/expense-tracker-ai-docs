# Functional Requirements

## Authentication

- The system shall support account creation and login using email/password.
- The system shall support Google authentication.
- The system shall support password reset through email for email/password accounts.
- The system shall allow the user to permanently delete their account after explicit confirmation.

## Onboarding

- The system shall collect the user's selected currency.
- The system shall collect monthly income and support multiple income streams.
- The system shall collect current savings.
- The system shall collect marital status.
- The system shall collect fixed financial commitments.
- The system shall allow the user to select predefined recurring expense categories and add custom categories.
- The system shall collect the user's current available money when onboarding begins after the start of a month.
- The system shall collect remaining commitments for the current month when applicable.
- The system shall calculate the user's available spending capacity for the remainder of the current month.
- After successful onboarding, the system shall route the user to the dashboard.
- The dashboard shall show the user's current financial position and prompt the user to record the first expense.

## Financial Profile

- The user shall be able to view their financial profile.
- The user shall be able to add, edit, or remove income streams.
- The user shall be able to add one-time income for a specific date/month.
- The user shall be able to manage recurring expenses and fixed commitments from the profile.
- Changes to profile values shall apply from an effective date and shall not rewrite historical financial data.
- The user shall be able to update their recorded savings.
- The system shall ask the user to confirm before changing savings based on a suggested change.

## Expense Categories

- The system shall provide predefined common expense categories.
- The user shall be able to create custom expense categories.
- Categories selected during onboarding shall be available for expense entry.

## Expenses

- The user shall be able to create an expense with amount, category, payment method, and transaction date.
- The transaction date shall default to the current date.
- The user shall be able to record an expense for a previous date.
- The user shall be able to edit amount, category, payment method, and transaction date.
- The user shall be able to delete an expense.
- The user shall be able to enter multiple expenses in one session.
- The user shall be able to optionally turn an expense into a recurring expense rule.
- The system shall not require the user to answer a recurrence question for every expense.

## Recurring Expenses

- The user shall be able to create recurring expenses during onboarding.
- The user shall be able to create recurring expenses later from the financial profile or expense flow.
- A recurring expense shall define its amount, category, frequency, start date, and an end condition when applicable.
- The user shall be able to change or end a recurring expense at any time.
- Changes shall affect future calculations only.
- Ending a recurring expense shall not modify historical expenses or monthly summaries.

## Payment Methods and Liabilities

- Every expense shall have a payment method.
- The system shall distinguish owned-money payment methods such as cash/debit from credit-card spending.
- Credit-card spending shall increase the user's recorded credit-card liability.
- Paying a credit-card bill shall settle liability and shall not create a duplicate expense for the original purchase.
- Full bank-account management is not required for the MVP.

## Monthly Financial Position

- The system shall calculate available spending capacity for the current month.
- Available spending capacity shall account for applicable income, fixed commitments, and remaining recurring commitments.
- The system shall show amount spent during the current month.
- The system shall show remaining spending capacity.
- The system shall show the amount by which spending exceeds capacity when applicable.
- The system shall not block the user from spending when capacity is exceeded.
- The dashboard shall show a daily spending amount derived from remaining spending capacity and remaining days, as guidance rather than a hard limit.

## Overspending

- Overspending shall not automatically be classified as debt.
- When required, the system shall ask the user how overspending was funded.
- Funding choices shall include debt/credit card, borrowed money, savings, other income, and other.
- If savings are selected, the system shall ask the user to confirm the amount before reducing recorded savings.

## Missing Days

- The system shall not interpret a day with no recorded expense as zero spending automatically.
- A day shall be distinguishable as recorded spending, confirmed no spending, or unknown/untracked.
- If the user has missing days, the system shall allow them to catch up later.
- The user may record expenses, explicitly confirm no spending, or leave the day unknown.
- The system shall avoid repeated reminders for each individual missing day.

## Dashboard

The current-month home screen shall provide:

- Current available spending capacity.
- Amount spent this month.
- Remaining spending capacity.
- Daily spending guidance.
- Category spending/consumption.
- Current overspending when applicable.
- Recent expenses.
- A primary action to add an expense.

## Expense History

- The system shall provide a dedicated expense history area.
- The user shall be able to filter expenses by month.
- The user shall be able to filter expenses by category.
- The user shall be able to filter expenses by payment method.
- The user shall be able to search expenses.
- The user shall be able to edit or delete expenses from history.
- The user shall be able to catch up on missing days from the history area.

## Monthly Overview

- The system shall provide a dedicated monthly overview area separate from detailed expense history.
- Each month shall contain the financial information applicable to that month.
- The monthly overview shall show income, commitments, spending capacity, actual spending, remaining capacity or overspending, category breakdown, and relevant payment/liability information where available.
- Historical months shall remain based on the financial data applicable to those months.

## Goals

- Goals shall be separate from onboarding.
- The user shall be able to create a goal when they choose.
- Goals shall not be required for MVP onboarding.
- Personalized goal guidance shall require sufficient financial history.

## Notifications

- The system shall be able to send one daily expense-tracking reminder near the end of the day when no expense has been recorded.
- The reminder shall ask whether the user spent anything rather than assuming they forgot.
- The user shall be able to record expenses or confirm no spending.

## Observation Period

- The first three months shall primarily be used to observe actual financial behavior.
- The system shall not automatically interpret unused spending capacity as intentional savings during this period.
- Advanced personalized recommendations are outside the MVP.
