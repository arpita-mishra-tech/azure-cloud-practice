# 🌍 Azure Public IP Address

## 📌 Overview

An **Azure Public IP Address** allows Azure resources to communicate with the internet.

It can be associated with resources such as:

* 🖥️ Virtual Machines
* ⚖️ Load Balancers
* 🚪 NAT Gateways

---

## 🎯 Why Use a Public IP?

A Public IP helps you:

* 🌐 Access Azure resources from the internet
* 🔗 Enable inbound and outbound connectivity
* 🖥️ Connect to Virtual Machines remotely
* 🚀 Expose applications and services

---

## ⚙️ Public IP Configuration

| Property              | Value                   |
| --------------------- | ----------------------- |
| **Public IP Name**    | `public-ip-practice`    |
| **SKU**               | `Standard`              |
| **Allocation Method** | `Static`                |
| **Resource Group**    | `<RESOURCE_GROUP_NAME>` |
| **Region**            | `<AZURE_REGION>`        |

---

## 🚀 Create a Public IP Address

```bash
az network public-ip create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name public-ip-practice \
  --sku Standard \
  --allocation-method Static
```

---

## 🔍 Verify the Public IP

```bash
az network public-ip list \
  --resource-group <RESOURCE_GROUP_NAME> \
  -o table
```

To view details of a specific Public IP:

```bash
az network public-ip show \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name public-ip-practice \
  -o table
```

---

## 🏗️ Network Flow

```text
Internet
   │
   ▼
🌍 Public IP Address
   │
   ▼
Azure Resource
```

---

## 🧠 What I Learned

* Understanding Azure Public IP addresses
* Creating a Public IP using Azure CLI
* Understanding Static and Dynamic allocation
* Verifying Public IP configuration

---

## 🔐 Security Note

A Public IP exposes a resource to internet connectivity. Always use appropriate security controls such as:

* 🛡️ Network Security Groups
* 🔐 Restricted inbound rules
* 👤 Strong authentication

---

## ✅ Result

Successfully created and verified an Azure Public IP address using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
