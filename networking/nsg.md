# 🛡️ Azure Network Security Group (NSG)

## 📌 Overview

A **Network Security Group (NSG)** is used to control inbound and outbound network traffic in Azure.

NSG rules allow or deny traffic based on ports, protocols, source, and destination.

---

## 🎯 Why Use an NSG?

* 🛡️ Control network traffic
* 🔐 Secure Azure resources
* 🚪 Allow or deny specific ports
* 🌐 Manage inbound and outbound connections

---

## ⚙️ NSG Configuration

| Property           | Value                   |
| ------------------ | ----------------------- |
| **NSG Name**       | `nsg-web`               |
| **VNet**           | `vnet-practice`         |
| **Subnet**         | `subnet-web`            |
| **Resource Group** | `<RESOURCE_GROUP_NAME>` |

---

## 🚀 Create an NSG

```bash
az network nsg create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name nsg-web
```

---

## 🌐 Allow HTTP Traffic

Allow inbound HTTP traffic on port `80`.

```bash
az network nsg rule create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --nsg-name nsg-web \
  --name Allow-HTTP \
  --priority 100 \
  --direction Inbound \
  --access Allow \
  --protocol Tcp \
  --destination-port-ranges 80
```

---

## 🔐 Allow SSH Traffic

Allow inbound SSH traffic on port `22`.

```bash
az network nsg rule create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --nsg-name nsg-web \
  --name Allow-SSH \
  --priority 110 \
  --direction Inbound \
  --access Allow \
  --protocol Tcp \
  --destination-port-ranges 22
```

---

## 🔗 Associate NSG with Subnet

```bash
az network vnet subnet update \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  --name subnet-web \
  --network-security-group nsg-web
```

---

## 🔍 Verify NSG Rules

```bash
az network nsg rule list \
  --resource-group <RESOURCE_GROUP_NAME> \
  --nsg-name nsg-web \
  -o table
```

### 📋 Configured Rules

| Rule Name      | Port | Protocol | Direction | Access |
| -------------- | ---- | -------- | --------- | ------ |
| **Allow-HTTP** | `80` | TCP      | Inbound   | Allow  |
| **Allow-SSH**  | `22` | TCP      | Inbound   | Allow  |

---

## 🏗️ Network Flow

```text
VNet
 │
 └── Subnet
      │
      └── NSG
           ├── Allow HTTP → Port 80
           └── Allow SSH  → Port 22
```

---

## 🧠 What I Learned

* Understanding Network Security Groups
* Creating NSGs using Azure CLI
* Configuring inbound security rules
* Allowing HTTP and SSH traffic
* Associating an NSG with a subnet

---

## ✅ Result

Successfully created an NSG, configured HTTP and SSH inbound rules, and associated it with the subnet.

> 🚀 **Learn → Practice → Verify → Document**
