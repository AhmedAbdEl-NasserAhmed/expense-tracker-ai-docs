# MVP Scope

## Purpose

Define the smallest version of the Smart Expense Tracker that delivers its core product promise: help users understand their spending, understand their current financial position, and make better financial decisions based on real financial behavior.

## MVP Goal

The MVP establishes a reliable financial foundation before introducing AI or advanced financial decision support.

The core loop is:

1. Build an initial financial profile.
2. Track real expenses with minimal friction.
3. Continuously calculate the user's current spending position.
4. Build a history of actual financial behavior.
5. Provide basic statistics and monthly summaries.
6. Maintain enough history to support future personalized guidance.

## In Scope

### Authentication

- Email/password authentication.
- Google authentication.
- Email-based password reset.
- Permanent account deletion after explicit confirmation.

### Financial Profile

The user can provide and update:

- One currency.
- Monthly income.
- Multiple income streams.
- One-time income for a specific month/date.
- Current savings.
- Marital status.
- Fixed financial commitments.
- Recurring expenses.
- Current available spending capacity when onboarding occurs partway through a month.
- Remaining commitments for the current month.

Profile changes apply from an effective date and do not rewrite historical financial data.

### Expense Categories

- Predefined common expense categories.
- Custom categories.
- Categories selected during onboarding are available during expense entry.

### Expense Tracking

Users can quickly record an expense using:

- Amount.
- Category.
- Payment method.
- Transaction date, defaulting to the current date.

Users can:

- Record expenses for previous dates.
- Edit amount, category, payment method, and transaction date.
- Delete expenses.
- Add multiple expenses in one session for efficient catch-up.

### Recurring Expenses

Users can define recurring expenses during onboarding or later.

A recurring expense includes:

- Amount.
- Category.
- Frequency.
- Start date.
- End date or another explicit end condition when applicable.

Recurring rules are explicit and can be changed or ended at any time. Changes affect future calculations only.

### Payment Methods and Credit Card Liability

Payment method is required for an expense.

For MVP, the system distinguishes owned-money payment methods such as cash/debit from credit-card spending.

Credit-card spending increases liability. Paying the credit-card bill later settles the liability and does not create a second expense for the original purchase.

Full bank-account management is outside MVP scope.

### Monthly Spending Position

The application continuously calculates the user's current-month spending position.

It shows:

- Available spending capacity.
- Amount spent so far.
- Remaining spending capacity.
- Amount by which spending exceeds capacity when applicable.
- Daily spending guidance based on remaining capacity and remaining days.

Spending capacity is guidance, not a hard limit. The application never blocks spending because the user exceeded capacity.

Available spending capacity accounts for applicable income, fixed commitments, and remaining recurring commitments.

### Overspending Handling

Overspending does not automatically become debt.

When the difference needs clarification, the application asks how the user funded it. Options include debt/credit card, borrowed money, savings, other income, and other.

If savings were used, the application asks the user to confirm the amount before changing recorded savings.

### Spending History and Statistics

The application provides:

- Detailed expense history.
- Month, category, and payment-method filters.
- Expense search.
- Expense editing and deletion.
- A dedicated monthly overview for each month.
- Basic category and monthly statistics.

### Missing Days

A day with no recorded expense is not automatically considered a zero-spending day.

A day can be:

- Spending recorded.
- Confirmed no spending.
- Unknown/untracked.

Users can catch up on missing days later and may leave a day unknown.

### Dashboard

The main screen focuses on the current month and provides:

- Current available spending capacity.
- Amount spent.
- Remaining capacity.
- Daily spending guidance.
- Category consumption.
- Overspending when applicable.
- Recent expenses.
- Quick add-expense action.

### Goals

Goals are separate from onboarding and can be created when the user chooses.

The application does not require a goal during onboarding. Personalized goal guidance requires sufficient financial history.

### Observation Period

The first three months are primarily an observation period.

The application does not automatically interpret unused capacity as savings during this period.

### Notifications

The MVP supports one daily expense-tracking reminder near the end of the day when no expense has been recorded. The user can record expenses or confirm no spending.

## Out of Scope

- AI-powered recommendations.
- AI financial chatbot.
- AI purchase decision assistant.
- Bank synchronization.
- Automatic transaction import.
- Full bank-account management.
- Receipt OCR.
- Voice expense recording.
- Investment tracking.
- Family accounts.
- Subscription detection.
- Advanced forecasting.
- Financial health score.
- Automatic allocation of unused money to goals or savings.
- Multi-currency support.
- Proactive AI financial notifications.

## MVP Product Principle

The MVP prioritizes accurate financial tracking and a low-friction experience over advanced intelligence.

AI and advanced recommendations will be built only after the application has established a trustworthy financial data foundation.
