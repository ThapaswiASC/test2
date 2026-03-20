# User Workflow Journey: Parent Allocating and Managing Funds for a Youth Account

## Experience Mindset

**Primary User:** Parent/Guardian
**Experience:** Managing a youth banking account (awareness, onboarding, fund allocation, limit setting, activity monitoring, troubleshooting)

---

## Identified Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged in and wants to view/manage their child's account.

#### Workflow Variation A: Direct Navigation
- Parent logs in → Main dashboard → Clicks 'Youth Accounts' → Youth Account Dashboard

#### Workflow Variation B: Notification-Driven Access
- Parent logs in → Receives notification (e.g., 'Review recent youth activity') → Clicks notification → Youth Account Dashboard

**User Goal:** Quickly access youth account information and controls.
**Business Goal:** Increase engagement and transparency for account management.

**Screens:**
1.0 Main Dashboard
2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent wants to add funds to the youth account.

#### Workflow Variation A: From Dashboard Quick Action
- Youth Account Dashboard → Click 'Add Funds' → Enter amount → Select source account → Confirm → Success/Error

#### Workflow Variation B: From Account Management Menu
- Youth Account Dashboard → Open 'Manage Funds' menu → Select 'Transfer to Youth' → Enter details → Confirm → Success/Error

**User Goal:** Seamlessly transfer funds to youth account.
**Business Goal:** Encourage responsible, trackable fund allocation.

**Screens:**
2.0 Youth Account Dashboard
3.0 Fund Transfer Initiation
3.1 Fund Transfer Confirmation
Er.1 Insufficient Balance Error
3.2 Fund Transfer Success

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to control weekly spending for the youth account.

#### Workflow Variation A: Inline Limit Setting
- Youth Account Dashboard → 'Set/Change Spending Limit' inline control → Enter value → Save → Confirmation

#### Workflow Variation B: Dedicated Limit Management Page
- Youth Account Dashboard → 'Manage Spending Limits' → Separate page/modal → Enter/edit value → Save → Confirmation

**User Goal:** Easily set or adjust spending limits.
**Business Goal:** Promote financial discipline and parental oversight.

**Screens:**
2.0 Youth Account Dashboard
4.0 Spending Limit Configuration
4.1 Spending Limit Confirmation
Er.2 Invalid Limit Value Error

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to monitor transactions and spending patterns.

#### Workflow Variation A: Dashboard Transaction List
- Youth Account Dashboard → Scroll to 'Recent Activity' → View/filter transactions

#### Workflow Variation B: Detailed Activity Page
- Youth Account Dashboard → Click 'View All Activity' → Dedicated transaction history page with filters

**User Goal:** Understand youth spending behavior at a glance or in detail.
**Business Goal:** Provide transparency and build trust in the platform.

**Screens:**
2.0 Youth Account Dashboard
5.0 Transaction History (with filters)

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more than available in their own account.

#### Workflow Variation A: Inline Error
- Fund Transfer → Enter amount → System detects insufficient funds → Inline error message, disables confirmation

#### Workflow Variation B: Post-Submission Error Modal
- Fund Transfer → Enter amount → Attempt transfer → Error modal appears explaining insufficient funds, with options to retry or cancel

**User Goal:** Clearly understand why a transfer failed and how to resolve it.
**Business Goal:** Reduce failed transactions and support self-service troubleshooting.

**Screens:**
3.1 Fund Transfer Confirmation
Er.1 Insufficient Balance Error

---

## Minimum Viable Experience (MVE)
- Parent can access youth dashboard, view balance and recent activity, allocate funds, set spending limits, and see clear errors for failed actions.

---

## Detailed Screen List & Documentation

### 1.0 Main Dashboard
- **Goal:** Provide entry point to all parent-managed accounts.
- **Description:** Overview of all linked accounts, notifications, and quick links (including 'Youth Accounts').
- **Design Problems:**
  - HMW make youth account access prominent without clutter?
  - HMW surface important notifications efficiently?
- **Design Opportunities:**
  - What if the dashboard adapts to show most-used actions?
  - What if notifications are personalized?

### 2.0 Youth Account Dashboard
- **Goal:** Central hub for youth account management.
- **Description:** Shows youth account balance, recent activity, quick actions (add funds, set limits), and summary widgets.
- **Design Problems:**
  - HMW balance information density with clarity?
  - HMW make 'Add Funds' and 'Set Limit' actions obvious but not overwhelming?
- **Design Opportunities:**
  - What if the dashboard visualizes spending trends?
  - What if parents get proactive suggestions (e.g., 'Consider raising limit for summer')?

### 3.0 Fund Transfer Initiation
- **Goal:** Initiate transfer from parent to youth account.
- **Description:** Form for selecting source account, entering amount, and viewing available balance.
- **Design Problems:**
  - HMW prevent errors before submission?
  - HMW reassure users about transfer security?
- **Design Opportunities:**
  - What if the system suggests typical transfer amounts?
  - What if parents can schedule recurring transfers?

### 3.1 Fund Transfer Confirmation
- **Goal:** Confirm transfer details before execution.
- **Description:** Summary of entered details, with clear confirm/cancel options.
- **Design Problems:**
  - HMW prevent accidental transfers?
- **Design Opportunities:**
  - What if confirmation includes a reminder of spending limits?

### 3.2 Fund Transfer Success
- **Goal:** Notify parent of successful transfer.
- **Description:** Success message, updated balances, and option to return to dashboard or set a spending limit.
- **Design Problems:**
  - HMW reinforce positive actions?
- **Design Opportunities:**
  - What if success screens offer tips for teaching kids about money?

### Er.1 Insufficient Balance Error
- **Goal:** Clearly communicate insufficient funds.
- **Description:** Inline or modal error with guidance (e.g., 'Your account balance is $X, please enter a lower amount or fund your account').
- **Design Problems:**
  - HMW reduce frustration when errors occur?
- **Design Opportunities:**
  - What if the error screen links to funding options?

### 4.0 Spending Limit Configuration
- **Goal:** Allow parent to set or edit weekly spending limits.
- **Description:** Input for limit value, explanation of how limits work, and current active limit display.
- **Design Problems:**
  - HMW make limits understandable and actionable?
- **Design Opportunities:**
  - What if parents get recommendations based on past spending?

### 4.1 Spending Limit Confirmation
- **Goal:** Confirm new/edited spending limit.
- **Description:** Confirmation message and updated dashboard display.
- **Design Problems:**
  - HMW reassure parents that limits are active?
- **Design Opportunities:**
  - What if confirmation includes an option to notify the youth?

### Er.2 Invalid Limit Value Error
- **Goal:** Prevent and explain invalid limit entries.
- **Description:** Inline error for non-numeric, negative, or excessively high values.
- **Design Problems:**
  - HMW prevent accidental misconfiguration?
- **Design Opportunities:**
  - What if the UI suggests reasonable limits?

### 5.0 Transaction History (with filters)
- **Goal:** Provide detailed view of youth spending.
- **Description:** List of transactions with date, merchant, amount, remaining balance, and filters for time period/type.
- **Design Problems:**
  - HMW make large lists scannable?
  - HMW support both overview and detail?
- **Design Opportunities:**
  - What if parents can flag or comment on transactions?
  - What if spending is categorized automatically?

---

## Sequence of Screens (Example Workflows)

### Workflow 1: Allocate Funds (Direct)
1.0 Main Dashboard → 2.0 Youth Account Dashboard → 3.0 Fund Transfer Initiation → 3.1 Fund Transfer Confirmation → 3.2 Fund Transfer Success

### Workflow 2: Allocate Funds (Insufficient Balance)
1.0 Main Dashboard → 2.0 Youth Account Dashboard → 3.0 Fund Transfer Initiation → 3.1 Fund Transfer Confirmation → Er.1 Insufficient Balance Error

### Workflow 3: Set Spending Limit (Inline)
1.0 Main Dashboard → 2.0 Youth Account Dashboard → 4.0 Spending Limit Configuration → 4.1 Spending Limit Confirmation

### Workflow 4: View Activity (Dashboard)
1.0 Main Dashboard → 2.0 Youth Account Dashboard → 5.0 Transaction History

### Workflow 5: Access via Notification
1.0 Main Dashboard → Notification → 2.0 Youth Account Dashboard

---

## Accessibility & Scalability Considerations
- All actions are accessible via keyboard and screen reader.
- Error messages are clear, persistent, and actionable.
- Layouts adapt for desktop and tablet.
- All data visualizations have text alternatives.
- Workflows support future features (e.g., multiple youth accounts, recurring transfers).

---

## Summary Table: Scenarios & Variations
| Scenario | Variation A | Variation B |
|----------|-------------|-------------|
| Access Youth Dashboard | Direct Navigation | Notification-Driven |
| Allocate Funds | Dashboard Quick Action | Account Management Menu |
| Set Spending Limit | Inline Control | Dedicated Page/Modal |
| View Activity | Dashboard List | Detailed Activity Page |
| Handle Insufficient Balance | Inline Error | Post-Submission Modal |

---

## End of User Workflow Journey Documentation
