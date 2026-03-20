# UX Design User Workflow Documentation: Youth Account Fund Management

## Story Context

**Story:** Parent can allocate and manage funds for a youth account

**Business Goal:** As a parent or guardian, I want to allocate and manage funds for my child’s youth account so that I can teach financial responsibility while maintaining visibility and control over spending.

---

## Experience Mindset & Scenario Identification

### Experience: Youth Account Management

#### Scenarios:
1. Access youth account dashboard
2. Allocate funds to youth account
3. Set spending limit
4. View youth spending activity
5. Handle insufficient balance during fund allocation

Each scenario is detailed below with at least two workflow design variations, minimum viable experience, user and business goals, screen sequence, and design considerations.

---

## Scenario 1: Access Youth Account Dashboard

### Context:
Parent is logged into the banking web application and navigates to the youth account section.

### User Goal:
To quickly access an overview of the youth account, including balance and recent activity.

### Business Goal:
To provide parents with clear visibility and easy access to youth account management features, fostering trust and engagement.

### Workflow Variations:

#### Variation 1: Direct Navigation
- Parent clicks on "Youth Account" from main dashboard.
- Youth account dashboard loads with balance, spending limit, and recent activity.

#### Variation 2: Guided Entry
- Parent selects "Accounts" > "Youth Account" from sidebar navigation.
- System displays a welcome message and onboarding tips before showing dashboard.

### Minimum Viable Experience:
Parent sees youth account balance, spending limit, and recent transactions immediately upon entry.

### Screen List & Details:

#### 1.0 Youth Account Dashboard
- **Goal:** Communicate youth account status and enable quick actions.
- **Description:** Displays balance summary, fund allocation action, spending limit display, recent transactions, and quick actions.
- **Design Problems:**
  - HMW make key actions (e.g., Add Funds) prominent?
  - HMW ensure information hierarchy for quick understanding?
- **Design Opportunities:**
  - What if dashboard adapts to parent’s previous actions?
  - What if accessibility features (e.g., screen reader support) are built-in?

#### 1.1 Onboarding Pop-Up (Optional)
- **Goal:** Educate new users about youth account features.
- **Description:** Brief tips, dismissible, accessible.
- **Design Problems:**
  - HMW avoid overwhelming users with information?
- **Design Opportunities:**
  - What if onboarding is personalized based on user history?

### Screen Sequence:
1.0 Youth Account Dashboard -> 1.1 Onboarding Pop-Up (optional)

---

## Scenario 2: Allocate Funds to Youth Account

### Context:
Parent is on the youth account dashboard and wants to add funds.

### User Goal:
To transfer funds to the youth account quickly and securely.

### Business Goal:
To facilitate seamless fund transfers, increasing parent engagement and youth account usage.

### Workflow Variations:

#### Variation 1: Inline Fund Transfer
- Parent clicks "Add Funds" button on dashboard.
- Inline modal opens for source account selection and amount entry.
- Confirmation and success message shown.

#### Variation 2: Step-by-Step Wizard
- Parent selects "Add Funds" > System guides through source account, amount, confirmation, and success screens.

### Minimum Viable Experience:
Parent can select source account, enter amount, confirm, and see success/error feedback.

### Screen List & Details:

#### 2.0 Fund Transfer Modal/Screen
- **Goal:** Enable secure, accessible fund transfer.
- **Description:** Source account selector, amount input, validation, confirmation, success/error messages.
- **Design Problems:**
  - HMW minimize steps while ensuring security?
  - HMW communicate validation errors clearly?
- **Design Opportunities:**
  - What if predictive suggestions for transfer amounts are shown?
  - What if transfer history is accessible?

#### Pu.1 Success Message Pop-Up
- **Goal:** Confirm successful transfer.
- **Description:** Accessible, clear confirmation.

#### Er.1 Insufficient Balance Error
- **Goal:** Inform parent of insufficient funds.
- **Description:** Clear, actionable error message with guidance.

### Screen Sequence:
1.0 Youth Account Dashboard -> 2.0 Fund Transfer Modal/Screen -> Pu.1 Success Message Pop-Up / Er.1 Insufficient Balance Error

---

## Scenario 3: Set Spending Limit

### Context:
Parent is viewing youth account management section and wants to configure a weekly spending limit.

### User Goal:
To set and manage spending limits for youth account easily.

### Business Goal:
To empower parents to teach financial responsibility and prevent overspending.

### Workflow Variations:

#### Variation 1: Inline Limit Configuration
- Parent clicks "Set Limit" on dashboard.
- Editable input appears for weekly limit.
- Limit saved and displayed.

#### Variation 2: Dedicated Limit Management Screen
- Parent navigates to "Spending Limit" section.
- Configures limit, sees contextual guidance, saves changes.

### Minimum Viable Experience:
Parent can set/edit weekly limit, see current limit, and receive feedback on invalid values.

### Screen List & Details:

#### 3.0 Spending Limit Configuration
- **Goal:** Allow easy configuration and visibility of spending limits.
- **Description:** Input for weekly limit, display of current limit, contextual guidance, validation.
- **Design Problems:**
  - HMW prevent invalid values?
  - HMW make limit configuration intuitive?
- **Design Opportunities:**
  - What if system suggests limits based on spending history?
  - What if guidance is personalized?

#### Pu.2 Limit Saved Confirmation
- **Goal:** Confirm successful limit update.
- **Description:** Accessible, clear confirmation.

#### Er.2 Invalid Limit Value Error
- **Goal:** Prevent and inform about invalid input.
- **Description:** Clear error, actionable guidance.

### Screen Sequence:
1.0 Youth Account Dashboard -> 3.0 Spending Limit Configuration -> Pu.2 Limit Saved Confirmation / Er.2 Invalid Limit Value Error

---

## Scenario 4: View Youth Spending Activity

### Context:
Parent is viewing youth account dashboard and wants to see recent transactions.

### User Goal:
To monitor youth spending activity and identify patterns.

### Business Goal:
To provide transparency and insights for parents, driving engagement and trust.

### Workflow Variations:

#### Variation 1: Transaction List on Dashboard
- Recent transactions shown directly on dashboard.
- Filters for time period available.

#### Variation 2: Dedicated Activity Screen
- Parent clicks "View Activity" to open full transaction history with filters and analytics.

### Minimum Viable Experience:
Parent can see transaction date, merchant/activity, amount spent, remaining balance, and filter by time period.

### Screen List & Details:

#### 4.0 Transaction Activity List
- **Goal:** Make transaction information easy to scan and understand.
- **Description:** List with date, merchant, amount, balance, filters. Responsive for desktop/tablet.
- **Design Problems:**
  - HMW help parents quickly identify spending patterns?
  - HMW ensure accessibility for scanning data?
- **Design Opportunities:**
  - What if visual analytics highlight unusual patterns?
  - What if parents can set alerts for specific activity?

#### 4.1 Filter Pop-Up
- **Goal:** Enable filtering by time period.
- **Description:** Accessible, easy-to-use filter controls.

### Screen Sequence:
1.0 Youth Account Dashboard -> 4.0 Transaction Activity List -> 4.1 Filter Pop-Up

---

## Scenario 5: Handle Insufficient Balance During Fund Allocation

### Context:
Parent attempts to transfer funds but selected account lacks sufficient balance.

### User Goal:
To understand why transfer failed and what steps to take next.

### Business Goal:
To reduce frustration, guide parents to resolve issues, and maintain trust.

### Workflow Variations:

#### Variation 1: Inline Error Message
- Error shown immediately on fund transfer modal.
- Guidance provided for resolving.

#### Variation 2: Error Pop-Up with Actionable Steps
- Error pop-up explains issue and offers options (e.g., link to add funds, retry).

### Minimum Viable Experience:
Parent sees clear error message and guidance for next steps.

### Screen List & Details:

#### Er.1 Insufficient Balance Error
- **Goal:** Communicate transfer failure and guide resolution.
- **Description:** Clear, accessible error message, actionable steps.
- **Design Problems:**
  - HMW reduce frustration when errors occur?
  - HMW guide parents to resolve issues efficiently?
- **Design Opportunities:**
  - What if system offers instant solutions (e.g., link to add funds)?
  - What if error messages are personalized?

### Screen Sequence:
2.0 Fund Transfer Modal/Screen -> Er.1 Insufficient Balance Error

---

## Summary of Screen Sequences for Each Scenario

1. Access youth account dashboard:
   - 1.0 Youth Account Dashboard -> 1.1 Onboarding Pop-Up (optional)

2. Allocate funds to youth account:
   - 1.0 Youth Account Dashboard -> 2.0 Fund Transfer Modal/Screen -> Pu.1 Success Message Pop-Up / Er.1 Insufficient Balance Error

3. Set spending limit:
   - 1.0 Youth Account Dashboard -> 3.0 Spending Limit Configuration -> Pu.2 Limit Saved Confirmation / Er.2 Invalid Limit Value Error

4. View youth spending activity:
   - 1.0 Youth Account Dashboard -> 4.0 Transaction Activity List -> 4.1 Filter Pop-Up

5. Handle insufficient balance during fund allocation:
   - 2.0 Fund Transfer Modal/Screen -> Er.1 Insufficient Balance Error

---

## Accessibility & Scalability Considerations
- All screens must be accessible (keyboard navigation, screen reader support, color contrast).
- Responsive layouts for desktop and tablet.
- Error messages and confirmations must be clear, actionable, and accessible.
- Workflows should support future expansion (e.g., multiple youth accounts, additional parental controls).

---

## Edge Cases & Use Cases Considered
- Multiple youth accounts per parent
- Invalid input values (e.g., negative transfer amount, excessive spending limit)
- Accessibility for parents with disabilities
- Tablet and desktop views
- Error handling for failed transfers
- Guidance for new users

---

## Design System Integration Opportunities
- Use modular UI components (e.g., modal, pop-up, dashboard cards, filters)
- Ensure consistency across workflows
- Enable easy updates and scalability

---

## Minimum Viable Experience Summary
For each scenario, the minimum viable experience includes clear, accessible, and actionable screens enabling parents to manage youth accounts efficiently while supporting business goals of engagement, trust, and financial education.
