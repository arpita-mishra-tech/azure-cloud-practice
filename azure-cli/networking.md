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
