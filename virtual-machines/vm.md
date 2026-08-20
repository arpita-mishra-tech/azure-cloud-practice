# 🖥️ Azure Virtual Machines

## 📌 Overview

An **Azure Virtual Machine (VM)** is an on-demand, scalable computing resource provided by Microsoft Azure.

Virtual Machines allow you to run applications, host services, and create development or testing environments without managing physical hardware.

---

## 🎯 Why Use Azure Virtual Machines?

Azure VMs help you:

* 🖥️ Run Windows or Linux operating systems
* 🚀 Deploy applications and services
* 📈 Scale computing resources when needed
* 🧪 Create development and testing environments
* ☁️ Use cloud infrastructure without managing physical servers

---

## 🏗️ Basic Architecture

```text
Internet
   │
   ▼
🌍 Public IP
   │
   ▼
🖥️ Virtual Machine
   │
   ▼
🌐 Virtual Network
   │
   └── 🔹 Subnet
```

---

## ⚙️ Basic Configuration

| Property           | Example Value       |
| ------------------ | ------------------- |
| **VM Name**        | `my-vm`             |
| **Resource Group** | `my-resource-group` |
| **Image**          | `Ubuntu2204`        |
| **Size**           | `Standard_B1s`      |
| **Admin Username** | `<ADMIN_USERNAME>`  |

> 🔐 Sensitive environment-specific details are intentionally replaced with generic values.

---

## 🚀 Create a Virtual Machine

```bash
az vm create \
  --resource-group my-resource-group \
  --name my-vm \
  --image Ubuntu2204 \
  --size Standard_B1s \
  --admin-username <ADMIN_USERNAME> \
  --generate-ssh-keys
```

---

## 📋 List Virtual Machines

```bash
az vm list -o table
```

---

## 🔍 View VM Details

```bash
az vm show \
  --resource-group my-resource-group \
  --name my-vm \
  -o table
```

---

## ▶️ Start a Virtual Machine

```bash
az vm start \
  --resource-group my-resource-group \
  --name my-vm
```

---

## ⏹️ Stop a Virtual Machine

```bash
az vm stop \
  --resource-group my-resource-group \
  --name my-vm
```

---

## 🧠 What I Learned

* Understanding Azure Virtual Machines
* Creating a Linux VM using Azure CLI
* Viewing VM details
* Starting and stopping a VM
* Understanding the relationship between VMs and networking resources

---

## 🔐 Security Note

For secure VM access:

* Use **SSH keys** instead of passwords where possible
* Restrict inbound NSG rules
* Avoid exposing management ports publicly unless required
* Consider **Azure Bastion** for secure VM connectivity

---

## ✅ Result

Successfully documented the basic workflow for creating and managing an Azure Virtual Machine using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
