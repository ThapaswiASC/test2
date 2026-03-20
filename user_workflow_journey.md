# UX Workflow Documentation: Parent Managing Youth Account

## Experience Mindset

**Primary User:** Parent/Guardian

**Experience:** Managing a youth account to teach financial responsibility, including fund allocation, spending limits, and activity monitoring.

---

## Identified Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application and wants to view/manage the youth account.

#### Variation A: Direct Dashboard Access
- **Workflow:**
  1. Parent logs in
  2. Selects "Youth Accounts" from main navigation
  3. Youth account dashboard loads with balance, recent activity, and quick actions

#### Variation B: Dashboard via Notifications
- **Workflow:**
  1. Parent logs in
  2. Receives notification (e.g., "Youth account activity alert")
  3. Clicks notification, landing directly on youth account dashboard

**User Goal:** Quickly access youth account status and actions.
**Business Goal:** Increase engagement and transparency for youth account features.

**Screens:**
- **1.0 Login Page**
  - *Goal:* Secure authentication
  - *Description:* Parent enters credentials
  - *Design Problems:* HMW ensure accessibility for all parents?
  - *Opportunities:* What if biometric login is offered?
- **2.0 Main Dashboard**
  - *Goal:* Central hub for all accounts
  - *Description:* Overview of all linked accounts, including youth
  - *Design Problems:* HMW highlight youth account for quick access?
  - *Opportunities:* Personalized account highlights
- **3.0 Youth Account Dashboard**
  - *Goal:* Present youth account details and actions
  - *Description:* Balance, recent activity, quick actions (add funds, set limits)
  - *Design Problems:* HMW communicate balance and actions clearly?
  - *Opportunities:* Visual cues for account health

**Screen Sequence:** 1.0 Login Page → 2.0 Main Dashboard → 3.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent wants to transfer money to the youth account.

#### Variation A: Inline Transfer Modal
- **Workflow:**
  1. On youth dashboard, parent clicks "Add Funds"
  2. Modal opens for transfer details
  3. Parent selects source account, enters amount
  4. Confirmation step
  5. Success or error message

#### Variation B: Dedicated Transfer Page
- **Workflow:**
  1. Parent selects "Add Funds" (navigates to new page)
  2. Fills transfer form
  3. Confirmation and result

**User Goal:** Easily and securely transfer funds to youth account.
**Business Goal:** Encourage regular funding, reduce friction in transfers.

**Screens:**
- **3.1 Add Funds Modal/Page**
  - *Goal:* Facilitate fund transfer
  - *Description:* Source account selector, amount input, confirm button
  - *Design Problems:* HMW prevent accidental transfers?
  - *Opportunities:* Pre-fill frequent transfer amounts
- **Pu.1 Transfer Confirmation**
  - *Goal:* Confirm details before committing
  - *Description:* Summary of transfer, confirm/cancel
  - *Design Problems:* HMW ensure clarity of action?
  - *Opportunities:* Show impact on balances
- **Pu.2 Success/Error Message**
  - *Goal:* Communicate result
  - *Description:* Success or error (e.g., insufficient funds)
  - *Design Problems:* HMW make errors actionable?
  - *Opportunities:* Suggest solutions (e.g., link to add funds to parent account)
- **Er.1 Insufficient Balance Error**
  - *Goal:* Prevent failed transfers
  - *Description:* Error message with guidance

**Screen Sequence:** 3.0 Youth Account Dashboard → 3.1 Add Funds Modal/Page → Pu.1 Transfer Confirmation → Pu.2 Success/Error Message/Er.1

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to set or edit a spending limit for the youth account.

#### Variation A: Inline Limit Editor
- **Workflow:**
  1. On dashboard, parent clicks "Edit Limit"
  2. Inline editor appears
  3. Parent enters new value, saves
  4. Limit updates on dashboard

#### Variation B: Dedicated Limit Management Page
- **Workflow:**
  1. Parent selects "Manage Limits"
  2. Navigates to limit configuration page
  3. Edits and saves limit

**User Goal:** Control youth spending easily.
**Business Goal:** Promote responsible usage and parental peace of mind.

**Screens:**
- **3.2 Spending Limit Editor/Management**
  - *Goal:* Configure and display limits
  - *Description:* Input for weekly limit, contextual guidance
  - *Design Problems:* HMW prevent invalid values?
  - *Opportunities:* Visualize spending vs. limit
- **Pu.3 Limit Update Confirmation**
  - *Goal:* Confirm changes
  - *Description:* Confirmation message

**Screen Sequence:** 3.0 Youth Account Dashboard → 3.2 Spending Limit Editor/Management → Pu.3 Limit Update Confirmation

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review youth account transactions.

#### Variation A: Inline Recent Activity List
- **Workflow:**
  1. On dashboard, parent scrolls to recent activity
  2. Can filter by time period

#### Variation B: Full Activity Page
- **Workflow:**
  1. Parent selects "View All Activity"
  2. Navigates to detailed transaction history
  3. Applies filters (date, merchant, amount)

**User Goal:** Monitor youth spending patterns.
**Business Goal:** Build trust and promote financial education.

**Screens:**
- **3.3 Activity List (Inline or Page)**
  - *Goal:* Display transactions clearly
  - *Description:* List with date, merchant, amount, remaining balance; filters
  - *Design Problems:* HMW make patterns easy to spot?
  - *Opportunities:* Highlight unusual activity, provide insights

**Screen Sequence:** 3.0 Youth Account Dashboard → 3.3 Activity List

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more than available in source account.

#### Variation A: Inline Error Message
- **Workflow:**
  1. Parent enters amount
  2. System validates and shows error if insufficient

#### Variation B: Pre-Transfer Balance Check
- **Workflow:**
  1. System disables transfer option if balance is insufficient

**User Goal:** Understand and resolve transfer issues quickly.
**Business Goal:** Reduce failed transactions and support requests.

**Screens:**
- **Er.1 Insufficient Balance Error**
  - *Goal:* Prevent and explain failed transfers
  - *Description:* Error message with next steps
  - *Design Problems:* HMW guide parent to resolution?
  - *Opportunities:* Offer direct link to fund parent account

**Screen Sequence:** 3.1 Add Funds Modal/Page → Er.1 Insufficient Balance Error

---

## Minimum Viable Experience (MVE)

### User Scenario Example
*Sam, a parent, wants to add funds to his child’s youth account and set a weekly spending limit. He logs in, navigates to the youth account dashboard, transfers $50, and sets a $20/week limit. He reviews recent transactions to ensure responsible spending.*

- **User Goal:** Empower parents to manage youth accounts efficiently and confidently.
- **Business Goal:** Drive adoption of youth account features, build trust, and reduce support overhead.

---

## Summary Table of Screens
| Screen Number | Title                        | Goal                                  |
|---------------|------------------------------|---------------------------------------|
| 1.0           | Login Page                   | Secure authentication                 |
| 2.0           | Main Dashboard               | Overview of all accounts              |
| 3.0           | Youth Account Dashboard      | Manage youth account                  |
| 3.1           | Add Funds Modal/Page         | Transfer funds                        |
| 3.2           | Spending Limit Editor        | Configure spending limits             |
| 3.3           | Activity List                | Review transactions                   |
| Pu.1          | Transfer Confirmation        | Confirm transfer                      |
| Pu.2          | Success/Error Message        | Communicate result                    |
| Pu.3          | Limit Update Confirmation    | Confirm limit update                  |
| Er.1          | Insufficient Balance Error   | Explain failed transfer               |

---

## Accessibility & Scalability Considerations
- All actions accessible via keyboard and screen reader
- Color contrast and text size meet WCAG standards
- Responsive layouts for desktop and tablet
- Error states provide actionable guidance
- Flows support future features (e.g., multiple youth accounts)

---

## Complete Workflow Sequences

### Example: Add Funds & Set Limit
1.0 Login Page → 2.0 Main Dashboard → 3.0 Youth Account Dashboard → 3.1 Add Funds Modal/Page → Pu.1 Transfer Confirmation → Pu.2 Success/Error Message → 3.2 Spending Limit Editor → Pu.3 Limit Update Confirmation → 3.3 Activity List

### Example: View Activity & Handle Error
1.0 Login Page → 2.0 Main Dashboard → 3.0 Youth Account Dashboard → 3.3 Activity List → 3.1 Add Funds Modal/Page → Er.1 Insufficient Balance Error

---

## Design Problems & Opportunities (HMW = How Might We)
- HMW make youth account management intuitive for non-technical parents?
- HMW prevent accidental or unauthorized transfers?
- HMW encourage positive financial behaviors for youth?
- HMW surface important activity without overwhelming the user?
- What if we provide contextual tips for teaching financial literacy?
- What if parents can set up recurring transfers or limits?
- What if the dashboard adapts to show trends and insights over time?

---

*This documentation balances user needs (clarity, control, education) with business objectives (adoption, engagement, reduced support), while ensuring accessibility and scalability for future growth.*
