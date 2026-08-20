# 🔹 Azure Subnet

## 📌 Overview

A **Subnet** is a smaller network created inside an Azure Virtual Network (VNet).

Subnets help organize resources and separate different workloads within a network.

---

## 🎯 Why Use Subnets?

* 🧩 Divide a VNet into smaller networks
* 🔐 Isolate different workloads
* 🛡️ Apply security rules
* 📦 Organize Azure resources efficiently

---

## ⚙️ Subnet Configuration

| Property           | Value                   |
| ------------------ | ----------------------- |
| **VNet Name**      | `vnet-practice`         |
| **Subnet Name**    | `subnet-web`            |
| **Address Prefix** | `10.0.1.0/24`           |
| **Resource Group** | `<RESOURCE_GROUP_NAME>` |

---

## 🚀 Create a Subnet

```bash
az network vnet subnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  --name subnet-web \
  --address-prefix 10.0.1.0/24
```

---

## 🔍 Verify the Subnet

```bash
az network vnet subnet list \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  -o table
```

---

## 🏗️ Network Structure

```text
🌐 VNet: vnet-practice
│
└── 🔹 Subnet: subnet-web
    └── 📍 Address Prefix: 10.0.1.0/24
```

---

## 🧠 What I Learned

* Understanding Azure Subnets
* Creating a subnet using Azure CLI
* Assigning an IP address range
* Verifying subnet configuration

---

## ✅ Result

Successfully created a subnet inside an Azure Virtual Network.

> 🚀 **Learn → Practice → Verify → Document**
