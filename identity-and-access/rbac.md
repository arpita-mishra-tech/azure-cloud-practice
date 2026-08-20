# 🛡️ Azure Role-Based Access Control (RBAC)

## 📌 Overview

**Azure Role-Based Access Control (RBAC)** is used to manage who can access Azure resources and what actions they are allowed to perform.

RBAC follows the principle of **least privilege**, meaning users should receive only the permissions required for their tasks.

---

## 🎯 Why Use Azure RBAC?

Azure RBAC helps you:

* 👤 Control access to Azure resources
* 🔐 Assign permissions based on roles
* 🧩 Manage access at different scopes
* 🛡️ Follow the principle of least privilege
* 👥 Control what users, groups, and applications can do

---

## 🏗️ RBAC Structure

```text
Security Principal
       │
       ▼
     Role
       │
       ▼
     Scope
       │
       ▼
Azure Resource
```

### 🔹 Key Components

| Component              | Description                                           |
| ---------------------- | ----------------------------------------------------- |
| **Security Principal** | A user, group, service principal, or managed identity |
| **Role Definition**    | A collection of permissions                           |
| **Role Assignment**    | Connects a role to an identity at a specific scope    |
| **Scope**              | Defines where the permissions apply                   |

---

## 📍 RBAC Scopes

Azure permissions can be assigned at different levels:

```text
Management Group
       │
       ▼
Subscription
       │
       ▼
Resource Group
       │
       ▼
Resource
```

Permissions assigned at a higher scope can be inherited by lower scopes.

---

## 👥 List Role Definitions

```bash
az role definition list -o table
```

---

## 🔍 List Role Assignments

```bash
az role assignment list -o table
```

---

## 🔐 Example: Assign a Role

The following example shows the general format for assigning a role:

```bash
az role assignment create \
  --assignee <USER_OR_PRINCIPAL_ID> \
  --role Reader \
  --scope <RESOURCE_SCOPE>
```

### Example Roles

| Role            | Access Level                                  |
| --------------- | --------------------------------------------- |
| **Owner**       | Full access, including managing access        |
| **Contributor** | Can manage resources but cannot manage access |
| **Reader**      | Can view resources but cannot make changes    |

---

## 🧠 What I Learned

* Understanding Azure RBAC
* Learning about roles and permissions
* Understanding RBAC scopes
* Viewing role definitions and assignments
* Applying the principle of least privilege

---

## 🔐 Security Note

Avoid sharing sensitive information such as:

* User IDs
* Subscription IDs
* Tenant IDs
* Principal IDs
* Access tokens

Use generic placeholders when documenting cloud environments in public repositories.

---

## ✅ Result

Successfully explored the fundamentals of **Azure Role-Based Access Control (RBAC)** and understood how permissions can be managed across Azure resources.

> 🚀 **Learn → Practice → Verify → Document**
