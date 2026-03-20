# UX Design User Workflow Documentation: Parent Fund Management for Youth Account

## Overview
This document outlines systematic, user-centered workflow designs for the experience of parents allocating and managing funds for a youth account. It covers all possible scenarios, provides at least two workflow design variations per scenario, and details minimum viable experiences. Each workflow includes user and business goals, screen flows, design problems, and opportunities, ensuring accessibility and scalability.

---

## Experience: Parent Fund Management for Youth Account

### Key Scenarios
1. Access youth account dashboard
2. Allocate funds to youth account
3. Set spending limit
4. View youth spending activity
5. Handle insufficient balance during fund allocation

---

## Scenario 1: Access Youth Account Dashboard

**User Scenario:**
Jordan, a parent, logs into the banking web app to check their child’s spending and manage the youth account.

### Workflow Variation 1: Direct Navigation
- Jordan logs in
- Selects "Youth Accounts" from main menu
- Dashboard loads with balance, recent activity, and quick actions

### Workflow Variation 2: Dashboard Widget
- Jordan logs in
- Home dashboard displays youth account summary widget
- Clicks widget to expand full youth account dashboard

**User Goal:**
Quickly access youth account details and controls

**Business Goal:**
Increase engagement and parental oversight, driving trust and feature adoption

### Screens
**1.0 Login Page**
- Goal: Secure authentication
- Description: Standard login with accessibility features
- Design Problems:
  - HMW ensure secure yet frictionless login?
  - HMW support parents with disabilities?
- Opportunities:
  - What if biometric login was available?

**2.0 Main Dashboard**
- Goal: Overview of all accounts
- Description: Parent sees all accounts, including youth account widget
- Design Problems:
  - HMW make youth account status prominent but not overwhelming?
- Opportunities:
  - What if the widget showed spending alerts?

**3.0 Youth Account Dashboard**
- Goal: Central hub for youth account management
- Description: Shows balance, recent activity, quick actions (Add Funds, Set Limit)
- Design Problems:
  - HMW surface key actions without clutter?
- Opportunities:
  - What if parents could customize dashboard sections?

**Screen Sequence:**
1.0 Login Page → 2.0 Main Dashboard → 3.0 Youth Account Dashboard

---

## Scenario 2: Allocate Funds to Youth Account

**User Scenario:**
Jordan wants to transfer $50 from their primary account to their child’s youth account for weekly allowance.

### Workflow Variation 1: Quick Transfer from Dashboard
- On youth account dashboard, clicks "Add Funds"
- Enters amount, selects source account, confirms
- Sees success or error message

### Workflow Variation 2: Guided Transfer Flow
- Clicks "Transfer Funds" from main menu
- Chooses youth account as recipient
- Follows step-by-step wizard (amount, source, review, confirm)

**User Goal:**
Easily transfer funds with minimal steps and clear confirmation

**Business Goal:**
Promote regular use of fund transfer, reduce errors, and build trust

### Screens
**3.0 Youth Account Dashboard** (from above)

**4.0 Add Funds Modal (Pu.1)**
- Goal: Simple, accessible fund transfer
- Description: Modal with amount input, source selector, confirm button
- Design Problems:
  - HMW prevent mistakes in amount entry?
  - HMW ensure modal is accessible (keyboard, screen reader)?
- Opportunities:
  - What if there was a "repeat last transfer" shortcut?

**5.0 Transfer Confirmation (Pu.2)**
- Goal: Prevent accidental transfers
- Description: Review transfer details, confirm/cancel
- Design Problems:
  - HMW make confirmation clear but not annoying?
- Opportunities:
  - What if confirmation included educational tips about allowances?

**6.0 Success/Error State (Er.1/Er.2)**
- Goal: Communicate outcome
- Description: Success message with updated balance, or error (e.g., insufficient funds)
- Design Problems:
  - HMW make errors actionable and friendly?
- Opportunities:
  - What if errors offered instant help or links to resolve?

**Screen Sequence (Variation 1):**
3.0 Youth Account Dashboard → 4.0 Add Funds Modal → 5.0 Transfer Confirmation → 6.0 Success/Error State

**Screen Sequence (Variation 2):**
2.0 Main Dashboard → Transfer Funds Flow (step screens) → 5.0 Transfer Confirmation → 6.0 Success/Error State

---

## Scenario 3: Set Spending Limit

**User Scenario:**
Jordan wants to set a $20/week spending limit on their child’s account.

### Workflow Variation 1: Inline Limit Edit
- On youth account dashboard, clicks "Edit" next to spending limit
- Inline input appears, enters new value, saves

### Workflow Variation 2: Dedicated Limit Management Page
- Clicks "Manage Limits" from dashboard
- Navigates to full page with current/previous limits, guidance, and edit controls

**User Goal:**
Easily set and understand spending limits

**Business Goal:**
Encourage responsible youth spending and parental control

### Screens
**3.0 Youth Account Dashboard** (from above)

**7.0 Spending Limit Edit (Pu.3)**
- Goal: Quick limit adjustment
- Description: Inline or modal input for weekly limit, with validation
- Design Problems:
  - HMW prevent invalid values (e.g., negative, too high)?
- Opportunities:
  - What if guidance explained how limits teach responsibility?

**8.0 Limit Management Page (8.0)**
- Goal: Full control and history
- Description: Page with current limit, edit history, contextual guidance
- Design Problems:
  - HMW balance simplicity with advanced options?
- Opportunities:
  - What if parents could set temporary limits for special occasions?

**Screen Sequence (Variation 1):**
3.0 Youth Account Dashboard → 7.0 Spending Limit Edit

**Screen Sequence (Variation 2):**
3.0 Youth Account Dashboard → 8.0 Limit Management Page

---

## Scenario 4: View Youth Spending Activity

**User Scenario:**
Jordan wants to review their child’s recent transactions to discuss spending habits.

### Workflow Variation 1: Inline Activity List
- On dashboard, scrolls to recent activity section
- Filters by week/month

### Workflow Variation 2: Detailed Activity Page
- Clicks "View All Activity"
- Navigates to full transaction history with filters and search

**User Goal:**
Quickly scan and understand youth spending patterns

**Business Goal:**
Increase transparency, encourage financial education conversations

### Screens
**3.0 Youth Account Dashboard** (from above)

**9.0 Activity List (9.0)**
- Goal: Easy-to-scan transaction info
- Description: List with date, merchant, amount, remaining balance; filter controls
- Design Problems:
  - HMW make patterns visible at a glance?
- Opportunities:
  - What if parents could tag or comment on transactions?

**10.0 Detailed Activity Page (10.0)**
- Goal: In-depth review
- Description: Full-page list, advanced filters, export option
- Design Problems:
  - HMW support accessibility for large lists?
- Opportunities:
  - What if insights or tips surfaced based on spending trends?

**Screen Sequence (Variation 1):**
3.0 Youth Account Dashboard → 9.0 Activity List

**Screen Sequence (Variation 2):**
3.0 Youth Account Dashboard → 10.0 Detailed Activity Page

---

## Scenario 5: Handle Insufficient Balance During Fund Allocation

**User Scenario:**
Jordan tries to transfer $100, but their primary account only has $50.

### Workflow Variation 1: Inline Error on Amount Entry
- Enters $100, system immediately flags insufficient funds
- Suggests available amount or alternate funding source

### Workflow Variation 2: Error on Confirmation
- Proceeds to confirmation, error appears after submit
- Offers retry or cancel options

**User Goal:**
Understand why transfer failed and resolve quickly

**Business Goal:**
Reduce failed transactions, increase satisfaction

### Screens
**4.0 Add Funds Modal (from above)**

**6.0 Error State (Er.2)**
- Goal: Clear, actionable error
- Description: Message with reason, suggested actions (e.g., "Transfer up to $50" or "Add funds to primary account")
- Design Problems:
  - HMW avoid frustration and confusion?
- Opportunities:
  - What if the system offered instant transfer from another linked account?

**Screen Sequence (Variation 1):**
4.0 Add Funds Modal → 6.0 Error State

**Screen Sequence (Variation 2):**
4.0 Add Funds Modal → 5.0 Transfer Confirmation → 6.0 Error State

---

# Summary Table of All Screens
| Screen Number | Title                       | Goal                                   |
|---------------|----------------------------|----------------------------------------|
| 1.0           | Login Page                 | Secure authentication                  |
| 2.0           | Main Dashboard             | Overview of all accounts               |
| 3.0           | Youth Account Dashboard    | Central hub for youth account mgmt     |
| 4.0           | Add Funds Modal (Pu.1)     | Simple, accessible fund transfer       |
| 5.0           | Transfer Confirmation (Pu.2)| Prevent accidental transfers           |
| 6.0           | Success/Error State (Er.1/2)| Communicate outcome                    |
| 7.0           | Spending Limit Edit (Pu.3) | Quick limit adjustment                 |
| 8.0           | Limit Management Page      | Full control and history               |
| 9.0           | Activity List              | Easy-to-scan transaction info          |
| 10.0          | Detailed Activity Page     | In-depth review                        |

---

# Accessibility & Scalability Considerations
- All modals and forms are keyboard navigable and screen reader compatible
- Color contrast and font size meet WCAG 2.1 AA
- Responsive layouts for desktop and tablet
- Error messages are clear, actionable, and non-blocking
- Workflows support future features (e.g., multi-child accounts, advanced analytics)

---

# Edge Cases Considered
- Parent with multiple youth accounts
- Attempting transfer with insufficient funds
- Invalid spending limit values
- No recent activity to display
- Large transaction history (pagination, search)

---

# Example User Journey (Minimum Viable Experience)
1. Jordan logs in (1.0)
2. Sees youth account widget on main dashboard (2.0)
3. Clicks widget to open youth account dashboard (3.0)
4. Clicks "Add Funds" (4.0)
5. Enters $50, confirms (5.0)
6. Sees success message and updated balance (6.0)
7. Clicks "Set Limit," enters $20/week (7.0)
8. Scrolls to recent activity (9.0)

---

# Design Problems & Opportunities (Summary)
- HMW ensure all actions are accessible and error-proof?
- HMW surface key information without clutter?
- HMW encourage financial education through UI?
- What if parents could automate allowances?
- What if the dashboard adapted to usage patterns?

---

# Screen Sequences for Each Scenario
- Access Dashboard: 1.0 → 2.0 → 3.0
- Allocate Funds: 3.0 → 4.0 → 5.0 → 6.0
- Set Spending Limit: 3.0 → 7.0 or 8.0
- View Activity: 3.0 → 9.0 or 10.0
- Handle Insufficient Funds: 4.0 → 6.0

---

# End of UX Workflow Documentation
