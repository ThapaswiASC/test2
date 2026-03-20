# UX Workflow Documentation: Parent Fund Allocation & Management for Youth Account

## Experience Mindset

**User:** Parent/Guardian
**Experience:** Allocating and managing funds for a youth account to teach financial responsibility and maintain visibility/control.

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard

#### Context:
Parent is logged into the banking web application and navigates to the youth account section.

#### User Goal:
Quickly view youth account balance and recent activity.

#### Business Goal:
Increase parent engagement and trust by providing clear visibility and easy access to youth account information.

#### Workflow Variation 1:
1.0 Youth Account Dashboard
  - Goal: Display youth account balance, recent activity, and quick actions.
  - Description: Parent sees balance, spending limit, recent transactions, and buttons for "Add Funds" and "Set Limit".
  - Design Problems:
    - HMW make the dashboard instantly understandable?
    - HMW highlight key actions without clutter?
  - Design Opportunities:
    - What if dashboard adapts to parent’s usage patterns?
    - What if a virtual assistant summarizes recent activity?

1.1 Recent Activity Subscreen
  - Goal: Show detailed transaction history.
  - Description: Parent can filter by date, merchant, or amount.
  - Design Problems:
    - HMW make scanning activity effortless?
  - Design Opportunities:
    - What if spending patterns are visualized?

#### Workflow Variation 2:
1.0 Youth Account Dashboard (with onboarding tips)
  - Goal: Educate new users about dashboard features.
  - Description: First-time users see callouts explaining each section.
  - Design Problems:
    - HMW onboard parents without overwhelming?
  - Design Opportunities:
    - What if onboarding adapts to parent’s familiarity?

Sequence: 1.0 Youth Account Dashboard -> 1.1 Recent Activity Subscreen

---

### Scenario 2: Allocate Funds to Youth Account

#### Context:
Parent is on the youth account dashboard and selects "Add Funds".

#### User Goal:
Transfer funds easily and securely from parent account to youth account.

#### Business Goal:
Drive usage of youth account and reinforce parental control.

#### Workflow Variation 1:
2.0 Fund Transfer Screen
  - Goal: Enable fund transfer with minimal steps.
  - Description: Parent selects source account, enters amount, reviews transfer, and confirms.
  - Design Problems:
    - HMW prevent errors in fund transfer?
    - HMW make confirmation reassuring?
  - Design Opportunities:
    - What if system suggests typical transfer amounts?

2.1 Confirmation Screen
  - Goal: Confirm transfer details before execution.
  - Description: Parent reviews amount, account, and can edit or proceed.
  - Design Problems:
    - HMW prevent accidental transfers?

2.2 Success Message (Pu.1)
  - Goal: Notify parent of successful transfer.
  - Description: Pop-up or toast confirms transfer.
  - Design Problems:
    - HMW make feedback timely and clear?

#### Workflow Variation 2:
2.0 Quick Transfer Modal (Pu.2)
  - Goal: Allow fast transfers from dashboard.
  - Description: Modal overlays dashboard for quick entry.
  - Design Problems:
    - HMW balance speed and accuracy?

Sequence: 1.0 Youth Account Dashboard -> 2.0 Fund Transfer Screen -> 2.1 Confirmation Screen -> 2.2 Success Message

---

### Scenario 3: Set Spending Limit

#### Context:
Parent configures a weekly spending limit for youth account.

#### User Goal:
Easily set and modify spending limits for youth account.

#### Business Goal:
Empower parents to teach budgeting and control youth spending.

#### Workflow Variation 1:
3.0 Spending Limit Configuration Screen
  - Goal: Allow parent to set/edit weekly limit.
  - Description: Input field for limit, guidance text, save button.
  - Design Problems:
    - HMW make limits easy to understand?
    - HMW prevent invalid values?
  - Design Opportunities:
    - What if system suggests age-appropriate limits?

3.1 Limit Display Subscreen
  - Goal: Show current active limit on dashboard.
  - Description: Limit is visible and editable.

#### Workflow Variation 2:
3.0 Inline Limit Edit (dashboard)
  - Goal: Edit limit directly from dashboard.
  - Description: Inline field with save/cancel.
  - Design Problems:
    - HMW make inline editing intuitive?

Sequence: 1.0 Youth Account Dashboard -> 3.0 Spending Limit Configuration Screen -> 3.1 Limit Display Subscreen

---

### Scenario 4: View Youth Spending Activity

#### Context:
Parent selects activity section to view youth transactions.

#### User Goal:
Monitor youth spending and identify patterns.

#### Business Goal:
Increase transparency and reinforce financial education.

#### Workflow Variation 1:
4.0 Activity List Screen
  - Goal: Display transaction history with filters.
  - Description: List of transactions, filter by date/merchant/amount.
  - Design Problems:
    - HMW make scanning and filtering easy?
  - Design Opportunities:
    - What if system highlights unusual spending?

4.1 Transaction Detail Pop-Up (Pu.3)
  - Goal: Show transaction details.
  - Description: Pop-up with full info.

#### Workflow Variation 2:
4.0 Spending Pattern Visualization Screen
  - Goal: Visualize spending trends.
  - Description: Chart or graph summarizes activity.
  - Design Problems:
    - HMW make patterns actionable?

Sequence: 1.0 Youth Account Dashboard -> 4.0 Activity List Screen -> 4.1 Transaction Detail Pop-Up

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation

#### Context:
Parent attempts to transfer funds but selected account lacks sufficient balance.

#### User Goal:
Understand why transfer failed and resolve quickly.

#### Business Goal:
Reduce frustration and failed transactions, encourage account funding.

#### Workflow Variation 1:
Er.1 Insufficient Balance Error State
  - Goal: Clearly communicate error and next steps.
  - Description: Error message with actionable advice (e.g., "Add funds to your account").
  - Design Problems:
    - HMW make error actionable?

#### Workflow Variation 2:
Er.2 Inline Error with Account Funding Option
  - Goal: Allow parent to resolve error from transfer screen.
  - Description: Inline error with "Add Funds" link.
  - Design Problems:
    - HMW reduce friction in error recovery?

Sequence: 2.0 Fund Transfer Screen -> Er.1 Insufficient Balance Error State

---

## Minimum Viable Experience

### User Scenario Example
Sam, a parent, wants to allocate $50 to his child’s youth account, set a weekly spending limit, and monitor recent activity. He logs in, navigates to the youth account dashboard, adds funds, sets a limit, and reviews transactions.

---

## Screen List & Details

### 1.0 Youth Account Dashboard
- Goal: Central hub for managing youth account.
- Description: Shows balance, spending limit, recent activity, and quick actions.
- Design Problems: HMW make dashboard clear and actionable?
- Design Opportunities: What if dashboard adapts to parent’s needs?

### 2.0 Fund Transfer Screen
- Goal: Transfer funds securely.
- Description: Source account selector, amount input, confirmation.
- Design Problems: HMW prevent errors?

### 2.1 Confirmation Screen
- Goal: Confirm transfer details.
- Description: Review and confirm.

### 2.2 Success Message (Pu.1)
- Goal: Confirm transfer success.
- Description: Pop-up feedback.

### 3.0 Spending Limit Configuration Screen
- Goal: Set/edit weekly spending limit.
- Description: Input, guidance, save.

### 3.1 Limit Display Subscreen
- Goal: Show/edit current limit.

### 4.0 Activity List Screen
- Goal: Review transactions.
- Description: Filterable list.

### 4.1 Transaction Detail Pop-Up (Pu.3)
- Goal: Show transaction details.

### 4.0 Spending Pattern Visualization Screen
- Goal: Visualize spending trends.

### Er.1 Insufficient Balance Error State
- Goal: Communicate error and resolution.

### Er.2 Inline Error with Account Funding Option
- Goal: Enable quick error recovery.

---

## Screen Sequence for Each Scenario

- Scenario 1: 1.0 Youth Account Dashboard -> 1.1 Recent Activity Subscreen
- Scenario 2: 1.0 Youth Account Dashboard -> 2.0 Fund Transfer Screen -> 2.1 Confirmation Screen -> 2.2 Success Message
- Scenario 3: 1.0 Youth Account Dashboard -> 3.0 Spending Limit Configuration Screen -> 3.1 Limit Display Subscreen
- Scenario 4: 1.0 Youth Account Dashboard -> 4.0 Activity List Screen -> 4.1 Transaction Detail Pop-Up
- Scenario 5: 2.0 Fund Transfer Screen -> Er.1 Insufficient Balance Error State

---

## Accessibility & Scalability Considerations
- All screens must be accessible via keyboard and screen reader.
- Error states must be clear and actionable.
- Responsive layouts for desktop and tablet.
- Scalable workflows allow for additional features (e.g., multiple youth accounts, advanced analytics).

---

## Summary
This documentation provides systematic, user-centered workflow variations for each scenario in the parent fund allocation and management experience for youth accounts. Each workflow balances user needs, business objectives, accessibility, and scalability, with clear screen goals, descriptions, design problems, and opportunities.
