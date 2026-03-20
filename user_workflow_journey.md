# UX Design User Workflow Documentation: Parent Managing Youth Account

## Experience Mindset

**User:** Parent/Guardian
**Experience:** Allocating and managing funds for a youth account to teach financial responsibility while maintaining visibility and control.

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard

**Context:** Parent is logged into the banking web application.
**Task:** Navigate to youth account section to view dashboard.
**Actor:** Parent
**Goal:** Quickly and easily access youth account information.

#### Workflow Variation A: Direct Navigation
- Parent logs in
- Parent clicks "Youth Accounts" from main menu
- Dashboard loads with balance, recent activity, spending limit

#### Workflow Variation B: Notification-Driven Access
- Parent receives notification (e.g., spending alert)
- Parent clicks notification link
- Dashboard loads directly, highlighting relevant activity

**User Goal:** Instantly access youth account overview
**Business Goal:** Increase engagement and transparency for parental controls

**Screens:**
1.0 Youth Account Dashboard

- **Page Goal:** Provide a clear overview of youth account status
- **Description:** Displays balance, spending limit, recent transactions, quick actions
- **Design Problems:**
  - HMW make key information immediately visible?
  - HMW reduce cognitive load for parents?
- **Design Opportunities:**
  - What if dashboard adapts to parent’s usage patterns?
  - What if quick tips for teaching financial responsibility are surfaced?

---

### Scenario 2: Allocate Funds to Youth Account

**Context:** Parent is on youth account dashboard.
**Task:** Add funds to youth account.
**Actor:** Parent
**Goal:** Transfer funds efficiently and securely.

#### Workflow Variation A: Standard Transfer
- Parent selects "Add Funds"
- Parent chooses source account
- Enters amount
- Confirms transfer
- Success message displayed

#### Workflow Variation B: Scheduled Transfer
- Parent selects "Add Funds"
- Chooses "Schedule Transfer"
- Sets frequency and amount
- Confirmation and scheduling success message

**User Goal:** Seamlessly allocate funds
**Business Goal:** Encourage regular funding, reduce friction

**Screens:**
2.0 Fund Transfer Interface

- **Page Goal:** Enable easy and secure fund transfer
- **Description:** Source account selector, amount input, confirmation, error handling
- **Design Problems:**
  - HMW prevent accidental transfers?
  - HMW communicate transfer limits and errors?
- **Design Opportunities:**
  - What if parent can set recurring transfers?
  - What if system suggests optimal funding based on youth spending?

Er.1 Insufficient Balance Error
- **Goal:** Clearly communicate funding failure
- **Description:** Error message with guidance
- **Design Problems:**
  - HMW help parent resolve insufficient funds?
- **Design Opportunities:**
  - What if system suggests alternate funding sources?

Pu.1 Transfer Success Pop-Up
- **Goal:** Confirm successful transfer
- **Description:** Pop-up with new balance and next steps

---

### Scenario 3: Set Spending Limit

**Context:** Parent is viewing youth account management section.
**Task:** Configure weekly spending limit.
**Actor:** Parent
**Goal:** Set and manage limits to teach budgeting.

#### Workflow Variation A: Manual Limit Setting
- Parent clicks "Set Spending Limit"
- Enters weekly limit
- Confirms
- Limit displayed on dashboard

#### Workflow Variation B: Guided Limit Setting
- Parent clicks "Set Spending Limit"
- Guided wizard explains benefits
- Parent selects recommended or custom limit
- Confirms
- Limit displayed

**User Goal:** Easily manage youth spending boundaries
**Business Goal:** Promote responsible spending, reduce risk

**Screens:**
3.0 Spending Limit Configuration

- **Page Goal:** Allow parent to set and modify limits
- **Description:** Limit input, contextual guidance, display of current limit
- **Design Problems:**
  - HMW make limit setting intuitive?
  - HMW prevent invalid values?
- **Design Opportunities:**
  - What if system recommends limits based on youth age/activity?
  - What if parent receives alerts when limit is approached?

Pu.2 Limit Saved Confirmation
- **Goal:** Confirm limit update
- **Description:** Pop-up with new limit and educational tip

---

### Scenario 4: View Youth Spending Activity

**Context:** Parent is viewing youth account dashboard.
**Task:** Review recent transactions.
**Actor:** Parent
**Goal:** Monitor youth spending patterns.

#### Workflow Variation A: List View
- Parent clicks "Activity"
- Transaction list loads (date, merchant, amount, balance)
- Filters for time period

#### Workflow Variation B: Pattern Analysis View
- Parent clicks "Activity"
- Transaction list + spending pattern visualization
- Parent can filter and drill down

**User Goal:** Quickly understand youth spending
**Business Goal:** Provide actionable insights for parental guidance

**Screens:**
4.0 Activity View

- **Page Goal:** Display transaction history and patterns
- **Description:** List with filters, pattern highlights, responsive layout
- **Design Problems:**
  - HMW make data easy to scan?
  - HMW surface unusual activity?
- **Design Opportunities:**
  - What if parent can tag transactions as educational moments?
  - What if system highlights savings opportunities?

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation

**Context:** Parent attempts transfer, but source account lacks funds.
**Task:** System displays error, guides parent to resolution.
**Actor:** Parent
**Goal:** Understand and resolve funding failure.

#### Workflow Variation A: Inline Error
- Parent enters transfer amount
- System checks balance
- Error message appears below input
- Parent can retry with new amount

#### Workflow Variation B: Error Dialog with Options
- Parent enters transfer amount
- System checks balance
- Error dialog appears with options:
  - Retry
  - Link another account
  - Contact support

**User Goal:** Quickly resolve failed transfer
**Business Goal:** Reduce drop-off, encourage successful funding

**Screens:**
Er.1 Insufficient Balance Error

- **Page Goal:** Communicate funding failure and options
- **Description:** Error message, actionable options
- **Design Problems:**
  - HMW reduce frustration?
  - HMW provide clear next steps?
- **Design Opportunities:**
  - What if system offers instant overdraft or alternate funding?

---

## Minimum Viable Experience (MVE)

**Scenario:** Parent allocates funds to youth account and sets spending limit.

**User Goal:** Empower parent to teach financial responsibility
**Business Goal:** Increase parental engagement and youth account usage

**Screens:**
1.0 Youth Account Dashboard -> 2.0 Fund Transfer Interface -> Pu.1 Transfer Success Pop-Up -> 3.0 Spending Limit Configuration -> Pu.2 Limit Saved Confirmation

---

## Sequence of Screens for Each Scenario & Workflow

### Scenario 1
1.0 Youth Account Dashboard

### Scenario 2
1.0 Youth Account Dashboard -> 2.0 Fund Transfer Interface -> Pu.1 Transfer Success Pop-Up -> Er.1 Insufficient Balance Error

### Scenario 3
1.0 Youth Account Dashboard -> 3.0 Spending Limit Configuration -> Pu.2 Limit Saved Confirmation

### Scenario 4
1.0 Youth Account Dashboard -> 4.0 Activity View

### Scenario 5
2.0 Fund Transfer Interface -> Er.1 Insufficient Balance Error

---

## Accessibility & Scalability Considerations

- All screens designed for keyboard navigation and screen reader compatibility
- Responsive layouts for desktop and tablet
- Error states provide clear, actionable guidance
- Modular workflows allow for future expansion (e.g., additional account types, more granular controls)

---

## Edge Cases & Use Cases

- Parent has multiple youth accounts: dashboard adapts with account selector
- Scheduled transfers fail: system notifies parent, suggests resolution
- Youth exceeds spending limit: alert sent to parent, dashboard highlights breach
- Parent attempts invalid limit: UI prevents and explains
- Parent needs support: quick access to help from error dialogs

---

## Summary

This documentation outlines systematic, user-centered workflows for managing youth accounts, balancing user needs (control, education, ease) with business objectives (engagement, trust, scalability), and ensuring accessibility for all users. Each scenario is covered with at least two workflow variations, minimum viable experience, and detailed screen goals, descriptions, design problems, and opportunities.
