# 🧪 iDURAR ERP/CRM – Installation (Docker, VPS)

## 📌 Overview

This document describes the full setup process of the iDURAR ERP/CRM system using Docker on a VPS environment.

The goal of this setup was:
- simulate a real-world QA testing environment
- deploy a fullstack application (frontend + backend + database)
- validate system behavior in a production-like setup

---

## 🖥️ Environment

- VPS Provider: Contabo
- OS: Ubuntu 22.04
- Access: SSH (remote)
- Tools:
  - Docker
  - docker-compose (v1.29.2)
  - VS Code (Remote SSH)

---

## 📦 Project Setup

### 1. Fork repository

```bash
git clone https://github.com/pawelbrudniak/idurar-erp-crm-fork.git
cd idurar-erp-crm-fork
```

### 2. Configure upstream (optional but recommended)

```bash
git remote add upstream https://github.com/idurar/idurar-erp-crm.git
```

---

## 🐳 Docker Setup

### 3. Run application

```bash
docker-compose up --build
```

---

## ⚠️ Issues encountered & solutions

### ❌ Issue 1: Permission denied (Docker socket)

```
permission denied while trying to connect to the Docker daemon
```

✅ Solution:

```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

### ❌ Issue 2: docker-compose `ContainerConfig` error

```
KeyError: 'ContainerConfig'
```

📌 Cause:
- Known issue with docker-compose v1 during container recreation

✅ Solution:

```bash
docker-compose down
docker-compose up --build
```

---

### ❌ Issue 3: Frontend not accessible externally

📌 Symptom:
- Vite running but not reachable via VPS IP

📌 Cause:
- Frontend listening only on `localhost` inside container

✅ Solution:

Edit `docker-compose.yml`:

```yaml
command: sh -c "npm install && npm run dev -- --host 0.0.0.0"
```

---

### ❌ Issue 4: HTTPS-only browser mode

📌 Symptom:
- “Secure site not available”

📌 Cause:
- Application runs on HTTP only

✅ Solution:

```
http://144.91.124.1:3000
```

---

## 🚀 Application Access

### Frontend

```
http://144.91.124.1:3000
```

### Backend

```
http://144.91.124.1:8888
```

---

## 🔐 Default Credentials

```
Email: admin@admin.com
Password: admin123
```

(*If credentials do not work, database seeding must be verified*)

⚠️ Note:
Default credentials are not available due to failed database initialization (setup script error).

---

## 📊 System Architecture

```
Frontend (React + Vite) → Port 3000
Backend (Node.js + Express) → Port 8888
Database (MongoDB) → Port 27017
```

All services are orchestrated using Docker Compose.

---

## 🧪 QA Perspective

This setup validates:

### ✔ Environment readiness
- container orchestration
- service communication
- port exposure

### ✔ System integration
- frontend ↔ backend communication
- backend ↔ database connection

### ✔ Deployment risks
- configuration issues
- networking problems
- dependency mismatches

---

## 🐞 Observed Issues

### Backend setup error

```
Error: Cannot find module '../models/appModels/PaymentMode'
```

📌 Impact:
- occurs during initial setup script
- does not block application startup

📌 Classification:
- **Defect (low severity / medium priority)**

---


## 🎯 Summary

The iDURAR system was successfully deployed using Docker on a VPS environment.

This process included:
- environment configuration
- debugging container issues
- fixing networking problems
- validating full system startup

The system is now ready for:
- functional testing
- API testing
- E2E scenarios
- defect reporting

---
## ⚠️ Blocking Issues Identified

During environment setup, a critical issue was identified:

- setup script failure (missing modules: PaymentMode, Taxes)
- database not fully initialized
- default admin user not usable

👉 This blocks further functional testing and requires workaround or fix.
