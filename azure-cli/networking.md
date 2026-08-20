# 🌐 Azure CLI – Networking

## 📌 Overview

This file contains commonly used **Azure CLI commands for managing Azure networking resources**.

The commands below cover:

* 🌐 Virtual Networks
* 🔹 Subnets
* 🛡️ Network Security Groups
* 🌍 Public IP Addresses

---

# 🌐 Virtual Networks

## Create a Virtual Network

```bash
az network vnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name <VNET_NAME> \
  --address-prefix 10.0.0.0/16
```

## List Virtual Networks

```bash
az network vnet list -o table
```

## Show VNet Details

```bash
az network vnet show \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name <VNET_NAME> \
  -o table
```

---

# 🔹 Subnets

## Create a Subnet

```bash
az network vnet subnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name <VNET_NAME> \
  --name <SUBNET_NAME> \
  --address-prefix 10.0.1.0/24
```

## List Subnets

```bash
az network vnet subnet list \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name <VNET_NAME> \
  -o table
```

---

# 🛡️ Network Security Groups

## Create an NSG

```bash
az network nsg create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name <NSG_NAME>
```

## Create an Inbound Rule

```bash
az network nsg rule create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --nsg-name <NSG_NAME> \
  --name Allow-HTTP \
  --priority 100 \
  --direction Inbound \
  --access Allow \
  --protocol Tcp \
  --destination-port-ranges 80
```

## List NSG Rules

```bash
az network nsg rule list \
  --resource-group <RESOURCE_GROUP_NAME> \
  --nsg-name <NSG_NAME> \
  -o table
```

---

# 🌍 Public IP Addresses

## Create a Public IP

```bash
az network public-ip create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name <PUBLIC_IP_NAME> \
  --sku Standard \
  --allocation-method Static
```

## List Public IP Addresses

```bash
az network public-ip list -o table
```

---

# 🧠 Quick Reference

| Task             | Azure CLI Command               |
| ---------------- | ------------------------------- |
| Create VNet      | `az network vnet create`        |
| List VNets       | `az network vnet list`          |
| Create Subnet    | `az network vnet subnet create` |
| Create NSG       | `az network nsg create`         |
| Create NSG Rule  | `az network nsg rule create`    |
| Create Public IP | `az network public-ip create`   |

---

> 🚀 **Azure CLI → Practice → Verify → Document**
