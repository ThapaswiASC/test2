# UX Design User Workflow Documentation: Parent Fund Management for Youth Account

## Experience Mindset

**User:** Parent/Guardian
**Experience:** Allocating and managing funds for a youth account to teach financial responsibility, maintain visibility, and control spending.

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application.
**Action:** Navigates to youth account section.
**Goal:** Quickly view youth account balance and recent activity.

#### Workflow Variation 1: Direct Navigation
- Parent clicks "Youth Accounts" from main menu.
- Dashboard loads with balance, recent activity, and quick actions.

#### Workflow Variation 2: Notification-Driven Access
- Parent receives notification (e.g., spending alert).
- Clicks notification, lands directly on youth account dashboard.

**Minimum Viable Experience:**
- Parent can access dashboard from main menu or notification.

**User Goal:** Instantly view youth account status and activity.
**Business Goal:** Increase engagement and trust by providing transparency.

**Screens:**
1.0 Youth Account Dashboard

**Screen Details:**
- **Page Goal:** Communicate account status and enable quick actions.
- **Description:**
  - Shows balance, recent activity, spending limit, fund allocation, quick actions.
- **Design Problems:**
  - HMW make key information immediately visible?
  - HMW reduce cognitive load for parents?
- **Design Opportunities:**
  - What if dashboard adapts to highlight unusual activity?
  - What if dashboard offers tips for teaching financial responsibility?

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent is on youth account dashboard.
**Action:** Selects "Add Funds".
**Goal:** Transfer funds efficiently and securely.

#### Workflow Variation 1: Simple Transfer Flow
- Parent clicks "Add Funds".
- Enters amount, selects source account.
- Confirms transfer.
- Success message displayed.

#### Workflow Variation 2: Guided Transfer Flow
- Parent clicks "Add Funds".
- Guided wizard: select account, enter amount, review, confirm.
- Success message displayed.

**Minimum Viable Experience:**
- Parent can transfer funds with validation and confirmation.

**User Goal:** Easily allocate funds to youth account.
**Business Goal:** Promote parental control and encourage usage.

**Screens:**
1.0 Youth Account Dashboard -> 2.0 Fund Transfer Modal/Screen -> 2.1 Confirmation -> 2.2 Success Message

**Screen Details:**
- **2.0 Fund Transfer Modal/Screen**
  - **Page Goal:** Enable secure fund transfer.
  - **Description:**
    - Source account selector, amount input, validation.
    - Error state for insufficient funds.
  - **Design Problems:**
    - HMW prevent accidental transfers?
    - HMW communicate errors clearly?
  - **Design Opportunities:**
    - What if transfer is suggested based on spending trends?
    - What if parent can schedule recurring transfers?
- **2.1 Confirmation**
  - **Goal:** Prevent accidental transfers.
  - **Description:** Review details before confirming.
- **2.2 Success Message**
  - **Goal:** Confirm completion, offer next steps.

---

### Scenario 3: Set Spending Limit
**Context:** Parent is viewing youth account management section.
**Action:** Configures weekly spending limit.
**Goal:** Control youth spending and teach budgeting.

#### Workflow Variation 1: Inline Limit Editing
- Parent edits spending limit directly on dashboard.
- Confirmation and error handling for invalid values.

#### Workflow Variation 2: Dedicated Limit Management Screen
- Parent navigates to "Manage Limits".
- Sets/edit weekly limit, sees contextual guidance.
- Confirmation and error handling.

**Minimum Viable Experience:**
- Parent can set and modify spending limits with guidance.

**User Goal:** Easily set spending boundaries for youth.
**Business Goal:** Encourage responsible spending and parental oversight.

**Screens:**
1.0 Youth Account Dashboard -> 3.0 Limit Configuration Modal/Screen -> 3.1 Confirmation -> 3.2 Error State (if invalid)

**Screen Details:**
- **3.0 Limit Configuration Modal/Screen**
  - **Page Goal:** Configure spending limits.
  - **Description:**
    - Input for weekly limit, display current limit, guidance.
    - Error state for invalid values.
  - **Design Problems:**
    - HMW make limit configuration intuitive?
    - HMW prevent setting unrealistic limits?
  - **Design Opportunities:**
    - What if system suggests limits based on spending history?
    - What if parent can set alerts for approaching limits?

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent is viewing youth account dashboard.
**Action:** Selects activity section.
**Goal:** Monitor youth transactions and identify patterns.

#### Workflow Variation 1: Transaction List with Filters
- Parent views transaction list.
- Filters by date, category.
- Scans for patterns.

#### Workflow Variation 2: Visual Spending Insights
- Parent views graphical summary (charts, trends).
- Can drill down to transaction list.

**Minimum Viable Experience:**
- Parent can view and filter transaction history.

**User Goal:** Understand youth spending behavior.
**Business Goal:** Provide actionable insights, foster engagement.

**Screens:**
1.0 Youth Account Dashboard -> 4.0 Activity View -> 4.1 Filter/Insights

**Screen Details:**
- **4.0 Activity View**
  - **Page Goal:** Display transaction history.
  - **Description:**
    - List of transactions: date, merchant, amount, remaining balance.
    - Filters for time period.
  - **Design Problems:**
    - HMW make transaction info easy to scan?
    - HMW highlight unusual spending?
  - **Design Opportunities:**
    - What if parent receives alerts for unusual activity?
    - What if system visualizes spending patterns?

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent attempts to transfer funds.
**Action:** Selected parent account has insufficient balance.
**Goal:** Prevent failed transfers, communicate error.

#### Workflow Variation 1: Inline Error Messaging
- Parent enters amount, system instantly checks balance.
- Error message shown if insufficient.

#### Workflow Variation 2: Pre-Transfer Validation
- Parent selects amount, system validates before confirmation.
- Error message shown, offers options (reduce amount, choose another account).

**Minimum Viable Experience:**
- Parent is prevented from completing transfer with clear error messaging.

**User Goal:** Avoid confusion and failed transactions.
**Business Goal:** Reduce support calls, improve trust.

**Screens:**
2.0 Fund Transfer Modal/Screen -> Er.1 Insufficient Balance Error

**Screen Details:**
- **Er.1 Insufficient Balance Error**
  - **Page Goal:** Communicate transfer failure and guide resolution.
  - **Description:**
    - Error message, options to adjust amount or select another account.
  - **Design Problems:**
    - HMW prevent frustration from failed transfers?
    - HMW offer actionable next steps?
  - **Design Opportunities:**
    - What if system suggests alternate funding sources?
    - What if parent can set up low-balance alerts?

---

## Sequence of Screens for Each Scenario & Workflow

### Scenario 1: Access Dashboard
- 1.0 Youth Account Dashboard

### Scenario 2: Allocate Funds
- 1.0 Youth Account Dashboard -> 2.0 Fund Transfer Modal/Screen -> 2.1 Confirmation -> 2.2 Success Message

### Scenario 3: Set Spending Limit
- 1.0 Youth Account Dashboard -> 3.0 Limit Configuration Modal/Screen -> 3.1 Confirmation -> 3.2 Error State

### Scenario 4: View Spending Activity
- 1.0 Youth Account Dashboard -> 4.0 Activity View -> 4.1 Filter/Insights

### Scenario 5: Insufficient Balance Handling
- 2.0 Fund Transfer Modal/Screen -> Er.1 Insufficient Balance Error

---

## Accessibility & Scalability Considerations
- Ensure all screens are accessible (WCAG 2.1 compliant):
  - High contrast, screen reader support, keyboard navigation.
- Responsive layouts for desktop/tablet.
- Scalable design: modular screens, reusable components.

---

## Summary Table
| Scenario | User Goal | Business Goal | Screens Sequence |
|----------|-----------|--------------|------------------|
| Access Dashboard | Instantly view youth account status | Increase engagement, transparency | 1.0 |
| Allocate Funds | Easily allocate funds | Promote parental control, usage | 1.0 -> 2.0 -> 2.1 -> 2.2 |
| Set Spending Limit | Set boundaries for youth | Encourage responsible spending | 1.0 -> 3.0 -> 3.1 -> 3.2 |
| View Spending Activity | Understand youth spending | Provide actionable insights | 1.0 -> 4.0 -> 4.1 |
| Insufficient Balance | Avoid failed transfers | Reduce support, improve trust | 2.0 -> Er.1 |

---

## Design Problems & Opportunities (Summary)
- HMW make key information immediately visible?
- HMW prevent accidental or failed transfers?
- HMW make limit configuration intuitive?
- HMW highlight unusual spending?
- HMW offer actionable next steps after errors?

- What if dashboard adapts to highlight unusual activity?
- What if system suggests limits or transfers?
- What if parent can schedule recurring transfers or alerts?
- What if system visualizes spending patterns?

---

## Minimum Viable Experience
- Parent can access dashboard, allocate funds, set limits, view activity, and handle errors efficiently.
- All workflows are accessible and scalable.
