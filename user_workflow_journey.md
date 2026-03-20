# UX Design User Workflow Documentation: Parent Managing Youth Account Funds

## Experience Overview
**User:** Parent or Guardian  
**Experience:** Allocating and managing funds for a youth account  
**Business Goal:** Enable parents to teach financial responsibility to their children while maintaining visibility and control over spending.

---

## Identified Scenarios & Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application and wants to view/manage the youth account.

#### Variation 1: Dashboard as Default Landing Page
- **Workflow:**
  1. Parent logs in → 2. Youth account dashboard is shown by default
- **User Goal:** Quickly access youth account info without extra navigation
- **Business Goal:** Reduce friction, increase engagement

#### Variation 2: Dashboard via Navigation Menu
- **Workflow:**
  1. Parent logs in → 2. Selects 'Youth Accounts' from main menu → 3. Youth account dashboard is displayed
- **User Goal:** Discover youth account features through structured navigation
- **Business Goal:** Highlight youth account as a distinct feature

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent is on the youth account dashboard and wants to add funds.

#### Variation 1: Inline Fund Transfer Widget
- **Workflow:**
  1. On dashboard, parent clicks 'Add Funds' → 2. Inline widget opens for transfer → 3. Parent selects source account, enters amount → 4. Confirms transfer → 5. Success or error message shown
- **User Goal:** Add funds quickly without leaving the dashboard
- **Business Goal:** Encourage frequent use, minimize drop-off

#### Variation 2: Dedicated Fund Transfer Page
- **Workflow:**
  1. On dashboard, parent clicks 'Add Funds' → 2. Redirected to dedicated transfer page → 3. Completes transfer steps → 4. Redirected back to dashboard with confirmation
- **User Goal:** Provide a focused, distraction-free transfer experience
- **Business Goal:** Reduce errors, support complex transfers

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to configure or update a weekly spending limit for the youth account.

#### Variation 1: Quick Edit on Dashboard
- **Workflow:**
  1. On dashboard, parent sees current limit → 2. Clicks 'Edit' → 3. Inline edit field appears → 4. Parent updates value → 5. Saves and sees confirmation
- **User Goal:** Change limits quickly
- **Business Goal:** Lower friction for responsible oversight

#### Variation 2: Settings Modal/Section
- **Workflow:**
  1. Parent clicks 'Manage Limits' → 2. Modal or settings section opens → 3. Parent configures limit with guidance → 4. Saves changes → 5. Confirmation shown
- **User Goal:** Understand and manage limits with guidance
- **Business Goal:** Educate parents, reduce misconfiguration

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review recent transactions on the youth account.

#### Variation 1: Activity Feed on Dashboard
- **Workflow:**
  1. Dashboard shows recent activity summary → 2. Parent clicks 'View All' for full transaction list
- **User Goal:** Scan activity at a glance, drill down as needed
- **Business Goal:** Increase transparency, build trust

#### Variation 2: Dedicated Activity Page with Filters
- **Workflow:**
  1. Parent navigates to 'Activity' tab/section → 2. Full transaction list with filters (date, amount, merchant)
- **User Goal:** Analyze spending patterns, find specific transactions
- **Business Goal:** Empower parents with insights

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more funds than available in the source account.

#### Variation 1: Inline Error on Amount Entry
- **Workflow:**
  1. Parent enters amount > balance → 2. Inline error message appears, disables 'Confirm'
- **User Goal:** Prevent mistakes before submitting
- **Business Goal:** Reduce failed transactions, improve satisfaction

#### Variation 2: Error on Confirmation Attempt
- **Workflow:**
  1. Parent enters amount, clicks 'Confirm' → 2. Error modal or toast appears, explains issue
- **User Goal:** Receive clear feedback, understand next steps
- **Business Goal:** Educate users, reduce support requests

---

## Minimum Viable Experience (MVE)

### User Scenario
**Context:** Jamie, a parent, wants to add funds to their child’s youth account, set a weekly spending limit, and review recent spending to teach financial responsibility.

### User Goal
- To allocate funds, set spending limits, and monitor youth account activity efficiently and securely.

### Business Goal
- Increase adoption and engagement of youth accounts by providing parents with effective tools for oversight and education.

---

## Screen List & Details

### 1.0 Youth Account Dashboard
- **Page Goal:** Provide an overview of youth account status and quick access to key actions
- **Screen Description:**
  - Shows current balance, recent activity, and spending limit
  - Prominent 'Add Funds' and 'Manage Limit' actions
  - Quick summary of recent transactions
- **Design Problems:**
  - HMW present all key info without overwhelming the user?
  - HMW prioritize actions for frequent tasks?
- **Design Opportunities:**
  - What if dashboard adapts to show tips based on usage?
  - What if parents can customize dashboard widgets?

### 2.0 Fund Transfer (Add Funds)
- **Page Goal:** Enable secure, intuitive transfer of funds from parent to youth account
- **Screen Description:**
  - Select source account, enter amount, see available balance
  - Inline validation for limits and insufficient funds
  - Confirmation step before transfer
- **Design Problems:**
  - HMW minimize errors in fund transfer?
  - HMW reassure parents about transaction security?
- **Design Opportunities:**
  - What if we suggest typical transfer amounts based on history?
  - What if we provide instant feedback on transfer status?

### 3.0 Spending Limit Management
- **Page Goal:** Allow parents to set and adjust weekly spending limits
- **Screen Description:**
  - Display current limit, allow easy editing
  - Contextual help explaining limits
  - Prevent invalid entries
- **Design Problems:**
  - HMW make limits understandable for all users?
  - HMW prevent accidental misconfiguration?
- **Design Opportunities:**
  - What if we show projected impact of limits?
  - What if we allow temporary overrides for special occasions?

### 4.0 Activity View
- **Page Goal:** Let parents review and analyze youth account spending
- **Screen Description:**
  - List of transactions: date, merchant, amount, remaining balance
  - Filters for time period, type, amount
  - Visual cues for unusual activity
- **Design Problems:**
  - HMW make it easy to spot trends or issues?
  - HMW ensure accessibility for all parents?
- **Design Opportunities:**
  - What if we highlight educational moments (e.g., first purchase)?
  - What if parents can tag or annotate transactions?

### Er.1 Insufficient Funds Error
- **Page Goal:** Clearly communicate why a transfer cannot proceed
- **Screen Description:**
  - Inline or modal error message with guidance
  - Suggest corrective actions (e.g., choose different account, lower amount)
- **Design Problems:**
  - HMW reduce frustration from failed transfers?
- **Design Opportunities:**
  - What if we offer to set up low-balance alerts?

---

## Example Workflow Sequences

### Workflow 1: Quick Fund Allocation
1.0 Youth Account Dashboard → 2.0 Fund Transfer (Add Funds) → 1.0 Dashboard (with updated balance)

### Workflow 2: Set Spending Limit
1.0 Youth Account Dashboard → 3.0 Spending Limit Management → 1.0 Dashboard (with updated limit)

### Workflow 3: Review Activity
1.0 Youth Account Dashboard → 4.0 Activity View

### Workflow 4: Handle Insufficient Funds
2.0 Fund Transfer (Add Funds) → Er.1 Insufficient Funds Error → 2.0 Fund Transfer (retry or cancel)

---

## Accessibility & Scalability Considerations
- All actions are accessible via keyboard and screen reader
- Clear visual hierarchy and color contrast
- Responsive layouts for desktop and tablet
- Scalable to support multiple youth accounts per parent
- Error states provide actionable guidance

---

## Summary Table of Screens
| Screen Number | Title                         | Purpose                                      |
|---------------|-------------------------------|----------------------------------------------|
| 1.0           | Youth Account Dashboard       | Overview, quick actions                      |
| 2.0           | Fund Transfer (Add Funds)     | Transfer funds securely                      |
| 3.0           | Spending Limit Management     | Configure weekly spending limits             |
| 4.0           | Activity View                 | Review youth account transactions            |
| Er.1          | Insufficient Funds Error      | Handle failed fund transfers                 |

---

## End of User Workflow Documentation
