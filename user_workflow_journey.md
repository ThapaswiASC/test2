# UX User Workflow Documentation: Parent Fund Management for Youth Account

## Experience Mindset

**Primary User:** Parent/Guardian

**Experience:** Managing Youth Account Funds (Awareness, Onboarding, Account Management, Fund Allocation, Spending Control, Monitoring, Troubleshooting)

---

## Scenarios & Workflow Design Variations

### Scenario 1: Access Youth Account Dashboard

**Context:** Parent is logged into the banking web application and wants to view/manage their child's youth account.

#### Workflow Variation 1A: Direct Navigation from Main Dashboard
- Parent logs in → Selects 'Youth Account' from main dashboard → Youth account dashboard loads

#### Workflow Variation 1B: Search-Based Navigation
- Parent logs in → Uses global search to find 'Youth Account' → Selects youth account from results → Youth account dashboard loads

**User Goal:** Quickly access youth account overview and controls.
**Business Goal:** Increase engagement and transparency for parental controls.

**Screens:**
1.0 Main Dashboard
- **Goal:** Entry point for all account actions
- **Description:** Lists all linked accounts, including youth accounts. Prominent navigation to youth account section.
- **Design Problems:**
  - HMW make youth account access prominent without cluttering the dashboard?
  - HMW support parents with multiple children/youth accounts?
- **Design Opportunities:**
  - What if the dashboard highlights important youth account alerts?

2.0 Youth Account Dashboard
- **Goal:** Provide a comprehensive overview of youth account status
- **Description:** Shows balance, recent activity, spending limit, quick actions (Add Funds, Set Limit)
- **Design Problems:**
  - HMW present critical info at a glance?
  - HMW avoid overwhelming users with too much data?
- **Design Opportunities:**
  - What if parents could customize dashboard widgets?

**Screen Sequence:** 1.0 Main Dashboard → 2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account

**Context:** Parent wants to add money to the youth account.

#### Workflow Variation 2A: Inline Modal Transfer
- From Youth Account Dashboard, parent clicks 'Add Funds' → Modal opens → Parent selects source account, enters amount → Confirms transfer → Success message

#### Workflow Variation 2B: Dedicated Transfer Page
- From Youth Account Dashboard, parent clicks 'Add Funds' → Redirected to transfer page → Parent selects source, enters amount → Reviews and confirms → Success message

**User Goal:** Seamlessly transfer funds with confidence and minimal steps.
**Business Goal:** Encourage regular funding and reinforce parental control.

**Screens:**
2.0 Youth Account Dashboard (as above)
3.0 Fund Transfer Modal/Page
- **Goal:** Facilitate secure and intuitive fund transfer
- **Description:** Source account selector, amount input, transfer button, validation for limits and balance
- **Design Problems:**
  - HMW prevent transfer errors (e.g., insufficient funds)?
  - HMW minimize cognitive load during transfer?
- **Design Opportunities:**
  - What if the system suggests typical transfer amounts based on history?

Pu.1 Transfer Confirmation (Modal/Popup)
- **Goal:** Confirm intent and prevent mistakes
- **Description:** Summarizes transfer details, requires explicit confirmation
- **Design Problems:**
  - HMW avoid accidental transfers?
- **Design Opportunities:**
  - What if parents could schedule recurring transfers?

Er.1 Insufficient Balance Error
- **Goal:** Clearly communicate transfer failure due to low funds
- **Description:** Error message with actionable advice (e.g., link to add funds to parent account)
- **Design Problems:**
  - HMW reduce frustration when transfer fails?
- **Design Opportunities:**
  - What if the system offers alternate funding sources?

**Screen Sequence (2A):** 2.0 Youth Account Dashboard → Pu.1 Transfer Modal → Pu.1 Confirmation → Success/Er.1 Error
**Screen Sequence (2B):** 2.0 Youth Account Dashboard → 3.0 Transfer Page → Pu.1 Confirmation → Success/Er.1 Error

---

### Scenario 3: Set Spending Limit

**Context:** Parent wants to control youth spending by setting a weekly limit.

#### Workflow Variation 3A: Inline Editing on Dashboard
- Parent clicks 'Edit' next to spending limit on dashboard → Inline input appears → Parent enters new limit → Saves → Confirmation

#### Workflow Variation 3B: Dedicated Limit Management Page
- Parent clicks 'Manage Spending Limit' → Navigates to a dedicated page → Sets/edits limit → Saves → Confirmation

**User Goal:** Easily set and adjust spending controls for youth.
**Business Goal:** Promote responsible youth spending and parental peace of mind.

**Screens:**
2.0 Youth Account Dashboard (as above)
4.0 Spending Limit Edit (Inline or Page)
- **Goal:** Enable clear, error-proof limit configuration
- **Description:** Input for weekly limit, contextual help, validation for numeric/allowed ranges
- **Design Problems:**
  - HMW explain the impact of limits?
  - HMW prevent invalid or extreme values?
- **Design Opportunities:**
  - What if the UI visualizes spending trends vs. limits?

Pu.2 Limit Change Confirmation
- **Goal:** Confirm and reinforce new limit
- **Description:** Modal summarizing new value, with undo option
- **Design Problems:**
  - HMW reassure parents about changes?
- **Design Opportunities:**
  - What if parents could set temporary limits for special occasions?

Er.2 Invalid Limit Error
- **Goal:** Prevent and explain invalid input
- **Description:** Error message for non-numeric, negative, or excessive values
- **Design Problems:**
  - HMW guide users to correct errors quickly?

**Screen Sequence (3A):** 2.0 Youth Account Dashboard → 4.0 Inline Edit → Pu.2 Confirmation/Er.2 Error
**Screen Sequence (3B):** 2.0 Youth Account Dashboard → 4.0 Limit Page → Pu.2 Confirmation/Er.2 Error

---

### Scenario 4: View Youth Spending Activity

**Context:** Parent wants to monitor youth spending patterns and details.

#### Workflow Variation 4A: Embedded Activity List
- Youth Account Dashboard displays recent transactions inline, with filter controls

#### Workflow Variation 4B: Full-Screen Activity View
- Parent clicks 'View All Activity' → Navigates to full transaction history page with advanced filters

**User Goal:** Quickly scan and understand youth spending.
**Business Goal:** Increase transparency and trust in youth account feature.

**Screens:**
2.0 Youth Account Dashboard (as above)
5.0 Activity List/History
- **Goal:** Present transaction data in a scannable, filterable format
- **Description:** List with date, merchant, amount, remaining balance; filters for time period and categories
- **Design Problems:**
  - HMW make large lists easy to scan?
  - HMW support accessibility for screen readers?
- **Design Opportunities:**
  - What if parents could flag suspicious transactions?
  - What if spending insights were visualized?

**Screen Sequence (4A):** 2.0 Youth Account Dashboard (embedded list)
**Screen Sequence (4B):** 2.0 Youth Account Dashboard → 5.0 Full Activity Page

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation

**Context:** Parent tries to transfer funds but their account lacks sufficient balance.

#### Workflow Variation 5A: Pre-Validation on Amount Entry
- System checks available balance as parent enters amount; disables transfer if insufficient

#### Workflow Variation 5B: Post-Submission Error Handling
- Parent submits transfer; system checks and displays error if insufficient

**User Goal:** Understand and resolve transfer failures without frustration.
**Business Goal:** Reduce failed transactions and support successful fund allocations.

**Screens:**
3.0 Fund Transfer Modal/Page (as above)
Er.1 Insufficient Balance Error (as above)
- **Goal:** Provide clear, actionable feedback
- **Description:** Error message with options (e.g., retry, choose different account, link to add funds)
- **Design Problems:**
  - HMW reduce friction in error recovery?
- **Design Opportunities:**
  - What if the system offered instant funding options?

**Screen Sequence (5A):** 3.0 Fund Transfer Modal → Inline validation/disable
**Screen Sequence (5B):** 3.0 Fund Transfer Modal → Er.1 Error

---

## Summary of All Unique Screens

1.0 Main Dashboard
2.0 Youth Account Dashboard
3.0 Fund Transfer Modal/Page
4.0 Spending Limit Edit (Inline/Page)
5.0 Activity List/History
Pu.1 Transfer Confirmation
Pu.2 Limit Change Confirmation
Er.1 Insufficient Balance Error
Er.2 Invalid Limit Error

---

## Accessibility & Scalability Considerations
- All screens must support keyboard navigation and screen readers
- Color contrast and text size must meet WCAG 2.1 AA
- Responsive layouts for desktop, tablet, and mobile
- Error messages must be programmatically associated with inputs
- Workflows must support multiple youth accounts per parent
- Transaction and limit data should be paginated and filterable for scalability

---

## Edge Cases & Additional Use Cases
- Parent with multiple youth accounts: Dashboard lists all; workflows support switching
- Youth account with no activity: Show empty states with guidance
- Attempt to set limit lower than current balance: Warn and explain
- Parent cancels transfer or limit change: No changes applied, return to previous state
- Network error during fund transfer: Show retry option and contact support link

---

## References (from Jira Story SCIB-25 & Subtasks)
- [SCIB-25] Parent can allocate and manage funds for a youth account
- [SCIB-194] Design fund transfer interaction for youth account
- [SCIB-195] Design youth account dashboard layout
- [SCIB-196] Design spending limit configuration interface
- [SCIB-197] Design youth account activity view
