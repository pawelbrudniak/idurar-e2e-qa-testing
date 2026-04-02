# 🤝 Contributing Guidelines – QA Process

This document describes how testing activities are conducted in this project.
The goal is to simulate a real-world QA workflow used in Agile environments.

---

## 🎯 Scope of Contributions

Contributions in this project include:

* Creating and maintaining test cases
* Reporting and tracking defects
* Performing API and data validation testing
* Executing regression and end-to-end tests
* Improving test coverage and documentation

---

## 🧪 QA Workflow Overview

All work is managed through the GitHub Project board (simulating Jira).

Workflow:

Backlog → In Progress → Testing → Done

Each task is represented as an Issue and linked to project artifacts.

---

## 🧩 Types of Work Items

Each contribution should be categorized as one of the following:

### 🎯 Test Case

* Describes a test scenario
* Includes steps, expected results, and test data
* Stored in `/02-test-cases/`

---

### 🐞 Bug Report

* Describes a defect found during testing
* Must include clear reproduction steps
* Stored in `/03-bug-reports/`

---

### 🔧 Task

* General QA activity (e.g., environment setup, data preparation)
* Can support testing but is not a test case or bug

---

## 📝 Creating Test Cases

Test cases should:

* Be based on requirements or user flows
* Have a clear structure:

  * Title
  * Preconditions
  * Steps
  * Expected Result
* Use naming convention:

```
TC-<AREA>-<NUMBER>.md
```

Example:

```
TC-LOGIN-01.md
```

---

## 🐞 Reporting Bugs

Each bug report should include:

* Title (clear and specific)
* Steps to reproduce
* Expected result
* Actual result
* Environment (if relevant)
* Severity & Priority

Bug reports should be linked to the related test case or user flow.

---

## 🔄 Defect Lifecycle

Typical flow:

1. Bug is reported
2. Bug is analyzed
3. Fix is implemented
4. Retest is performed
5. Regression testing is executed (if needed)
6. Bug is closed

---

## 🔗 Traceability

Each element should be connected:

* Test Case ↔ Bug Report
* Test Case ↔ Feature / User Flow
* Bug ↔ Fix (Issue / Commit)

This ensures full traceability across the testing process.

---

## 🧪 Testing Areas Covered

* Functional testing
* API testing (Postman)
* Data validation (DB vs API)
* End-to-End user flows
* Basic security checks

---

## 📌 Notes

This project is designed to demonstrate:

* Understanding of QA processes
* Ability to work with structured test documentation
* Practical approach to defect reporting and validation
* End-to-end thinking across system layers (UI → API → DB)

---

## 🚀 Goal

The main goal is not only to test the application,
but to simulate **real QA responsibilities in a production-like environment**.
