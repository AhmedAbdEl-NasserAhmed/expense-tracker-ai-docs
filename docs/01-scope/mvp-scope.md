# MVP Scope

## Purpose

Define the smallest version of the Smart Expense Tracker that delivers its core product promise: help users understand their spending, understand their current financial position, and make better financial decisions based on real financial behavior.

## MVP Goal

The MVP should establish a reliable financial foundation before introducing AI or advanced financial decision support.

The core loop is:

1. Build an initial financial profile.
2. Track real expenses with minimal friction.
3. Continuously calculate the user's current spending position.
4. Build a history of actual financial behavior.
5. Provide basic statistics and monthly summaries.
6. Maintain enough history to support future personalized guidance.

## In Scope

### 1. Financial Profile

The user can provide and update:

- Monthly income.
- Multiple income streams.
- Current savings.
- Marital status.
- Fixed financial commitments.
- Recurring expenses.
- Current available money when onboarding occurs partway through a month.
- Remaining commitments for the current month.

Profile changes must preserve their effective date so historical analysis is not rewritten.

### 2. Expense Categories

- Provide predefined common expense categories.
- Allow users to create custom categories.
- Make selected categories available during expense entry.

### 3. Expense Tracking

Users can quickly record an expense using:

- Amount.
- Category.
- Payment method.
- Transaction date, defaulting to the current date.

Users can:

- Record expenses for previous dates.
- Edit the amount.
- Edit the category.
- Edit the payment method.
- Edit the transaction date.
- Delete expenses.
- Add multiple expenses in one session for efficient catch-up.

### 4. Recurring Expenses

Users can optionally define a recurring expense.

A recurring expense includes enough information to determine its recurrence, including:

- Amount.
- Category.
- Frequency.
- Start date.
- End date or another explicit end condition when applicable.

Recurring expenses are not assumed automatically. The user explicitly chooses to create a recurring rule.

Known recurring expenses can also be entered during onboarding.

### 5. Payment Methods and Credit Card Liability

Payment method is required for an expense.

For MVP, payment methods distinguish money already owned from credit-card liability.

Credit-card spending increases the user's liability. Paying the credit-card bill later must not create a second expense for the same purchase.

Full bank-account management is outside MVP scope.

### 6. Monthly Spending Position

The application continuously calculates the user's spending position for the current month.

The user should be able to understand:

- Available spending capacity.
- Amount spent so far.
- Remaining spending capacity.
- Amount by which spending has exceeded the available capacity, when applicable.

The application does not block spending when the user exceeds their available spending capacity.

### 7. Overspending Handling

Overspending does not automatically become debt.

If the user exceeds their available spending capacity, the application records the overspending and asks how the difference was funded when that information is needed.

Possible funding sources include:

- Credit card / debt.
- Borrowed money.
- Existing savings.
- Other income.
- Other.

If the user states that savings were used, the application must ask the user to confirm the amount before changing the recorded savings balance.

### 8. Spending History and Statistics

The application builds spending history from actual recorded expenses.

It should provide basic statistics and monthly summaries, including the user's total spending and whether the month ended within or above the available spending capacity.

The first three months are primarily an observation period. The application should not automatically interpret unused money as intentional savings during this period.

### 9. Goals

Goals are a separate feature and are not required during onboarding.

Users can create goals when they choose.

Personalized goal guidance should only be introduced after sufficient financial history has been collected.

### 10. Daily Tracking Reminder

If no expense has been recorded for a day, the application may send one reminder near the end of the day asking whether the user spent anything.

The user can either record expenses or explicitly indicate that they had no spending that day.

The MVP should not send repeated reminders for the same missed day.

## Out of Scope

The following are intentionally excluded from MVP:

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
- Automatic allocation of unused money to goals or savings.

## MVP Product Principle

The MVP should prioritize accurate financial tracking and a low-friction experience over advanced intelligence.

AI and advanced recommendations will be built only after the application has established a trustworthy financial data foundation.
