# UX Design User Workflow Documentation: Parent Fund Management for Youth Account

## Experience: Parent Managing Youth Account

### User: Parent/Guardian

### Business Goal:
Enable parents/guardians to allocate and manage funds for a youth account, teaching financial responsibility while maintaining visibility and control over spending.

---

## Identified Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application and wants to view/manage the youth account.

#### Workflow Variation 1A: Direct Dashboard Access
- Parent logs in → Navigates to "Youth Account" from main dashboard → Youth Account Dashboard loads

#### Workflow Variation 1B: Notification-Driven Access
- Parent receives notification (e.g., spending alert) → Clicks notification → Lands directly on Youth Account Dashboard

**User Goal:** Quickly access youth account information and management tools.
**Business Goal:** Increase engagement and transparency for youth account features.

##### Screens:
1.0 Main Dashboard
  - **Goal:** Provide entry point to youth account features.
  - **Description:** Shows all accounts, highlights youth account section.
  - **Design Problems:** HMW make youth account prominent without cluttering?
  - **Design Opportunities:** What if youth account has a distinct color/icon?

2.0 Youth Account Dashboard
  - **Goal:** Summarize balance, recent activity, and quick actions.
  - **Description:** Shows current balance, recent transactions, spending limit, "Add Funds" and "Set Limit" actions.
  - **Design Problems:** HMW surface key info at a glance?
  - **Design Opportunities:** What if dashboard is customizable?

**Screen Sequence:** 1.0 Main Dashboard → 2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent wants to transfer money from their account to the youth account.

#### Workflow Variation 2A: From Dashboard Quick Action
- On Youth Account Dashboard, click "Add Funds" → Enter amount → Select source account → Confirm transfer → Success/Error message

#### Workflow Variation 2B: From Account Management Menu
- From main menu, select "Transfer Funds" → Choose youth account as recipient → Enter amount → Confirm transfer → Success/Error message

**User Goal:** Easily and securely transfer funds to youth account.
**Business Goal:** Encourage regular use of youth account and parental oversight.

##### Screens:
2.0 Youth Account Dashboard (entry point)

3.0 Fund Transfer Screen
  - **Goal:** Facilitate secure, simple fund transfer.
  - **Description:** Input amount, select source, see available balance, transfer button.
  - **Design Problems:** HMW prevent errors/accidental transfers?
  - **Design Opportunities:** What if there’s a transfer suggestion based on history?

3.1 Transfer Confirmation (sub-screen)
  - **Goal:** Prevent accidental transfers.
  - **Description:** Review details, confirm/cancel.
  - **Design Problems:** HMW balance speed and safety?
  - **Design Opportunities:** What if confirmation uses biometrics?

Pu.1 Success Pop-Up
  - **Goal:** Confirm successful transfer.
  - **Description:** Shows confirmation, updated balance, option to return to dashboard.

Er.1 Insufficient Balance Error
  - **Goal:** Prevent failed transfers, guide user.
  - **Description:** Error message with guidance to add funds or select another account.

**Screen Sequence:** 2.0 → 3.0 → 3.1 → (Pu.1 or Er.1)

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to configure or update a weekly spending limit for the youth account.

#### Workflow Variation 3A: Inline Limit Edit
- On dashboard, click "Edit" next to spending limit → Edit value inline → Save/cancel → Confirmation

#### Workflow Variation 3B: Dedicated Limit Management Screen
- Click "Manage Limit" → Go to separate screen → Enter new limit → Save → Confirmation

**User Goal:** Set and adjust spending limits for youth account.
**Business Goal:** Promote responsible spending and parental control.

##### Screens:
2.0 Youth Account Dashboard (entry point)

4.0 Spending Limit Edit (inline or dedicated)
  - **Goal:** Allow quick, clear limit setting.
  - **Description:** Input for weekly limit, contextual help, validation for values.
  - **Design Problems:** HMW explain limits simply?
  - **Design Opportunities:** What if system suggests limits based on age/spending?

Pu.2 Limit Saved Pop-Up
  - **Goal:** Confirm limit update.
  - **Description:** Shows new limit, option to return.

Er.2 Invalid Limit Error
  - **Goal:** Prevent invalid entries.
  - **Description:** Error for non-numeric/negative values, guidance for correction.

**Screen Sequence:** 2.0 → 4.0 → (Pu.2 or Er.2)

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review youth account transactions.

#### Workflow Variation 4A: Dashboard Recent Activity
- On dashboard, view recent transactions list (scrollable/expandable)

#### Workflow Variation 4B: Detailed Activity View
- Click "View All Activity" → Go to full transaction history with filters (date, amount, merchant)

**User Goal:** Monitor youth spending patterns and activity.
**Business Goal:** Build trust, transparency, and encourage financial learning.

##### Screens:
2.0 Youth Account Dashboard (entry point)

5.0 Activity List (inline or full page)
  - **Goal:** Make transactions easy to scan and analyze.
  - **Description:** List with date, merchant, amount, balance; filters for time period.
  - **Design Problems:** HMW highlight unusual activity?
  - **Design Opportunities:** What if system flags learning moments or trends?

**Screen Sequence:** 2.0 → 5.0

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more than available balance in source account.

#### Workflow Variation 5A: Pre-Validation
- On fund transfer screen, entering amount greater than available disables transfer button and shows inline error

#### Workflow Variation 5B: Post-Submission Error
- Parent submits transfer, system checks balance, shows error pop-up if insufficient

**User Goal:** Avoid failed transfers and confusion.
**Business Goal:** Reduce support queries, improve trust.

##### Screens:
3.0 Fund Transfer Screen (with pre-validation)

Er.1 Insufficient Balance Error (inline or pop-up)
  - **Goal:** Clearly communicate issue and next steps.
  - **Description:** Error message, guidance to reduce amount or add funds.
  - **Design Problems:** HMW prevent frustration?
  - **Design Opportunities:** What if system suggests alternative funding sources?

**Screen Sequence:** 3.0 → Er.1

---

## Edge Cases & Accessibility
- All workflows must be accessible (keyboard navigation, screen reader support, color contrast)
- Error states must be clear and actionable
- Flows should scale for desktop and tablet
- All actions must have confirmations and undo where possible

---

## Summary of Screen Sequences
- 1.0 Main Dashboard → 2.0 Youth Account Dashboard
- 2.0 → 3.0 Fund Transfer → 3.1 Confirm → Pu.1 Success/Er.1 Error
- 2.0 → 4.0 Limit Edit → Pu.2 Success/Er.2 Error
- 2.0 → 5.0 Activity List
- 3.0 → Er.1 (Insufficient Balance)

---

## Minimum Viable Experience
- Parent can view youth account dashboard (balance, recent activity, limits)
- Parent can allocate funds with validation and confirmation
- Parent can set and edit spending limits
- Parent can view detailed transaction history
- All errors are clearly communicated and actionable

---

## Design Problems & Opportunities (Consolidated)
- HMW make youth account management intuitive and stress-free?
- HMW ensure parents feel in control but not overwhelmed?
- What if the system proactively suggests financial lessons or tips?
- What if parents can set goals/rewards for youth spending behavior?

---

## End of Documentation
