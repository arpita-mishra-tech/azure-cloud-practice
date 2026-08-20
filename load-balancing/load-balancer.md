# ⚖️ Azure Load Balancer

## 📌 Overview

**Azure Load Balancer** distributes incoming network traffic across multiple backend resources, such as Virtual Machines.

This helps improve:

* ⚡ Availability
* 📈 Scalability
* 🔄 Traffic distribution
* 🛡️ Application reliability

---

## 🏗️ Basic Architecture

```text
                🌐 Internet
                     │
                     ▼
              ⚖️ Load Balancer
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
      🖥️ VM 1               🖥️ VM 2
          │                     │
          └──────────┬──────────┘
                     ▼
                🌐 Virtual Network
```

---

## 🎯 Why Use a Load Balancer?

Azure Load Balancer helps:

* Distribute traffic across multiple servers
* Improve application availability
* Reduce the load on individual Virtual Machines
* Support highly available architectures

---

## 🔹 Key Components

| Component               | Purpose                                      |
| ----------------------- | -------------------------------------------- |
| **Frontend IP**         | Receives incoming traffic                    |
| **Backend Pool**        | Contains the resources that receive traffic  |
| **Load Balancing Rule** | Defines how traffic is distributed           |
| **Health Probe**        | Checks whether backend instances are healthy |

---

## 🚀 Create a Load Balancer

```bash
az network lb create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name <LOAD_BALANCER_NAME> \
  --sku Standard
```

---

## 🌐 Create a Frontend IP Configuration

```bash
az network lb frontend-ip create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --lb-name <LOAD_BALANCER_NAME> \
  --name <FRONTEND_NAME>
```

---

## 🖥️ Create a Backend Pool

```bash
az network lb address-pool create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --lb-name <LOAD_BALANCER_NAME> \
  --name <BACKEND_POOL_NAME>
```

---

## ❤️ Create a Health Probe

```bash
az network lb probe create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --lb-name <LOAD_BALANCER_NAME> \
  --name <PROBE_NAME> \
  --protocol Tcp \
  --port 80
```

---

## 🧠 What I Learned

* Understanding the purpose of load balancing
* Learning about frontend and backend configurations
* Understanding backend pools
* Understanding health probes
* Exploring Azure Load Balancer using Azure CLI

---

## 🔐 Best Practices

* Use health probes to monitor backend availability
* Use multiple backend instances for high availability
* Restrict unnecessary network access
* Monitor traffic and backend health regularly

---

## ✅ Result

Successfully documented the basic concepts and Azure CLI workflow for **Azure Load Balancer**.

> 🚀 **Learn → Practice → Verify → Document**
