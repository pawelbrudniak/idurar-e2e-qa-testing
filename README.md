# 🧪 iDURAR E2E QA Testing Project

## 🚀 Overview

This repository presents a **real-world, end-to-end QA testing process** performed on the iDURAR ERP/CRM system.

The project simulates actual QA responsibilities in a production-like environment, including:

* test analysis and planning
* test design and execution
* defect reporting
* debugging and root cause analysis
* system-level investigation

---

## 🔍 Login Flow Investigation (Case Study)

During testing, critical issues were discovered in the login functionality.

👉 Full analysis:
📄 [Login Investigation Report](./docs/LOGIN-INVESTIGATION.md)

### Identified Issues:

* 🐞 [BUG-LOGIN-001 – CORS / communication failure](./03-bug-reports/BUG-LOGIN-001.md)
* 🐞 [BUG-LOGIN-002 – Missing admin user (database issue)](./03-bug-reports/BUG-LOGIN-002.md)

### 🧠 Key Insight

Login failure was caused by **multiple issues across system layers**:

* frontend ↔ backend communication (CORS)
* infrastructure configuration (Docker ports)
* data layer (missing user in database)

👉 This reflects real-world QA scenarios where problems are rarely isolated.

---

## 📊 QA Workflow

The testing process is managed using a GitHub Project board to simulate Agile QA workflow:

👉 [Open QA Board](https://github.com/users/pawelbrudniak/projects/3)
👉 [Workflow Documentation](./docs/board-workflow.md)

### Workflow includes:

* backlog management
* test case tracking
* defect lifecycle
* status transitions (Backlog → In Progress → Testing → Done)

---

## 🧭 Project Navigation

### 🧠 Analysis & Preparation

* 📊 [Requirements Analysis](./00-requirements-analysis/)
* 🔧 [Environment Setup](./00-environment-setup/README.md)
* 📋 [Test Plan](./01-test-plan/README.md)

### 🧪 Test Design & Execution

* 🧪 [Test Cases](./02-test-cases/)
* 🔄 [E2E Flows](./07-e2e-flows/)
* 🔌 [API Tests](./04-api-tests/)
* 🗄️ [Data Validation](./05-data-validation/)

### 🐞 Defects & Quality

* 🐞 [Bug Reports](./03-bug-reports/)
* 🔐 [Security Tests](./06-security-tests/)
* 📊 [Test Report](./08-test-report/)

### 📁 Supporting Materials

* 🖼️ [Assets (Evidence)](./assets/)
* 📚 [Documentation](./docs/)
* 🤝 [Contributing](./CONTRIBUTING.md)

---

## 🧱 Project Structure

```id="proj-structure"
00-requirements-analysis/
01-test-plan/
02-test-cases/
03-bug-reports/
04-api-tests/
05-data-validation/
06-security-tests/
07-e2e-flows/
08-test-report/

docs/
assets/
```

---

## 🔧 Environment Setup

The application is deployed on a **remote VPS (Contabo)** and tested in a Docker-based environment.

Key setup elements:

* VPS provisioning
* SSH key-based authentication
* VS Code Remote SSH
* Docker containers (frontend, backend, database)

👉 [View setup documentation](./00-environment-setup/README.md)

### 🧠 QA Perspective

Environment setup ensures:

* reproducibility of defects
* consistency of testing
* realistic working conditions

---

## 🧪 Testing Scope

### Functional Testing

* authentication (login)
* customer management
* invoice workflows
* form validation
* CRUD operations

### Non-functional Testing

* usability
* error handling
* input validation
* basic security checks

---

## 🐞 Defect Reporting Approach

Each bug report includes:

* clear reproduction steps
* expected vs actual result
* severity & priority
* visual evidence (screenshots)
* root cause analysis (when applicable)

👉 Focus: **actionable, developer-friendly reports**

---

## 🧠 QA Approach

This project follows a structured QA process aligned with ISTQB principles:

* requirements analysis
* risk-based thinking
* test design techniques
* defect lifecycle management
* traceability between artifacts

Additionally, the project emphasizes:

* system understanding (frontend + backend + DB)
* debugging skills
* investigation mindset

---

## 🔗 External References

* Repository: https://github.com/idurar/idurar-erp-crm
* Live Demo: https://cloud.idurarapp.com

---

## 🎓 Certification Context

This project supports preparation for the **ISTQB Foundation Level** certification by applying theory in a practical environment.

---

## 🎯 Project Goal

To demonstrate the ability to:

* analyze system behavior end-to-end
* identify real defects and risks
* debug across multiple layers
* communicate findings clearly and professionally

---

## 📌 Note

This is a **QA-focused project**.

The goal is not to modify the application, but to:

* evaluate its quality
* simulate real QA work
* document findings in a professional way


## 🏆 Key Achievements

* Identified and resolved a **multi-layer login failure** involving:

  * CORS misconfiguration
  * incorrect Docker port mapping
  * frontend proxy misconfiguration

* Performed **end-to-end debugging across system layers**:

  * browser (Network / DevTools)
  * frontend configuration (Vite)
  * backend (Express)
  * database (MongoDB)

* Conducted **root cause analysis**, not just symptom reporting

* Validated system behavior using:

  * API inspection
  * database queries (MongoDB)
  * log analysis (Docker containers)

* Created **structured QA documentation**, including:

  * bug reports with evidence
  * investigation report (case study)
  * traceability between defects and analysis

---

## 💼 CV / Interview Angle

This project demonstrates practical experience in:

### 🧪 QA Skills

* test analysis and planning
* test case design
* defect reporting
* exploratory testing

### 🔍 Technical QA

* debugging frontend ↔ backend communication
* analyzing API requests and responses
* working with Docker environments
* validating data in databases (MongoDB)

### 🧠 Problem Solving

* identifying root causes across multiple layers
* distinguishing between configuration issues and functional defects
* understanding system behavior end-to-end

---


## 🎯 What This Shows

* ability to work independently
* understanding of real QA workflows
* technical awareness beyond UI testing
* structured thinking and communication


