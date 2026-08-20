# 👤 Microsoft Entra ID (Azure AD)

## 📌 Overview

**Microsoft Entra ID**, previously known as **Azure Active Directory (Azure AD)**, is Microsoft's cloud-based identity and access management service.

It helps manage:

* 👤 Users
* 👥 Groups
* 🔐 Authentication
* 🛡️ Access to Azure resources and applications

---

## 🎯 Why Use Microsoft Entra ID?

Microsoft Entra ID helps you:

* 🔐 Manage user identities
* 👥 Organize users into groups
* 🔑 Control authentication
* 🛡️ Secure access to Azure resources
* 🌐 Manage access to cloud applications

---

## 🏗️ Basic Identity Structure

```text
Microsoft Entra ID
│
├── 👤 Users
│
├── 👥 Groups
│
├── 🔐 Authentication
│
└── 🛡️ Access Management
```

---

## 👤 View the Current Signed-In User

```bash
az ad signed-in-user show
```

---

## 👥 List Users

```bash
az ad user list -o table
```

---

## 🔍 Show User Details

```bash
az ad user show \
  --id <USER_PRINCIPAL_NAME>
```

---

## 👥 List Groups

```bash
az ad group list -o table
```

---

## 🧠 What I Learned

* Understanding identity and access management in Azure
* The role of Microsoft Entra ID
* Managing users and groups
* Viewing identity information using Azure CLI
* Understanding authentication and access control

---

## 🔐 Security Note

Avoid sharing sensitive identity information such as:

* User IDs
* Tenant IDs
* Email addresses
* Access tokens
* Passwords

Use generic placeholders when documenting Azure environments in public repositories.

---

## ✅ Result

Successfully explored the basics of **Microsoft Entra ID** and identity management using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
