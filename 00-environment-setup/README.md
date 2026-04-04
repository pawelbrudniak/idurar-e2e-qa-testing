# 🧪 Environment Setup – VPS (Contabo) & Remote Access

## 🎯 Objective

The goal of this stage was to prepare a stable and reproducible test environment for executing end-to-end QA activities on the iDURAR ERP/CRM system.

This included:

* provisioning a remote VPS server
* configuring secure access
* integrating the environment with a local development setup (VS Code)

---

## 🖥️ Infrastructure

* **Provider:** Contabo VPS
* **Operating System:** Ubuntu (Linux)
* **Access Type:** SSH (Secure Shell)
* **Local Environment:** Windows + Visual Studio Code

---

## 🔐 SSH Access Configuration

To enable secure and passwordless authentication, SSH key-based access was configured.

### 1. SSH Key Generation (Local Machine)

An SSH key pair was generated locally:

```bash
ssh-keygen -t ed25519
```

Generated files:

* private key: `~/.ssh/id_ed25519`
* public key: `~/.ssh/id_ed25519.pub`

---

### 2. Public Key Deployment (VPS)

The public key was added to the VPS under the target user (`admin`):

```bash
~/.ssh/authorized_keys
```

Permissions were configured to meet SSH security requirements:

```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```

---

### 3. SSH Client Configuration

A local SSH config entry was created for simplified access:

```bash
Host contabo
    HostName <VPS_IP>
    User admin
    IdentityFile C:\Users\******\.ssh\id_ed25519
```

This allowed connection using:

```bash
ssh contabo
```

instead of manually specifying credentials each time.

---

## 🔌 VS Code Integration (Remote Development)

To simulate a real-world development and testing workflow, the environment was integrated with Visual Studio Code using the **Remote - SSH** extension.

### Steps:

1. Installed extension: `Remote - SSH`
2. Connected to VPS via:

   ```
   Remote-SSH: Connect to Host → contabo
   ```
3. Established full remote workspace

---

## 💻 Result

* Remote server accessible without password (SSH key authentication)
* Full terminal access inside VS Code
* File system of VPS available directly in editor
* Environment ready for:

  * application deployment
  * test execution
  * log inspection
  * debugging

---

## 🧠 QA Perspective

From a QA standpoint, this setup ensures:

* **Environment consistency** – reproducible setup across sessions
* **Traceability** – documented configuration steps
* **Test readiness** – immediate ability to deploy and validate application
* **Real-world workflow simulation** – mirrors professional QA environments

---

## ⚠️ Known Risks / Considerations

* Incorrect SSH permissions may block key authentication
* Misconfigured SSH config may cause fallback to password login
* Environment currently lacks monitoring and backup setup

---

## ✅ Next Step

Proceed with application deployment:

👉 [02 – iDURAR Installation (Docker Setup)](./02-idurar-installation.md)

This step covers:
- application deployment on VPS
- Docker-based setup
- preparing the system for testing
