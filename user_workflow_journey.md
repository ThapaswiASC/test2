# UX Workflow Documentation: Parent Management of Youth Account Funds

## Experience Mindset

**Primary User:** Parent/Guardian
**Experience:** Managing a youth banking account (teaching financial responsibility, maintaining control)

### Key Scenarios
1. Access youth account dashboard
2. Allocate funds to youth account
3. Set spending limit
4. View youth spending activity
5. Handle insufficient balance during fund allocation

---

## Scenario 1: Access Youth Account Dashboard

### Scenario Context
Parent, after logging in, wants to review their child’s youth account status and recent activity.

### User Goal
To quickly and clearly view youth account balance and recent transactions.

### Business Goal
Increase engagement and trust by providing transparent, easy-to-understand account information.

### Workflow Design Variations

#### Variation 1: Dashboard as Landing Page
- **1.0 Dashboard Home**
  - **Goal:** Immediate overview of youth account
  - **Description:** Upon login, parent lands directly on dashboard showing balance, recent activity, and quick actions.
  - **Design Problems:**
    - HMW ensure the dashboard is not overwhelming?
    - HMW prioritize information for quick scanning?
  - **Design Opportunities:**
    - What if parents could customize dashboard widgets?
    - What if a virtual assistant summarizes recent activity?

#### Variation 2: Dashboard via Navigation
- **1.0 Main Menu**
  - **Goal:** Provide clear navigation to youth account section
  - **Description:** Parent selects "Youth Accounts" from main menu.
  - **Design Problems:**
    - HMW make navigation intuitive for first-time users?
  - **Design Opportunities:**
    - What if the menu highlights new activity?
- **2.0 Youth Account Dashboard**
  - (Same as above)

### Screen Sequence
- Variation 1: 1.0 Dashboard Home
- Variation 2: 1.0 Main Menu -> 2.0 Youth Account Dashboard

---

## Scenario 2: Allocate Funds to Youth Account

### Scenario Context
Parent wants to transfer money from their account to the youth account, e.g., for allowance or purchases.

### User Goal
To transfer funds quickly, securely, and with clear confirmation.

### Business Goal
Promote use of youth accounts, reduce support queries about transfers.

### Workflow Design Variations

#### Variation 1: Inline Transfer Widget
- **1.0 Dashboard Home**
- **1.1 Add Funds Pop-Up (Pu.1)**
  - **Goal:** Enable quick fund allocation
  - **Description:** Parent clicks "Add Funds"; modal appears with source account selector, amount input, and confirm button.
  - **Design Problems:**
    - HMW prevent errors in amount entry?
    - HMW make source account selection clear?
  - **Design Opportunities:**
    - What if suggested amounts are based on past transfers?
- **1.2 Confirmation Pop-Up (Pu.2)**
  - **Goal:** Confirm transfer before execution
  - **Description:** Shows transfer summary, asks for confirmation.

#### Variation 2: Dedicated Transfer Page
- **1.0 Dashboard Home**
- **2.0 Fund Transfer Page**
  - **Goal:** Provide detailed transfer flow
  - **Description:** Parent navigates to a full page for fund transfer, with contextual tips and validation.
  - **Design Problems:**
    - HMW keep the flow efficient while providing guidance?
  - **Design Opportunities:**
    - What if the page shows projected balance after transfer?
- **2.1 Success Pop-Up (Pu.1)**

### Screen Sequence
- Variation 1: 1.0 Dashboard Home -> 1.1 Add Funds Pop-Up -> 1.2 Confirmation Pop-Up
- Variation 2: 1.0 Dashboard Home -> 2.0 Fund Transfer Page -> 2.1 Success Pop-Up

---

## Scenario 3: Set Spending Limit

### Scenario Context
Parent wants to set or adjust a weekly spending limit for the youth account.

### User Goal
To easily configure and understand spending limits.

### Business Goal
Empower parents to teach budgeting, reduce risk of overspending.

### Workflow Design Variations

#### Variation 1: Inline Limit Editor
- **1.0 Dashboard Home**
- **1.1 Edit Limit Pop-Up (Pu.1)**
  - **Goal:** Quick access to limit settings
  - **Description:** Parent clicks "Edit Limit"; modal allows input, with guidance and validation.
  - **Design Problems:**
    - HMW explain limits without jargon?
    - HMW prevent invalid values?
  - **Design Opportunities:**
    - What if the system suggests limits based on age or spending history?

#### Variation 2: Dedicated Limit Management Page
- **1.0 Dashboard Home**
- **2.0 Spending Limit Page**
  - **Goal:** Provide comprehensive limit management
  - **Description:** Full page with current limit, edit controls, and educational content.
  - **Design Problems:**
    - HMW balance detail with simplicity?
  - **Design Opportunities:**
    - What if parents could set multiple types of limits (daily, category)?

### Screen Sequence
- Variation 1: 1.0 Dashboard Home -> 1.1 Edit Limit Pop-Up
- Variation 2: 1.0 Dashboard Home -> 2.0 Spending Limit Page

---

## Scenario 4: View Youth Spending Activity

### Scenario Context
Parent wants to review where and how their child is spending money.

### User Goal
To quickly scan and filter youth account transactions.

### Business Goal
Increase transparency, help parents guide responsible spending.

### Workflow Design Variations

#### Variation 1: Embedded Transaction List
- **1.0 Dashboard Home**
  - **Goal:** Show recent transactions at a glance
  - **Description:** List of recent transactions with date, merchant, amount, and balance. Filter by time period.
  - **Design Problems:**
    - HMW make patterns visible?
  - **Design Opportunities:**
    - What if the system highlights unusual spending?

#### Variation 2: Full Activity Page
- **1.0 Dashboard Home**
- **2.0 Activity Page**
  - **Goal:** Provide detailed, filterable transaction history
  - **Description:** Full page with advanced filters, export options, and spending summaries.
  - **Design Problems:**
    - HMW keep filtering simple?
  - **Design Opportunities:**
    - What if parents could set alerts for specific merchants or amounts?

### Screen Sequence
- Variation 1: 1.0 Dashboard Home
- Variation 2: 1.0 Dashboard Home -> 2.0 Activity Page

---

## Scenario 5: Handle Insufficient Balance During Fund Allocation

### Scenario Context
Parent attempts to transfer more funds than available in their account.

### User Goal
To understand why the transfer failed and what to do next.

### Business Goal
Reduce failed transactions and support calls.

### Workflow Design Variations

#### Variation 1: Inline Error Message
- **1.0 Add Funds Pop-Up (Pu.1)**
- **Er.1 Insufficient Balance Error**
  - **Goal:** Clearly communicate the error
  - **Description:** Error message appears inline, with actionable suggestions (e.g., "Choose smaller amount" or "View account balance").
  - **Design Problems:**
    - HMW avoid user frustration?
  - **Design Opportunities:**
    - What if the system suggests alternative funding sources?

#### Variation 2: Error Pop-Up
- **1.0 Add Funds Pop-Up (Pu.1)**
- **Pu.2 Error Modal**
  - **Goal:** Ensure error is noticed and understood
  - **Description:** Modal with error details and next steps.
  - **Design Problems:**
    - HMW prevent repeated errors?
  - **Design Opportunities:**
    - What if the modal links directly to add funds to parent account?

### Screen Sequence
- Variation 1: 1.0 Add Funds Pop-Up -> Er.1 Insufficient Balance Error
- Variation 2: 1.0 Add Funds Pop-Up -> Pu.2 Error Modal

---

## Summary of All Screens (Unique Numbering)

- 1.0 Dashboard Home
- 1.1 Add Funds Pop-Up (Pu.1)
- 1.2 Confirmation Pop-Up (Pu.2)
- 2.0 Fund Transfer Page
- 2.1 Success Pop-Up (Pu.1)
- 1.1 Edit Limit Pop-Up (Pu.1)
- 2.0 Spending Limit Page
- 2.0 Activity Page
- Er.1 Insufficient Balance Error
- Pu.2 Error Modal
- 1.0 Main Menu

---

## Accessibility & Scalability Considerations
- All workflows use clear, high-contrast layouts and large touch targets for accessibility.
- All error states provide actionable, non-technical language.
- All screens are designed to scale for desktop and tablet, with responsive layouts.
- All lists and forms support keyboard navigation and screen readers.
- All pop-ups and modals are accessible via ARIA roles and focus management.

---

## Edge Cases Considered
- Parent with multiple youth accounts
- Parent with no available funds
- Parent with no transaction history
- Attempt to set a negative or zero spending limit
- Network or system errors during fund transfer

---

## Example Workflow Sequences

**Allocate Funds (Variation 1):**
1.0 Dashboard Home → 1.1 Add Funds Pop-Up → 1.2 Confirmation Pop-Up

**Set Spending Limit (Variation 2):**
1.0 Dashboard Home → 2.0 Spending Limit Page

**View Activity (Variation 2):**
1.0 Dashboard Home → 2.0 Activity Page

**Handle Insufficient Balance (Variation 1):**
1.0 Add Funds Pop-Up → Er.1 Insufficient Balance Error

---

# End of Workflow Documentation
