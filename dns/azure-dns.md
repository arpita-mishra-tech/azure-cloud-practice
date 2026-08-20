# 🌐 Azure DNS

## 📌 Overview

**Azure DNS** is a hosting service for managing DNS zones and records using Azure infrastructure. DNS translates domain names into IP addresses.

---

## 🎯 Key Benefits

* 🌍 Manage DNS zones and records
* 🔗 Map domain names to IP addresses
* ⚙️ Manage DNS using Azure CLI
* 🔐 Control access using Azure permissions

---

## 🏗️ DNS Flow

```text
User
  │
  ▼
🌐 Domain Name
  │
  ▼
📡 DNS Zone
  │
  ▼
📝 DNS Record
  │
  ▼
🖥️ Azure Resource
```

---

## 🔹 Common Record Types

| Record    | Purpose                              |
| --------- | ------------------------------------ |
| **A**     | Maps a domain to an IPv4 address     |
| **AAAA**  | Maps a domain to an IPv6 address     |
| **CNAME** | Maps one domain name to another      |
| **MX**    | Defines mail server information      |
| **NS**    | Specifies authoritative name servers |

---

## 🚀 Create a DNS Zone

```bash
az network dns zone create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name example.com
```

---

## 📝 Create an A Record

```bash
az network dns record-set a add-record \
  --resource-group <RESOURCE_GROUP_NAME> \
  --zone-name example.com \
  --record-set-name www \
  --ipv4-address <IP_ADDRESS>
```

---

## 🔍 List DNS Zones

```bash
az network dns zone list -o table
```

---

## 🧠 What I Learned

* Understanding Azure DNS
* Creating DNS zones
* Managing DNS records
* Mapping domain names to IP addresses

---

## ✅ Result

Successfully documented the basics of **Azure DNS** and DNS management using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
