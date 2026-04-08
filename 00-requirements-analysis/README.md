# 🧠 Requirements Analysis – iDURAR ERP/CRM

---

## 📌 Overview

This section contains the initial analysis of the iDURAR ERP/CRM system from a Quality Assurance perspective.

The goal of this analysis is to:
- understand the system before testing
- identify key business flows
- detect potential risks early
- support test planning and prioritization

---

## 📂 Contents

### 📄 system-overview.md
High-level description of the system architecture, modules, and functionality.

👉 Focus:
- system purpose
- core modules
- technical stack
- initial observations from testing

---

### 🔄 key-user-flows.md
Description of the main user journeys within the system.

👉 Focus:
- login flow
- customer management
- invoice creation
- payment processing

Each flow is connected with planned or existing test cases.

---

### ⚠️ risk-analysis.md
Identification and evaluation of potential risks in the system.

👉 Focus:
- likelihood vs impact
- business-critical areas
- blockers affecting testing

---

## 🎯 QA Approach

This analysis follows a **risk-based testing approach**, where:

- critical flows are tested first
- blockers are identified early
- testing effort is aligned with business impact

---

## 🔗 Traceability

This section is directly connected to:

- Test Plan → `01-test-plan`
- Test Cases → `02-test-cases`
- Bug Reports → `03-bug-reports`

Example:
- Login flow → TC-LOGIN-01, TC-LOGIN-02, TC-LOGIN-03
- Setup issues → BUG-SETUP-001
- Missing users → BUG-LOGIN-002

---

## ⚠️ Key Findings

During the analysis phase, several critical issues were identified:

- No users available in the database after deployment
- Setup script fails due to missing modules (PaymentMode, Taxes)
- Login functionality is blocked

👉 These issues prevent access to the system and must be resolved before full functional testing.

---

## 🧠 QA Perspective

This section demonstrates a structured QA approach:

1. Understanding the system before testing
2. Identifying high-risk areas
3. Designing tests based on real user flows
4. Linking analysis with test execution

---

## 🚀 Outcome

This requirements analysis serves as a foundation for:

- test design
- test prioritization
- defect identification
- end-to-end testing strategy

---

## 📎 Notes

All findings and observations are based on hands-on testing of a locally deployed iDURAR instance (Docker environment).
