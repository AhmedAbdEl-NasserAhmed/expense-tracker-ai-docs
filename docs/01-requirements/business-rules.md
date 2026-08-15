# Business Rules

## Financial Profile

1. A user has a financial profile associated with their account.
2. The profile can contain multiple income streams.
3. An income stream can be ongoing for an effective period.
4. One-time income belongs to a specific date/month.
5. Profile changes apply from an effective date and do not rewrite historical periods.
6. Recurring expenses and fixed commitments are managed through the profile.
7. Recurring expense changes affect future calculations only.

## Starting the Current Month

8. The application does not reconstruct financial activity from before the user begins using the application.
9. When onboarding starts after the beginning of a month, the user provides the available spending capacity for the remainder of that month.
10. Expense tracking begins from the user's onboarding/start point.

## Spending Capacity

11. Available spending capacity is based on income applicable to the month minus applicable fixed commitments and remaining recurring commitments.
12. Spending capacity is guidance, not a hard spending limit.
13. The application does not prevent a user from exceeding spending capacity.
14. The dashboard may derive a daily spending guidance amount from remaining capacity and remaining days.

## Expenses

15. An expense requires amount, category, payment method, and transaction date.
16. Transaction date defaults to the current date but may be changed.
17. Historical expenses may be edited or deleted.
18. Editing an expense must affect future calculations/statistics that depend on it while preserving the corrected transaction as the source of truth.
19. Multiple expenses may be entered in one session.

## Recurring Expenses

20. A recurring expense is explicitly created by the user.
21. Recurring expenses have a recurrence definition and an end condition when applicable.
22. A recurring expense may be changed or ended at any time.
23. Ending or changing a recurring expense must not modify historical expenses.

## Credit Card and Debt

24. An expense paid by credit card is still an expense at the purchase date.
25. Credit-card spending creates or increases a liability.
26. Paying the credit-card bill settles the liability and does not create another expense for the original purchase.
27. Overspending does not automatically mean debt exists.
28. If the application needs to understand how overspending was funded, the user confirms the funding source.

## Savings

29. Unused spending capacity is not automatically treated as savings.
30. During the first three months, the application primarily observes saving behavior.
31. If the application proposes changing recorded savings, the user must confirm the amount.

## Missing Days

32. No recorded expense does not automatically mean zero spending.
33. A day can be recorded as spending, confirmed no spending, or unknown.
34. Missing days can be completed later.

## Currency

35. The MVP uses one currency per user financial profile.
36. Multi-currency financial calculations are outside MVP scope.

## Goals and Recommendations

37. Goals are separate from onboarding.
38. Users may create goals when they choose.
39. Personalized goal guidance requires sufficient financial history.
40. AI-powered recommendations and purchase-decision assistance are outside MVP scope.

## Notifications

41. The MVP supports one daily expense-tracking reminder near the end of the day when no expense has been recorded.
42. The system should avoid repeated reminders for the same missed day.
