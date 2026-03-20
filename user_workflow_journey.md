# UX User Workflow Documentation: Parent Fund Management for Youth Account

## Experience Overview

**Experience:** Parent allocates and manages funds for a youth account

**Business Goal:**
Enable parents/guardians to teach financial responsibility to their children by providing tools to allocate/manage funds, set spending limits, and monitor activity, while maintaining visibility and control.

**User Goal:**
Allow parents to easily allocate funds, set spending limits, and monitor youth account activity, ensuring a safe and educational banking experience for their children.

---

## Identified Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard

**Context:** Parent is logged into the banking web application.

#### Variation 1: Quick Dashboard Access
- Parent selects "Youth Accounts" from main navigation.
- System displays dashboard with current balance, recent activity, and quick actions.

#### Variation 2: Guided Dashboard Access
- Parent selects "Accounts" > "Youth Account" from a grouped list.
- System presents an onboarding tooltip highlighting dashboard features for first-time users.

**User Goal:** Quickly access youth account overview and available actions.
**Business Goal:** Encourage engagement and foster trust by making youth account features discoverable.

**Screens:**
1.0 Youth Account Dashboard
- **Goal:** Present a clear overview of youth account status and actions.
- **Description:**
  - Shows current balance, recent transactions, spending limit, and quick actions (Add Funds, Set Limit).
  - Entry point for all youth account management tasks.
- **Design Problems:**
  - HMW make the dashboard intuitive for first-time and returning users?
  - HMW prioritize information for quick scanning?
- **Design Opportunities:**
  - What if the dashboard adapts to user behavior (e.g., highlights most-used actions)?
  - What if onboarding tips are shown contextually?

---

### Scenario 2: Allocate Funds to Youth Account

**Context:** Parent wants to transfer money from their account to the youth account.

#### Variation 1: Inline Transfer
- Parent clicks "Add Funds" on dashboard.
- Modal opens for transfer details (source account, amount).
- Confirmation and success message inline.

#### Variation 2: Stepper Flow
- Parent clicks "Add Funds" and is guided through a stepper:
  1. Select source account
  2. Enter amount
  3. Review & confirm
  4. Success screen

**User Goal:** Easily and securely transfer funds to youth account.
**Business Goal:** Increase usage of youth account features and reinforce parental control.

**Screens:**
2.0 Add Funds Modal/Flow
- **Goal:** Facilitate a smooth, error-free transfer process.
- **Description:**
  - Source account selector, amount input, validation for limits/balance.
  - Confirmation step to prevent mistakes.
  - Success feedback.
- **Design Problems:**
  - HMW minimize friction while ensuring security?
  - HMW prevent accidental or invalid transfers?
- **Design Opportunities:**
  - What if the system suggests common transfer amounts?
  - What if transfer templates are available for recurring actions?

Er.1 Insufficient Balance Error
- **Goal:** Clearly communicate when parent’s account lacks sufficient funds.
- **Description:**
  - Error message with actionable suggestions (e.g., "Choose another account" or "Deposit funds").
- **Design Problems:**
  - HMW reduce frustration when errors occur?
- **Design Opportunities:**
  - What if the system offers to schedule the transfer when funds are available?

---

### Scenario 3: Set Spending Limit

**Context:** Parent wants to configure or update a weekly spending limit for the youth account.

#### Variation 1: Dashboard Inline Edit
- Spending limit displayed on dashboard with an "Edit" button.
- Inline edit field appears for quick updates.

#### Variation 2: Dedicated Limit Management Screen
- Parent clicks "Manage Limit" and navigates to a separate screen with guidance, input, and history of changes.

**User Goal:** Easily set or adjust spending limits for their child.
**Business Goal:** Promote responsible spending and parental oversight.

**Screens:**
3.0 Spending Limit Configuration
- **Goal:** Make limit setting understandable and accessible.
- **Description:**
  - Input for weekly limit, validation for allowed values.
  - Contextual help explaining how limits work.
  - Display of current active limit.
- **Design Problems:**
  - HMW prevent confusion about how limits are applied?
  - HMW ensure parents feel in control?
- **Design Opportunities:**
  - What if the system provides recommendations based on child’s age or spending patterns?
  - What if parents can set alerts for approaching limits?

---

### Scenario 4: View Youth Spending Activity

**Context:** Parent wants to review recent transactions and spending patterns.

#### Variation 1: Transaction List on Dashboard
- Recent transactions shown directly on dashboard with filters (date, category).

#### Variation 2: Full Activity Page
- Parent clicks "View All Activity" to see a paginated/filterable transaction history with visual summaries (charts, trends).

**User Goal:** Monitor child’s spending for transparency and guidance.
**Business Goal:** Build trust and encourage ongoing use by providing clear oversight.

**Screens:**
4.0 Transaction Activity List
- **Goal:** Make it easy to scan and understand youth spending.
- **Description:**
  - List with date, merchant, amount, and remaining balance.
  - Filters for time period.
  - Visual cues for unusual activity.
- **Design Problems:**
  - HMW help parents quickly spot concerning transactions?
  - HMW support accessibility for all users?
- **Design Opportunities:**
  - What if the system highlights spending trends or anomalies?
  - What if parents can tag or comment on transactions for discussion with their child?

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation

**Context:** Parent attempts to transfer funds but lacks sufficient balance.

#### Variation 1: Inline Error Message
- Error appears below amount input with suggestions.

#### Variation 2: Error Modal with Actions
- Dedicated error modal with options to retry, choose another account, or link to deposit funds.

**User Goal:** Understand why the transfer failed and what to do next.
**Business Goal:** Reduce drop-off and frustration, encourage continued engagement.

**Screens:**
Er.1 Insufficient Balance Error (see above)

---

## Minimum Viable Experience (MVE)

**Scenario:**
Jenna, a parent, logs into her bank’s web app to allocate her child’s weekly allowance. She accesses the youth account dashboard, adds funds, sets a spending limit, and reviews her child’s recent purchases.

- **User Goal:** Quickly allocate allowance, set limits, and review spending.
- **Business Goal:** Drive adoption of youth accounts and parental engagement.

**Screen Sequence:**
1.0 Youth Account Dashboard → 2.0 Add Funds Modal/Flow → 3.0 Spending Limit Configuration → 4.0 Transaction Activity List

---

## Summary Table of Screens

| Screen # | Title                         | Goal                                        |
|----------|-------------------------------|---------------------------------------------|
| 1.0      | Youth Account Dashboard       | Overview, entry point for all actions       |
| 2.0      | Add Funds Modal/Flow          | Transfer funds to youth account             |
| 3.0      | Spending Limit Configuration  | Set/manage weekly spending limits           |
| 4.0      | Transaction Activity List     | Review youth account spending               |
| Er.1     | Insufficient Balance Error    | Communicate and resolve transfer errors     |

---

## Accessibility & Scalability Considerations
- All screens support keyboard navigation and screen readers.
- Color contrast and font sizes meet WCAG 2.1 AA standards.
- Responsive layouts for desktop and tablet.
- Error states provide clear, actionable feedback.
- Workflows are modular for future features (e.g., multiple youth accounts, notifications).

---

## Edge Cases & Additional Use Cases
- Parent with multiple youth accounts: Dashboard lists all, with drill-down.
- Parent attempts to set limit above allowed threshold: Validation and guidance provided.
- Parent reviews spending on mobile: Responsive design ensures usability.
- Parent wants to export transaction history: Download option available.
- Parent receives notification for large/unusual youth transactions: Alert system (future opportunity).

---

## Workflow Sequences (for each scenario)

### Scenario 1: Access Youth Account Dashboard
- 1.0 Youth Account Dashboard

### Scenario 2: Allocate Funds to Youth Account
- 1.0 Youth Account Dashboard → 2.0 Add Funds Modal/Flow → (Er.1 if error)

### Scenario 3: Set Spending Limit
- 1.0 Youth Account Dashboard → 3.0 Spending Limit Configuration

### Scenario 4: View Youth Spending Activity
- 1.0 Youth Account Dashboard → 4.0 Transaction Activity List

### Scenario 5: Handle Insufficient Balance
- 2.0 Add Funds Modal/Flow → Er.1 Insufficient Balance Error

---

# End of UX User Workflow Documentation
