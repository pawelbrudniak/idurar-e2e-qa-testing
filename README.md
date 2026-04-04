# 🧪 iDURAR E2E QA Testing Project

## 📌 Quick Navigation

### 🧠 Analysis & Preparation
- 📊 [Requirements Analysis](./00-requirements-analysis/)
- 🔧 [Environment Setup](./00-environment-setup/README.md)
- 📋 [Test Plan](./01-test-plan/README.md)

### 🧪 Test Design & Execution
- 🧪 [Test Cases](./02-test-cases/)
- 🔄 [E2E Flows](./07-e2e-flows/)
- 🔌 [API Tests](./04-api-tests/)
- 🗄️ [Data Validation](./05-data-validation/)

### 🐞 Defects & Quality
- 🐞 [Bug Reports](./03-bug-reports/)
- 🔐 [Security Tests](./06-security-tests/)
- 📊 [Test Report](./08-test-report/)

### 📁 Supporting Materials
- 🖼️ [Assets (Screenshots & Evidence)](./assets/)
- 📚 [Documentation](./docs/)
- 🤝 [Contributing Guidelines](./CONTRIBUTING.md)


---

## 🚀 Environment Setup

The testing environment is hosted on a remote VPS and configured using secure SSH access integrated with Visual Studio Code.

👉 [View Environment Setup Documentation](./00-environment-setup/README.md)

### 🔧 Scope of Configuration

- VPS provisioning (Contabo)
- SSH key-based authentication (secure, passwordless login)
- Remote development environment (VS Code + Remote SSH)
- Initial preparation for application deployment

### 🎯 Purpose

This setup ensures a stable and reproducible environment for executing QA activities, including:

- application deployment and validation
- test execution
- defect investigation
- log analysis and debugging

### 🧠 QA Perspective

From a QA standpoint, environment setup is a critical part of test preparation, ensuring:

- consistency across testing sessions
- reliability of results
- ability to reproduce defects
- alignment with real-world QA workflows

The testing activities in this project are based on the publicly available iDURAR ERP/CRM system.

- Repository: https://github.com/idurar/idurar-erp-crm
- Live Demo: https://cloud.idurarapp.com

## 📊 QA Workflow Board

The testing workflow for this project is managed using a GitHub Project board, simulating a real QA process.

👉 [**Open QA Board**](https://github.com/users/pawelbrudniak/projects/3)

👉 [**View QA Workflow Documentation** – detailed explanation of process, issue lifecycle and traceability](docs/board-workflow.md)

This setup reflects a real-world QA workflow used in Agile environments.

The board includes:

- test case tracking
- defect lifecycle management
- task progress (Backlog → In Progress → Testing → Done)
---

This repository presents a comprehensive **end-to-end quality assurance process** conducted on the iDURAR ERP/CRM system.

The goal of this project is to simulate real-world QA responsibilities and demonstrate practical testing skills in a production-like environment.

---

## 🎯 Project Scope

The project focuses on testing key functionalities of the iDURAR system, including:

- User authentication (login, validation)
- Customer management
- Invoice and payment workflows
- Core CRM operations

Testing covers both **functional behavior** and **system quality aspects** such as usability, validation, and error handling.

---

## 🧠 QA Approach

This project follows a structured QA process aligned with ISTQB principles:

- Requirements analysis and risk identification
- Test planning
- Test case design
- Defect reporting
- Test execution
- Quality evaluation and reporting

The focus is not only on verifying functionality, but also on identifying:
- usability issues
- system risks
- potential business impact of defects

---

## 🧱 Project Structure

- **/test-plan** → test strategy and scope  
- **/test-cases** → designed test scenarios  
- **/bug-reports** → identified defects  
- **/api-tests** → API requests and test scenarios  
- **/data-validation** → verification of data flow between UI and backend  
- **/security-tests** → basic security checks  
- **/e2e-flows** → user journey testing  
- **/test-report** → final quality assessment  
- **/assets** → screenshots and evidence  

---

## 🔍 Testing Scope

### Functional Testing
- Login and authentication
- Form validation
- CRUD operations (customers, invoices)
- Workflow consistency

### Non-functional Testing
- Usability issues
- Error handling
- Input validation
- Basic security checks

---

## 🐞 Defect Reporting

Each defect is documented with:

- clear reproduction steps
- expected vs actual result
- severity and priority
- screenshots (if applicable)

The goal is to provide **actionable and developer-friendly reports**.

---

## 🔗 External Contributions

If applicable, issues and improvements identified during testing may be reported to the original project:

- GitHub Issues
- Pull Requests (for fixes or improvements)

---

## 🎓 Certification Context

This project is created as part of practical preparation for the **ISTQB Foundation Level** certification.

It applies structured testing techniques and QA principles in a real-world scenario.

---

## 🚀 Project Goal

To demonstrate the ability to:

- think like a QA engineer
- identify real system issues
- document testing work professionally
- understand system behavior and risks

---

## 📌 Note

This is a testing-focused project.  
It does not aim to modify the core application but to evaluate its quality from a QA perspective.
