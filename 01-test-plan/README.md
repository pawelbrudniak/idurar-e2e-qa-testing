# 📋 Test Plan – iDURAR ERP/CRM QA Project

## 📌 Overview

This document defines the test strategy, scope, and approach for the iDURAR ERP/CRM QA project.

The goal is to validate core system functionality, identify defects, and assess system readiness for further testing.

---

## 🎯 Objectives

- Verify core business workflows in the ERP/CRM system  
- Identify functional defects affecting user operations  
- Validate data consistency between frontend and backend  
- Assess system behavior under incorrect inputs and edge cases  

---

## 📦 Scope

### In Scope

Testing focuses on critical business functionalities:

- User authentication (login, session handling)  
- Customer management (create, update, delete)  
- Invoice management (creation, validation, calculations)  
- Payment processing and tracking  

### Out of Scope

- Advanced performance testing  
- Full security penetration testing  

---

## 🧩 Test Items

The following system components will be tested:

- Frontend (React application)  
- Backend (Node.js / Express API)  
- Database (MongoDB)  
- Integration between system layers  

---

## 🧪 Test Levels & Types

### Test Levels

- System Testing  
- Integration Testing  

### Test Types

- Functional Testing  
- API Testing  
- Data Validation Testing  
- Exploratory Testing  

---

## 🧪 Test Approach

Testing will be conducted using a risk-based approach.

### Process:

1. Analyze application behavior and identify critical flows  
2. Design test cases based on real user scenarios  
3. Execute manual tests via UI  
4. Validate API behavior using Postman  
5. Verify data directly in MongoDB (mongosh)  
6. Report defects with detailed steps and evidence  

---

## 🖥️ Test Environment

- VPS: Contabo (Ubuntu)  
- Deployment: Docker (frontend + backend + MongoDB)  
- Browser: Firefox  

### Tools:

- VS Code (Remote SSH)  
- Postman  
- MongoDB Shell (mongosh)  

---

## 🚪 Entry Criteria

- Application deployed successfully  
- Services accessible via browser and API  
- Basic communication between frontend, backend, and database confirmed  

---

## ✅ Exit Criteria

- Critical test cases executed  
- Major defects identified and documented  
- Test evidence collected  
- Test report prepared  

---

## ⚠️ Risks

- Broken setup script preventing full data initialization  
- Missing users in database blocking login functionality  
- Integration issues between frontend and backend  
- Limited test data affecting coverage  

---

## 👤 Roles & Responsibilities

**QA Engineer:**  
Responsible for test design, execution, defect reporting, and analysis  

*(Project executed individually to simulate full QA ownership)*

---

## 🔗 Traceability

- Test Cases are linked to user flows (Stories)  
- Bugs are linked to affected Test Cases and system modules  
- All artifacts are tracked in GitHub Project Board  

---

## 📦 Deliverables

- Test Plan  
- Test Cases  
- Bug Reports  
- Evidence (screenshots, logs)  
- Final Test Report  

---

## 🔗 References

- Project repository: https://github.com/idurar/idurar-erp-crm  
- QA portfolio repository (this project)  

---

## 🧠 QA Perspective

This test plan ensures:

- Structured and repeatable testing process  
- Clear scope and priorities  
- Traceability between tests and system behavior  
- Real-world QA workflow simulation  
