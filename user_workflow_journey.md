# UX Workflow Documentation: Parent Fund Management for Youth Account

## Overview
This document details user-centered workflow designs for the experience of parents allocating and managing funds for a youth account. It covers all possible scenarios, workflow variations, user and business goals, screen flows, design problems, and opportunities, ensuring accessibility and scalability.

---

## Experience Mindset
**Primary User:** Parent/Guardian
**Experience:** Managing a child's youth account (fund allocation, spending limits, activity monitoring)

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application.
**Action:** Navigates to the youth account section.
**Goal:** Quickly view youth account overview (balance, recent activity).

#### Workflow Variation 1A: Direct Navigation
- Parent selects "Youth Accounts" from main dashboard menu.
- System loads youth account dashboard directly.

#### Workflow Variation 1B: Notification Shortcut
- Parent receives notification about youth account activity.
- Clicks notification, which deep-links to youth account dashboard.

**User Goal:** Instantly access youth account status and actions.
**Business Goal:** Increase engagement with youth account features.

**Screens:**
1.0 Main Dashboard
  - Goal: Central hub for all parent accounts and actions.
  - Description: Lists all accounts, notifications, and quick links.
  - Design Problems: HMW make youth account access prominent without cluttering the dashboard?
  - Opportunities: What if the dashboard adapts based on recent activity?

2.0 Youth Account Dashboard
  - Goal: Provide a comprehensive overview of youth account status.
  - Description: Shows balance, recent transactions, spending limit, and quick actions.
  - Design Problems: HMW surface the most important info for quick scanning?
  - Opportunities: What if parents could customize the dashboard widgets?

**Screen Sequence:** 1.0 Main Dashboard → 2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent is on youth account dashboard.
**Action:** Selects "Add Funds" to transfer money from primary account.
**Goal:** Seamlessly transfer funds with clear feedback and error handling.

#### Workflow Variation 2A: Modal Transfer
- Parent clicks "Add Funds"; modal pops up for transfer details.
- Parent selects source account, enters amount, confirms.
- Success or error message shown in modal.

#### Workflow Variation 2B: Dedicated Transfer Page
- Parent clicks "Add Funds"; navigates to a dedicated transfer page.
- Parent completes transfer steps with more guidance and details.
- Redirected back to dashboard after success.

**User Goal:** Move funds to youth account quickly and confidently.
**Business Goal:** Encourage regular use of youth account funding.

**Screens:**
2.0 Youth Account Dashboard
  - Goal: Entry point for all youth account actions.

Pu.1 Add Funds Modal (Variation 2A)
  - Goal: Enable quick, focused fund transfer.
  - Description: Source selector, amount input, confirm/cancel, validation.
  - Design Problems: HMW prevent accidental transfers?
  - Opportunities: What if the modal suggested typical transfer amounts?

3.0 Add Funds Page (Variation 2B)
  - Goal: Provide a detailed, accessible fund transfer flow.
  - Description: Step-by-step guidance, contextual help, summary before confirm.
  - Design Problems: HMW balance guidance with speed?
  - Opportunities: What if the page offered financial tips for parents?

Pu.2 Success Message
  - Goal: Confirm completion and reinforce positive action.

Er.1 Insufficient Balance Error
  - Goal: Clearly communicate why transfer failed and what to do next.

**Screen Sequences:**
- 2.0 → Pu.1 → Pu.2/Er.1 (Modal)
- 2.0 → 3.0 → Pu.2/Er.1 → 2.0 (Page)

---

### Scenario 3: Set Spending Limit
**Context:** Parent is in youth account management section.
**Action:** Configures or edits weekly spending limit.
**Goal:** Easily set and understand spending controls.

#### Workflow Variation 3A: Inline Editing
- Parent clicks "Edit" next to spending limit on dashboard.
- Inline input appears for new limit; parent saves or cancels.

#### Workflow Variation 3B: Dedicated Limit Management Page
- Parent selects "Manage Limits"; navigates to a full page for configuring limits, with explanations and history.

**User Goal:** Set clear boundaries for child’s spending.
**Business Goal:** Promote responsible youth spending and parental control.

**Screens:**
2.0 Youth Account Dashboard
  - Goal: Show current limit and entry to limit management.

4.0 Inline Limit Editor (Variation 3A)
  - Goal: Fast, low-friction editing of spending limit.
  - Description: Input field replaces display, with save/cancel.
  - Design Problems: HMW prevent invalid values?
  - Opportunities: What if the UI suggested age-appropriate limits?

5.0 Limit Management Page (Variation 3B)
  - Goal: Provide context, guidance, and history for spending limits.
  - Description: Current/previous limits, input, help text, FAQs.
  - Design Problems: HMW explain limits to less tech-savvy users?
  - Opportunities: What if parents could set limits by category (e.g., food, entertainment)?

Pu.3 Success Message
  - Goal: Confirm limit update.

Er.2 Invalid Limit Error
  - Goal: Prevent and explain invalid input (e.g., negative values).

**Screen Sequences:**
- 2.0 → 4.0 → Pu.3/Er.2 (Inline)
- 2.0 → 5.0 → Pu.3/Er.2 → 2.0 (Page)

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent is on youth account dashboard.
**Action:** Selects activity section to review transactions.
**Goal:** Understand child’s spending patterns and details.

#### Workflow Variation 4A: Embedded Activity List
- Recent transactions displayed on dashboard with filter options.
- Parent can expand/collapse for more detail.

#### Workflow Variation 4B: Full Activity Page
- Parent clicks "View All Activity"; navigates to a dedicated page with advanced filters and export options.

**User Goal:** Gain insight into youth spending habits.
**Business Goal:** Increase transparency and trust in youth account.

**Screens:**
2.0 Youth Account Dashboard
  - Goal: Show summary of recent activity.

6.0 Activity List (Variation 4A)
  - Goal: Quick scan of recent transactions.
  - Description: Date, merchant, amount, remaining balance, filter by time.
  - Design Problems: HMW make patterns visible at a glance?
  - Opportunities: What if system highlighted unusual spending?

7.0 Full Activity Page (Variation 4B)
  - Goal: Deep dive into transaction history.
  - Description: Advanced filters, export, search, visual summaries.
  - Design Problems: HMW support accessibility for large data sets?
  - Opportunities: What if parents could set up alerts for specific merchants?

**Screen Sequences:**
- 2.0 → 6.0 (Embedded)
- 2.0 → 7.0 (Full Page)

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent attempts to transfer funds, but selected account lacks sufficient balance.
**Action:** System blocks transfer and shows error.
**Goal:** Prevent failed transactions and provide clear guidance.

#### Workflow Variation 5A: Inline Error on Amount Input
- As parent enters amount, system checks balance and shows error inline if insufficient.

#### Workflow Variation 5B: Error on Confirmation
- Parent completes all steps, error shown after confirm, with suggestions to resolve.

**User Goal:** Avoid confusion and wasted effort when transferring funds.
**Business Goal:** Reduce failed transactions and support user success.

**Screens:**
Pu.4 Inline Insufficient Funds Error (Variation 5A)
  - Goal: Prevent error before submission.
  - Description: Inline message, disables confirm button.
  - Design Problems: HMW make error messages actionable?
  - Opportunities: What if system suggested alternate funding sources?

Er.3 Post-Confirmation Error (Variation 5B)
  - Goal: Explain failure and next steps.
  - Description: Error page/modal with retry/cancel options.
  - Design Problems: HMW reduce frustration after failed actions?
  - Opportunities: What if system offered to schedule transfer when funds are available?

**Screen Sequences:**
- 3.0 → Pu.4 (Inline)
- 3.0 → Er.3 (Post-Confirmation)

---

## Minimum Viable Experience (MVE)
- Parent logs in → Navigates to Youth Account Dashboard → Views balance/transactions → Adds funds (with validation) → Sets spending limit → Reviews activity

---

## Accessibility & Scalability Considerations
- All screens support keyboard navigation and screen readers.
- Responsive layouts for desktop and tablet.
- Error states use clear, descriptive language.
- Workflows designed to support future features (e.g., multiple youth accounts, advanced spending controls).

---

## Summary of Screen Sequences by Scenario
1. Access Dashboard: 1.0 → 2.0
2. Allocate Funds: 2.0 → Pu.1/3.0 → Pu.2/Er.1
3. Set Spending Limit: 2.0 → 4.0/5.0 → Pu.3/Er.2
4. View Activity: 2.0 → 6.0/7.0
5. Handle Insufficient Balance: 3.0 → Pu.4/Er.3

---

## End of Document
