# 🔍 Login Flow Investigation – iDURAR QA Case Study

## 🔗 Related Bug Reports

* 🐞 [BUG-LOGIN-001 – CORS issue](../03-bug-reports/BUG-LOGIN-001.md)
* 🐞 [BUG-LOGIN-002 – Missing admin user](../03-bug-reports/BUG-LOGIN-002.md)


## 📌 Overview
This investigation documents the full debugging process of login issues discovered during testing of the iDURAR ERP/CRM system.

The goal was to identify why users were unable to authenticate after deployment.

---

## 🧪 Scope
- User authentication (login)
- Frontend ↔ Backend communication
- Backend configuration
- Database validation

---

## 🚨 Identified Issues

### 🐞 BUG-LOGIN-001 – CORS / Communication Failure
- Login request blocked by browser
- Cause: missing CORS configuration + port mismatch
- Impact: login completely blocked

📄 Details:  
[BUG-LOGIN-001.md](../03-bug-reports/BUG-LOGIN-001.md)

---

### 🐞 BUG-LOGIN-002 – Missing Admin User
- Login returns 404 (user not found)
- Cause: empty `admins` collection in database
- Impact: authentication impossible

📄 Details:  
[BUG-LOGIN-002.md](../03-bug-reports/BUG-LOGIN-002.md)

---

## 🔄 Debugging Process (Step-by-Step)

### 1. Initial symptom
- User cannot log in
- Browser shows CORS error

👉 Conclusion: request blocked before reaching backend

---

### 2. Network analysis
- OPTIONS request fails
- CORS policy violation detected

👉 Action: fix backend CORS configuration

---

### 3. Backend connectivity
- After CORS fix → request reaches backend
- New issue: internal server error

👉 Action: investigate backend + Docker config

---

### 4. Port mismatch identified
- Backend running on port 8888
- Exposed as 5000

👉 Fix: correct Docker port mapping

---

### 5. API response analysis
- Login request returns 404
- Message: user not found

👉 Conclusion: backend works, but no user exists

---

### 6. Database validation
- MongoDB checked via mongosh
- `admins` collection is empty

👉 Root cause confirmed

---

## 🧠 Root Causes Summary

| Area        | Issue                          | Type                |
|------------|-------------------------------|---------------------|
| Backend     | Missing CORS configuration     | Configuration Issue |
| Docker      | Wrong port mapping            | Environment Issue   |
| Database    | No admin user (no seed data)  | Data Issue          |

---

## 📈 Final Outcome
- CORS fixed → communication restored
- Ports fixed → backend reachable
- Root cause identified → missing user

System requires:
- initial data (admin user)
- or registration mechanism

---

## 🧠 QA Insights

This investigation demonstrates:

✔️ Layered debugging approach  
✔️ Network → Backend → Database analysis  
✔️ Root cause identification (not just symptoms)  
✔️ Understanding of environment and infrastructure  

---

## 🏁 Conclusion
Login failure was not caused by a single bug, but by a chain of issues across multiple layers:

1. Communication (CORS)
2. Infrastructure (ports)
3. Data (missing user)

This reflects real-world QA scenarios where multiple factors impact system behavior.

---

## 🏷️ Tags
- QA Case Study
- Debugging
- Integration Testing
- Backend Analysis
- Docker Environment
