# 📦 Azure Resource Groups

## 📌 Overview

An **Azure Resource Group** is a logical container used to organize and manage related Azure resources.

For example, a Virtual Machine, Virtual Network, Storage Account, and other resources belonging to the same project can be managed together inside a Resource Group.

---

## 🎯 Why Use Resource Groups?

Resource Groups help you:

* 📂 Organize Azure resources
* 🧩 Manage related resources together
* 🔐 Apply access control using Azure RBAC
* 📊 Monitor and manage resources efficiently
* 🗑️ Delete multiple related resources together when no longer needed

---

## ⚙️ Basic Configuration

| Property                | Example Value       |
| ----------------------- | ------------------- |
| **Resource Group Name** | `my-resource-group` |
| **Location**            | `<AZURE_REGION>`    |

> 🔐 Sensitive or personal Azure environment details are intentionally replaced with generic values.

---

## 🚀 Create a Resource Group

```bash
az group create \
  --name my-resource-group \
  --location <AZURE_REGION>
```

---

## 📋 List Resource Groups

```bash
az group list -o table
```

---

## 🔍 Show Resource Group Details

```bash
az group show \
  --name my-resource-group \
  -o table
```

---

## 📦 List Resources Inside a Resource Group

```bash
az resource list \
  --resource-group my-resource-group \
  -o table
```

---

## 🏗️ Example Structure

```text
📦 Resource Group
│
├── 🌐 Virtual Network
├── 🖥️ Virtual Machine
├── 💾 Storage Account
└── 🛡️ Network Security Group
```

---

## 🧠 What I Learned

* Understanding Azure Resource Groups
* Creating a Resource Group using Azure CLI
* Listing available Resource Groups
* Viewing Resource Group details
* Organizing Azure resources logically

---

## ⚠️ Important Note

Deleting a Resource Group can delete the resources contained within it. Always verify the resources before performing deletion operations.

---

## ✅ Result

Successfully practiced managing Azure Resource Groups using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
