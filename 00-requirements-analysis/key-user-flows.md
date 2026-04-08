# 🔄 Key User Flows – iDURAR ERP/CRM

---

## 📌 Purpose

This document identifies the main user flows in the iDURAR ERP/CRM system from a QA perspective.

The goal is to understand how users interact with the application and to define the most important business paths for testing.

---

## 🎯 Why These Flows Matter

Key user flows represent the most valuable and business-critical actions in the system.

Testing these flows helps to:
- validate core functionality
- identify high-impact defects
- prioritize testing effort based on business importance

---

## 🔐 Flow 1 – User Login

### Description
A user enters credentials and attempts to access the system dashboard.

### Main Steps
1. Open login page
2. Enter email and password
3. Submit login form
4. Access dashboard

### Expected Outcome
- Valid credentials allow access
- Invalid credentials are rejected
- Empty fields trigger validation

### QA Coverage
- TC-LOGIN-01 – Verify login with valid credentials
- TC-LOGIN-02 – Verify login with invalid credentials
- TC-LOGIN-03 – Verify login validation with empty fields

### Risks
- No users available in database
- Setup script fails to create default admin
- Login flow blocked before dashboard access

### Related Defects
- BUG-LOGIN-002
- BUG-SETUP-001

---

## 👥 Flow 2 – Customer Management

### Description
A logged-in user creates, edits, or removes customer records.

### Main Steps
1. Log into the system
2. Navigate to customer module
3. Create or update customer data
4. Save changes

### Expected Outcome
- Customer data is stored correctly
- Required fields are validated
- Updated data is visible in the system

### QA Coverage
- To be covered by future customer test cases

### Risks
- Login blocker prevents access to customer module
- Missing validation may allow incomplete or incorrect customer data

---

## 🧾 Flow 3 – Invoice Creation

### Description
A logged-in user creates an invoice for a selected customer.

### Main Steps
1. Log into the system
2. Navigate to invoice module
3. Select customer
4. Add invoice items
5. Save invoice

### Expected Outcome
- Invoice is created successfully
- Values and totals are calculated correctly
- Invoice is linked to the correct customer

### QA Coverage
- To be covered by future invoice test cases

### Risks
- Incorrect calculations
- Missing customer linkage
- Validation issues in invoice fields

---

## 💳 Flow 4 – Payment Registration

### Description
A logged-in user records payment information related to an invoice.

### Main Steps
1. Log into the system
2. Open invoice or payment section
3. Enter payment details
4. Save payment record

### Expected Outcome
- Payment is registered successfully
- Payment is associated with the correct invoice
- Financial data is updated correctly

### QA Coverage
- To be covered by future payment test cases

### Risks
- Missing setup data for payment configuration
- Incorrect payment-to-invoice mapping
- Incomplete payment records

---

## ⚠️ Testing Implications

The login flow is currently the most critical entry point because it blocks access to all other business flows.

As a result:
- Login-related defects have the highest testing priority
- Setup and bootstrap issues must be treated as blockers
- Further functional coverage depends on resolving or working around authentication blockers

---

## 🔗 Traceability

This document supports:
- Requirements understanding
- Risk-based prioritization
- Test case design
- Defect analysis

Current traceability:
- Login flow → TC-LOGIN-01, TC-LOGIN-02, TC-LOGIN-03
- Setup blocker → BUG-SETUP-001
- User availability issue → BUG-LOGIN-002

---

## 🧠 QA Notes

This flow-based view helps connect business processes with testing activities.

Instead of testing isolated screens only, QA focuses on end-to-end user journeys and system behavior across connected modules.
