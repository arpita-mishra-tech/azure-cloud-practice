# 💾 Azure Blob Storage

## 📌 Overview

**Azure Blob Storage** is a cloud storage service designed for storing large amounts of unstructured data.

It can store:

* 📄 Documents
* 🖼️ Images
* 🎥 Videos
* 📦 Backup files
* 📊 Log files

---

## 🎯 Why Use Blob Storage?

Azure Blob Storage helps you:

* ☁️ Store data securely in the cloud
* 📈 Scale storage as needed
* 🌍 Access data from anywhere
* 💰 Pay only for the storage you use
* 🔐 Control access to stored data

---

## 🏗️ Blob Storage Structure

```text
Storage Account
│
└── 📦 Container
     │
     ├── 📄 file-1.txt
     ├── 🖼️ image.png
     └── 📦 backup.zip
```

---

## ⚙️ Basic Configuration

| Property            | Example Value       |
| ------------------- | ------------------- |
| **Storage Account** | `mystorageaccount`  |
| **Container Name**  | `my-container`      |
| **Resource Group**  | `my-resource-group` |
| **Location**        | `<AZURE_REGION>`    |

> 🔐 Environment-specific details are replaced with generic values.

---

## 🚀 Create a Storage Account

```bash
az storage account create \
  --name mystorageaccount \
  --resource-group my-resource-group \
  --location <AZURE_REGION> \
  --sku Standard_LRS
```

---

## 📦 Create a Blob Container

```bash
az storage container create \
  --name my-container \
  --account-name mystorageaccount
```

---

## ⬆️ Upload a Blob

```bash
az storage blob upload \
  --account-name mystorageaccount \
  --container-name my-container \
  --name sample.txt \
  --file sample.txt
```

---

## 📋 List Blobs

```bash
az storage blob list \
  --account-name mystorageaccount \
  --container-name my-container \
  -o table
```

---

## 🧠 What I Learned

* Understanding Azure Blob Storage
* Creating a Storage Account
* Creating a Blob Container
* Uploading files as blobs
* Listing stored blobs using Azure CLI

---

## 🔐 Security Note

Storage access should be managed using appropriate authentication and authorization methods. Avoid exposing sensitive access keys or credentials in public repositories.

---

## ✅ Result

Successfully documented the basic workflow for creating and managing Azure Blob Storage using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
