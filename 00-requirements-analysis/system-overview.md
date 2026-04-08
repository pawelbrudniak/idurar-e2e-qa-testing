# 🧠 System Overview – iDURAR ERP/CRM

---

## 📌 Introduction

iDURAR is an open-source ERP/CRM web application designed to manage business operations such as invoicing, customer management, and financial tracking.

The system is built using a modern MERN stack:
- **Frontend:** React (Ant Design UI)
- **Backend:** Node.js / Express
- **Database:** MongoDB
- **Deployment:** Docker-based environment

---

## 🎯 System Purpose

The primary goal of the system is to support small and medium businesses in managing:

- Customer data
- Invoices and billing
- Payments and financial records

---

## 🧩 Core Functional Modules

### 🔐 Authentication & Authorization
- User login
- Session management
- Role-based access (Admin)

---

### 👥 Customer Management
- Create, edit, delete customers
- Store contact and business information

---

### 🧾 Invoice Management
- Create and manage invoices
- Assign customers to invoices
- Track invoice status

---

### 💳 Payment Management
- Define payment methods
- Track payments
- Associate payments with invoices

---

### ⚙️ System Settings
- Default configurations
- Taxes and payment modes
- General system parameters

---

## 🔄 High-Level Workflow

1. User logs into the system
2. User manages customers
3. User creates invoices
4. User records payments
5. System updates financial data

---

## ⚠️ Observations (Testing Perspective)

During initial setup and testing, the following issues were identified:

- No users exist in the database after deployment
- Setup script fails due to missing modules:
  - PaymentMode
  - Taxes
- Login is not possible without manual intervention

👉 These issues directly impact system usability and must be resolved before functional testing.

---

## 🔗 Traceability

This system overview supports the following test areas:

- Login functionality → TC-LOGIN-01, TC-LOGIN-02, TC-LOGIN-03
- Setup validation → BUG-SETUP-001
- User availability → BUG-LOGIN-002

---

## 🧠 QA Notes

This document provides a high-level understanding of the system to support:

- Test planning
- Risk identification
- Test case design

Understanding system architecture is critical for effective testing strategy.
