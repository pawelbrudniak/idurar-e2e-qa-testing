# ⚠️ Risk Analysis – iDURAR ERP/CRM

---

## 📌 Purpose

This document identifies potential risks in the iDURAR ERP/CRM system from a QA perspective.

The goal is to:
- highlight areas with the highest probability of failure
- assess business impact
- support risk-based testing prioritization

---

## 🧠 Risk-Based Testing Approach

Testing effort is prioritized based on:

- **Likelihood** – probability of defect occurrence
- **Impact** – effect on business or user experience

---

## 📊 Risk Matrix

| ID | Risk Description | Likelihood | Impact | Priority |
|----|----------------|-----------|--------|----------|
| R1 | No users in database after deployment | High | Critical | 🔴 High |
| R2 | Setup script fails due to missing modules | High | Critical | 🔴 High |
| R3 | Login functionality blocked | High | Critical | 🔴 High |
| R4 | Incorrect validation of login inputs | Medium | High | 🟠 Medium |
| R5 | Incorrect invoice calculations | Medium | High | 🟠 Medium |
| R6 | Missing or incorrect payment configuration | Medium | Medium | 🟡 Medium |
| R7 | Data inconsistency in customer records | Low | High | 🟡 Medium |

---

## 🔍 Detailed Risk Description

---

### 🔴 R1 – No Users in Database

**Description:**  
After deployment, the system does not contain any user accounts.

**Impact:**  
- Users cannot log in  
- Entire system becomes unusable  

**Likelihood:** High  
**Impact Level:** Critical  

**Related Defects:**  
- BUG-LOGIN-002  

**Mitigation:**  
- Execute setup script  
- Verify user creation in database  

---

### 🔴 R2 – Setup Script Failure

**Description:**  
The setup script fails due to missing modules (e.g. PaymentMode, Taxes).

**Impact:**  
- Incomplete system initialization  
- Missing configuration data  
- Broken application state  

**Likelihood:** High  
**Impact Level:** Critical  

**Related Defects:**  
- BUG-SETUP-001  

**Mitigation:**  
- Fix incorrect module imports  
- Validate setup process end-to-end  

---

### 🔴 R3 – Login Blocker

**Description:**  
User cannot log into the system due to missing data or backend errors.

**Impact:**  
- All system functionality is inaccessible  
- Testing cannot proceed  

**Likelihood:** High  
**Impact Level:** Critical  

**Related Test Cases:**  
- TC-LOGIN-01  
- TC-LOGIN-02  
- TC-LOGIN-03  

---

### 🟠 R4 – Login Validation Issues

**Description:**  
Login form does not properly validate input fields.

**Impact:**  
- Poor user experience  
- Invalid requests sent to backend  

**Likelihood:** Medium  
**Impact Level:** High  

---

### 🟠 R5 – Invoice Calculation Errors

**Description:**  
Incorrect calculation of totals, taxes, or invoice values.

**Impact:**  
- Financial inaccuracies  
- Business risk  

**Likelihood:** Medium  
**Impact Level:** High  

---

### 🟡 R6 – Payment Configuration Issues

**Description:**  
Missing or incorrect payment modes or configuration.

**Impact:**  
- Payment processing errors  
- Incomplete financial tracking  

**Likelihood:** Medium  
**Impact Level:** Medium  

---

### 🟡 R7 – Customer Data Issues

**Description:**  
Incorrect or incomplete customer data stored in the system.

**Impact:**  
- Data inconsistency  
- Business process disruption  

**Likelihood:** Low  
**Impact Level:** High  

---

## 🎯 Testing Priorities

Based on the risk analysis:

### 🔴 Highest Priority
- Setup process
- User creation
- Login functionality

### 🟠 Medium Priority
- Input validation
- Invoice logic

### 🟡 Lower Priority
- Data consistency
- Payment configuration

---

## 🔗 Traceability

Risk analysis is directly linked to:

- Test Cases → TC-LOGIN-01, TC-LOGIN-02, TC-LOGIN-03  
- Bug Reports → BUG-LOGIN-002, BUG-SETUP-001  

---

## 🧠 QA Notes

Risk analysis supports:

- Test planning
- Test prioritization
- Defect impact assessment

This approach ensures that testing focuses on areas with the highest business value and system vulnerability.
