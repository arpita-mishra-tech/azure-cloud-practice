# 🔐 Azure Bastion

## 📌 Overview

**Azure Bastion** is a fully managed Azure service that provides secure **RDP and SSH connectivity** to Virtual Machines directly through the Azure portal.

With Azure Bastion, you can connect to a VM without exposing the VM directly to the internet using a Public IP.

---

## 🎯 Why Use Azure Bastion?

Azure Bastion helps you:

* 🔐 Connect securely to Azure Virtual Machines
* 🚫 Avoid assigning Public IP addresses directly to VMs
* 🌐 Access VMs through the Azure portal
* 🛡️ Reduce exposure to internet-based attacks

---

## 🏗️ Architecture

```text
Internet
   │
   ▼
🔐 Azure Bastion
   │
   ▼
🌐 Virtual Network
   │
   ▼
🖥️ Virtual Machine
```

---

## ⚙️ Requirements

Before creating Azure Bastion, the Virtual Network must contain a dedicated subnet named:

```text
AzureBastionSubnet
```

The subnet should have an appropriate address range, for example:

```text
10.0.2.0/26
```

> ⚠️ The subnet name **must be exactly `AzureBastionSubnet`**.

---

## 🚀 Create the Bastion Subnet

```bash
az network vnet subnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  --name AzureBastionSubnet \
  --address-prefix 10.0.2.0/26
```

---

## 🌍 Create a Public IP

Azure Bastion requires a Public IP address.

```bash
az network public-ip create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name bastion-public-ip \
  --sku Standard \
  --allocation-method Static
```

---

## 🔐 Create Azure Bastion

```bash
az network bastion create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name bastion-practice \
  --vnet-name vnet-practice \
  --public-ip-address bastion-public-ip \
  --location <AZURE_REGION>
```

---

## 🔍 Verify Azure Bastion

```bash
az network bastion list \
  --resource-group <RESOURCE_GROUP_NAME> \
  -o table
```

---

## 🧠 What I Learned

* Understanding Azure Bastion
* Secure VM connectivity using SSH and RDP
* Why Bastion reduces the need for VM Public IP addresses
* Creating the required `AzureBastionSubnet`
* Creating Azure Bastion using Azure CLI

---

## 🔐 Security Benefits

Azure Bastion improves security by allowing VM access without directly exposing management ports such as:

* SSH — Port `22`
* RDP — Port `3389`

to the public internet.

---

## ✅ Result

Successfully understood and documented the Azure Bastion architecture and its role in providing secure access to Azure Virtual Machines.

> 🚀 **Learn → Practice → Verify → Document**
