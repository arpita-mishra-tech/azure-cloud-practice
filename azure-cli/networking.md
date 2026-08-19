# 🌐 Azure Networking

## 📌 Overview

**Azure Networking** provides the network infrastructure that allows Azure resources to communicate with each other, the internet, and on-premises environments.

Key networking components include:

- 🌐 Virtual Networks (VNet)
- 🔹 Subnets
- 🛡️ Network Security Groups (NSG)
- 🌍 Public IP Addresses

---

## 🎯 Why Azure Networking?

Azure networking helps with:

- 🔗 Connecting cloud resources
- 🔐 Controlling network traffic
- 🌍 Providing internet connectivity
- 🧩 Separating workloads using subnets
- 🛡️ Securing virtual machines and applications

---

## 🌐 Virtual Networks

An **Azure Virtual Network (VNet)** is a private network in Azure that allows resources to communicate securely.

### List Virtual Networks

```bash
az network vnet list -o table

```

---

## 🧪 Hands-on Networking Project

I created and configured an Azure networking environment using Azure CLI.

### Resources Created

| Resource | Name | Configuration |
|----------|------|---------------|
| Virtual Network | `vnet-practice` | `10.0.0.0/16` |
| Subnet | `subnet-web` | `10.0.1.0/24` |
| Network Security Group | `nsg-web` | Attached to `subnet-web` |

### NSG Rules

| Rule | Protocol | Port | Direction | Access |
|------|----------|------|-----------|--------|
| `Allow-HTTP` | TCP | 80 | Inbound | Allow |
| `Allow-SSH` | TCP | 22 | Inbound | Allow |

### Architecture

```text
Azure Resource Group
│
└── VNet: vnet-practice
    │
    ├── Subnet: subnet-web
    │   │
    │   └── NSG: nsg-web
    │       ├── Allow-HTTP → TCP 80
    │       └── Allow-SSH  → TCP 22
    │
    └── AzureBastionSubnet
