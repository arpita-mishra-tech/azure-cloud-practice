# ☁️ Azure Storage

## 📌 Overview

**Azure Storage** is Microsoft's cloud storage platform for storing data such as files, blobs, queues, and tables.

Azure Storage provides highly available and scalable storage services that can be managed through the Azure Portal, Azure CLI, and other tools.

---

## 🧩 Azure Storage Services

| Service | Purpose |
|---------|---------|
| 📦 Blob Storage | Store files, images, videos, backups, and unstructured data |
| 📁 Azure Files | Managed file shares |
| 📨 Queue Storage | Store messages for asynchronous processing |
| 📊 Table Storage | Store structured NoSQL data |

---

## ⚡ Azure CLI Practice

### List Storage Accounts

```bash
az storage account list -o table
