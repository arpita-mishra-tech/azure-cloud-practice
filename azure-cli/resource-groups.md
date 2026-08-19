# ☁️ Azure Resource Groups

## 📌 Overview

An **Azure Resource Group** is a logical container used to organize and manage related Azure resources.

Resources such as virtual machines, storage accounts, virtual networks, and other Azure services can be grouped together inside a resource group.

---

## 🎯 Why Use Resource Groups?

Resource Groups help with:

- 📦 Organizing Azure resources
- 🔐 Managing access and permissions
- 💰 Tracking and managing costs
- 🧹 Deleting related resources together
- 🏷️ Applying tags and management policies

---

## ⚡ Create a Resource Group

### Azure CLI

```bash
az group create --name myGroup --location centralindia
