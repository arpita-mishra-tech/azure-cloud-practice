# 🌐 Azure Virtual Network (VNet)

## 📌 Overview

An **Azure Virtual Network (VNet)** is the foundation of networking in Microsoft Azure.

It provides an isolated network environment where Azure resources such as **Virtual Machines, Subnets, and other services** can communicate securely.

---

## 🎯 Why Use a Virtual Network?

A Virtual Network helps you:

* 🌐 Create an isolated network in Azure
* 🔗 Connect Azure resources securely
* 🧩 Organize resources using subnets
* 🔐 Control network traffic
* 🚀 Build a secure cloud infrastructure

---

## 🧪 Hands-on Practice

As part of my Azure Networking practice, I created and verified a Virtual Network using the **Azure CLI**.

### ⚙️ VNet Configuration

| Property           | Value                   |
| ------------------ | ----------------------- |
| **VNet Name**      | `vnet-practice`         |
| **Address Space**  | `10.0.0.0/16`           |
| **Resource Group** | `<RESOURCE_GROUP_NAME>` |
| **Location**       | `<AZURE_REGION>`        |

---

## 🚀 Create a Virtual Network

```bash
az network vnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name vnet-practice \
  --address-prefix 10.0.0.0/16
```

---

## 🔍 Verify the VNet

```bash
az network vnet list -o table
```

To view a specific VNet:

```bash
az network vnet show \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name vnet-practice \
  -o table
```

---

## 🏗️ Network Structure

```text
🌐 Virtual Network
│
├── Name: vnet-practice
├── Address Space: 10.0.0.0/16
└── Region: <AZURE_REGION>
```

---

## 🧠 What I Learned

* What an Azure Virtual Network is
* Why VNets are important in cloud networking
* How to create a VNet using Azure CLI
* How IP address spaces are assigned
* How to verify networking resources

---

## 🔐 Security & Privacy

Sensitive Azure-specific information such as subscription IDs, resource IDs, and personal resource group names are intentionally excluded.

---

## ✅ Result

Successfully created and verified an Azure Virtual Network using Azure CLI.

---

> 🚀 **Learn → Practice → Verify → Document**
