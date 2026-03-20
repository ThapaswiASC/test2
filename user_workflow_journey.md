# UX Workflow Documentation: Parent Fund Management for Youth Account

## Experience Overview

**Story:** Parent can allocate and manage funds for a youth account  
**Business Goal:** As a parent or guardian, I want to allocate and manage funds for my child’s youth account so that I can teach financial responsibility while maintaining visibility and control over spending.

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application and wants to manage their child’s youth account.

#### Workflow Variation 1: Direct Navigation
- Parent logs in and selects "Youth Accounts" from the main dashboard.
- Youth account dashboard loads with balance, recent activity, and quick actions.

#### Workflow Variation 2: Notification-Driven Access
- Parent receives a notification (e.g., email, in-app) about recent youth account activity.
- Parent clicks the notification, which deep-links to the youth account dashboard.

**User Goal:** Quickly and easily access the youth account overview.
**Business Goal:** Increase engagement and awareness of youth account features.

**Screens:**
- **1.0 Main Dashboard**
  - *Goal:* Provide entry point to youth account management.
  - *Description:* Shows parent’s accounts, highlights youth account section.
  - *Design Problems:* HMW make youth account management prominent but not overwhelming?
  - *Design Opportunities:* What if the dashboard adapts based on recent youth account activity?
- **2.0 Youth Account Dashboard**
  - *Goal:* Summarize youth account status and actions.
  - *Description:* Displays balance, recent transactions, spending limit, and quick actions.
  - *Design Problems:* HMW ensure parents can quickly grasp account status?
  - *Design Opportunities:* What if we use visual cues for spending trends?

**Screen Sequence:** 1.0 Main Dashboard → 2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent wants to add money to the youth account.

#### Workflow Variation 1: Inline Transfer
- From youth account dashboard, parent clicks "Add Funds".
- Modal appears for transfer details (source account, amount).
- Confirmation and success message.

#### Workflow Variation 2: Stepper Flow
- Parent selects "Add Funds".
- Guided stepper: select source, enter amount, review, confirm.

**User Goal:** Seamlessly transfer funds with confidence.
**Business Goal:** Encourage regular funding and reinforce parental control.

**Screens:**
- **2.1 Add Funds Modal (Pu.1)**
  - *Goal:* Enable quick fund transfer.
  - *Description:* Modal overlays dashboard, with account selector and amount input.
  - *Design Problems:* HMW prevent errors and accidental transfers?
  - *Design Opportunities:* What if we suggest typical transfer amounts?
- **2.2 Add Funds Stepper (3.0, 3.1, 3.2)**
  - *Goal:* Guide parent through safe, clear transfer process.
  - *Description:* Multi-step form with validation and review.
  - *Design Problems:* HMW reduce friction without losing clarity?
  - *Design Opportunities:* What if we show projected youth balance after transfer?
- **Er.1 Insufficient Balance Error**
  - *Goal:* Clearly communicate transfer issues.
  - *Description:* Error message if parent’s account lacks funds.
  - *Design Problems:* HMW help parents resolve insufficient funds quickly?
  - *Design Opportunities:* What if we offer to set up a funding reminder?

**Screen Sequence:** 2.0 Youth Account Dashboard → 2.1 Add Funds Modal (or 3.0 Stepper) → Er.1 (if error)

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to control how much their child can spend weekly.

#### Workflow Variation 1: Inline Limit Edit
- Parent sees current limit on dashboard.
- Clicks "Edit", updates value inline, saves.

#### Workflow Variation 2: Dedicated Limit Management Screen
- Parent clicks "Manage Limits".
- Navigates to a full page with limit history, guidance, and edit options.

**User Goal:** Easily set and understand spending boundaries.
**Business Goal:** Empower parents, reduce overspending incidents.

**Screens:**
- **4.0 Spending Limit Display/Edit**
  - *Goal:* Make limit visible and editable.
  - *Description:* Inline edit on dashboard or in modal.
  - *Design Problems:* HMW prevent invalid or unrealistic limits?
  - *Design Opportunities:* What if we recommend limits based on age or past spending?
- **5.0 Limit Management Page**
  - *Goal:* Provide comprehensive limit controls.
  - *Description:* Shows current, past limits, and educational tips.
  - *Design Problems:* HMW explain limits without jargon?
  - *Design Opportunities:* What if we visualize spending vs. limits?
- **Pu.2 Confirmation Pop-Up**
  - *Goal:* Confirm changes to limits.
  - *Description:* Modal for parent to review before saving.

**Screen Sequence:** 2.0 Youth Account Dashboard → 4.0 Inline Edit or 5.0 Limit Management → Pu.2 Confirmation

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review how their child is using funds.

#### Workflow Variation 1: Embedded Transaction List
- Recent transactions shown directly on dashboard.
- Parent can filter by date or category.

#### Workflow Variation 2: Full Activity Page
- Parent clicks "View All Activity".
- Navigates to a dedicated transaction history page with advanced filters.

**User Goal:** Quickly understand youth spending patterns.
**Business Goal:** Increase transparency and foster financial education.

**Screens:**
- **6.0 Transaction List (Dashboard)**
  - *Goal:* Provide snapshot of recent activity.
  - *Description:* List with date, merchant, amount, balance.
  - *Design Problems:* HMW make data scannable and accessible?
  - *Design Opportunities:* What if we highlight unusual spending?
- **7.0 Full Activity Page**
  - *Goal:* Enable deep dive into spending history.
  - *Description:* Advanced filters, export options, and visual summaries.
  - *Design Problems:* HMW support accessibility for all parents?
  - *Design Opportunities:* What if we offer insights or tips based on spending?

**Screen Sequence:** 2.0 Youth Account Dashboard → 6.0 Transaction List or 7.0 Full Activity Page

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more than their available balance.

#### Workflow Variation 1: Inline Error Messaging
- Error appears under amount input in modal/stepper.

#### Workflow Variation 2: Dedicated Error Screen
- After failed attempt, parent is redirected to an error page with solutions (e.g., link to deposit funds).

**User Goal:** Understand and resolve funding issues without frustration.
**Business Goal:** Reduce failed transactions, encourage account funding.

**Screens:**
- **Er.1 Inline Error**
  - *Goal:* Immediate feedback on input.
  - *Description:* Red text under amount field, with guidance.
  - *Design Problems:* HMW ensure error is noticed and understood?
  - *Design Opportunities:* What if we offer quick actions to resolve?
- **Er.2 Error Resolution Page**
  - *Goal:* Guide parent to next steps.
  - *Description:* Explains issue, offers links to fund parent account or adjust amount.
  - *Design Problems:* HMW avoid user frustration?
  - *Design Opportunities:* What if we provide a chatbot for help?

**Screen Sequence:** 2.1 Add Funds Modal/3.1 Stepper → Er.1 Inline Error or Er.2 Error Page

---

## Minimum Viable Experience (MVE)

**Scenario:** Parent logs in, views youth account dashboard, adds funds, sets a spending limit, and reviews recent transactions.

**User Goal:** Manage youth account efficiently and confidently.
**Business Goal:** Drive adoption of youth account features, build trust, and foster financial literacy.

**MVE Screen Sequence:**
1.0 Main Dashboard → 2.0 Youth Account Dashboard → 2.1 Add Funds Modal → 4.0 Spending Limit Display/Edit → 6.0 Transaction List

---

## Accessibility & Scalability Considerations
- All screens use high-contrast, readable fonts and support keyboard navigation.
- Transaction lists and forms are screen-reader friendly.
- Responsive layouts for desktop and tablet.
- Error messages use clear language and visual cues.
- Workflows support future features (e.g., multiple youth accounts, advanced analytics).

---

## Summary Table of Screens
| Screen # | Title                        | Goal                                  |
|----------|------------------------------|---------------------------------------|
| 1.0      | Main Dashboard               | Entry point to youth management       |
| 2.0      | Youth Account Dashboard      | Overview, quick actions               |
| 2.1      | Add Funds Modal              | Transfer funds quickly                |
| 3.0-3.2  | Add Funds Stepper            | Guided transfer flow                  |
| 4.0      | Spending Limit Display/Edit  | Set/edit spending limits              |
| 5.0      | Limit Management Page        | Advanced limit controls               |
| 6.0      | Transaction List             | Recent youth spending                 |
| 7.0      | Full Activity Page           | Detailed transaction history          |
| Pu.1     | Add Funds Pop-Up             | Confirm fund transfer                 |
| Pu.2     | Limit Change Confirmation    | Confirm limit update                  |
| Er.1     | Inline Error                 | Immediate feedback on issues          |
| Er.2     | Error Resolution Page        | Guide to resolve funding errors       |

---

## End-to-End Workflow Sequences (for each scenario)

**Scenario 1:** 1.0 → 2.0  
**Scenario 2:** 2.0 → 2.1 (or 3.0-3.2) → Pu.1 → Er.1/Er.2 (if error)  
**Scenario 3:** 2.0 → 4.0 (or 5.0) → Pu.2  
**Scenario 4:** 2.0 → 6.0 (or 7.0)  
**Scenario 5:** 2.1/3.1 → Er.1/Er.2  

---

*This document is designed to balance user needs, business objectives, accessibility, and scalability for the parent-youth account fund management experience.*
