# 📁 Azure File Storage

## 📌 Overview

**Azure File Storage** provides fully managed file shares in the cloud that can be accessed using standard file-sharing protocols such as **SMB**.

It is useful when applications or multiple systems need shared file storage.

---

## 🎯 Why Use Azure File Storage?

Azure File Storage helps you:

* 📂 Store and share files in the cloud
* 🔗 Access shared files from multiple systems
* ☁️ Reduce dependency on on-premises file servers
* 📈 Scale storage as required
* 🔐 Manage access securely

---

## 🏗️ Storage Structure

```text
Storage Account
│
└── 📁 File Share
     │
     ├── 📄 document.txt
     ├── 📁 backups/
     └── 📁 application-data/
```

---

## ⚙️ Basic Configuration

| Property            | Example Value       |
| ------------------- | ------------------- |
| **Storage Account** | `mystorageaccount`  |
| **File Share Name** | `myfileshare`       |
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

## 📁 Create a File Share

```bash
az storage share create \
  --name myfileshare \
  --account-name mystorageaccount
```

---

## ⬆️ Upload a File

```bash
az storage file upload \
  --account-name mystorageaccount \
  --share-name myfileshare \
  --source sample.txt \
  --path sample.txt
```

---

## 📋 List Files

```bash
az storage file list \
  --account-name mystorageaccount \
  --share-name myfileshare \
  -o table
```

---

## 🧠 What I Learned

* Understanding Azure File Storage
* Creating an Azure File Share
* Uploading files to a file share
* Listing files using Azure CLI
* Understanding shared cloud storage

---

## 🔐 Security Note

Avoid exposing storage account keys or connection strings in public repositories. Use secure authentication methods wherever possible.

---

## ✅ Result

Successfully documented the basic workflow for creating and managing Azure File Storage using Azure CLI.

> 🚀 **Learn → Practice → Verify → Document**
