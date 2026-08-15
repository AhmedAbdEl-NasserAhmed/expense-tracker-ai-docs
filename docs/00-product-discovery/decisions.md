# Architectural & Product Decisions

## Decision #001 — Goals are separate from onboarding

Financial goals are not required during onboarding. Users can create goals separately when they choose.

## Decision #002 — Personalized guidance requires history

The application should first observe actual financial behavior before providing personalized guidance. The first three months are primarily an observation period.

## Decision #003 — Expense categories are predefined with custom additions

Common categories are provided during onboarding and users can add custom categories.

## Decision #004 — Onboarding builds the initial financial profile

Onboarding establishes the user's starting financial position before expense tracking begins.

## Decision #005 — Expense entry is intentionally minimal

The primary expense flow requires amount, category, and payment method. Transaction date defaults automatically and can be changed.

## Decision #006 — Recurring expenses are explicit

Users can define recurring expenses during onboarding or later. The application does not ask a recurrence question for every normal expense.

## Decision #007 — Credit cards represent liability

A credit-card purchase is an expense and increases liability. Paying the credit-card bill settles the liability and must not create a duplicate expense.

## Decision #008 — Spending capacity is guidance, not a limit

The application shows remaining spending capacity and daily spending guidance but never blocks the user from spending.

## Decision #009 — Overspending is not automatically debt

If spending exceeds capacity, the system does not assume debt. The user can explain how the difference was funded.

## Decision #010 — Savings changes require user confirmation

Unused capacity does not automatically become savings. When the application proposes a savings change, the user confirms the amount.

## Decision #011 — Missing days are explicitly modeled

No recorded expense is not automatically treated as zero spending. Days can be spending recorded, confirmed no spending, or unknown.

## Decision #012 — Historical data is preserved

Changes to income, commitments, recurring expenses, and other profile values apply from an effective date and do not rewrite historical data.

## Decision #013 — Mid-month onboarding starts from the user's declared position

The MVP does not reconstruct spending before onboarding. When onboarding starts after the month begins, the user provides available spending capacity for the remainder of that month.

## Decision #014 — One currency per user in MVP

The MVP uses one currency for the user's financial profile.

## Decision #015 — Dashboard is current-month focused

The main screen focuses on current-month financial position, category consumption, daily guidance, recent expenses, and quick expense entry.

## Decision #016 — Expenses and months are separate views

Detailed transaction history and month-level financial overviews are separate areas of the product.

## Decision #017 — AI is postponed

AI-powered recommendations, purchase decision assistance, and AI chat are outside MVP scope. The MVP first establishes reliable financial data and deterministic calculations.

## Decision #018 — Authentication options

The MVP supports email/password and Google authentication, including email-based password reset for password accounts.

## Decision #019 — Account deletion

Users can permanently delete their account and associated financial data after explicit confirmation.
