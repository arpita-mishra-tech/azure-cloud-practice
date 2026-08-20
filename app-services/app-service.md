# 🌐 Azure App Service

## 📌 Overview

**Azure App Service** is a fully managed platform for building, deploying, and scaling web applications and APIs.

It allows developers to focus on application development without managing the underlying server infrastructure.

---

## 🎯 Why Use Azure App Service?

Azure App Service helps you:

* 🚀 Deploy web applications quickly
* 🌐 Host websites and APIs
* 📈 Scale applications when needed
* 🔄 Integrate with CI/CD pipelines
* 🔐 Use built-in security and authentication features

---

## 🏗️ Basic Architecture

```text
Developer
   │
   ▼
📦 Application Code
   │
   ▼
⚙️ Azure App Service
   │
   ▼
🌐 Web Application
   │
   ▼
👤 Users
```

---

## ⚙️ Key Components

| Component            | Description                                           |
| -------------------- | ----------------------------------------------------- |
| **App Service Plan** | Defines the compute resources used by the application |
| **Web App**          | Hosts the web application or API                      |
| **Deployment**       | Publishes application code to Azure                   |
| **Scaling**          | Adjusts resources based on application demand         |

---

## 🚀 Create an App Service Plan

```bash
az appservice plan create \
  --name my-app-service-plan \
  --resource-group my-resource-group \
  --sku B1 \
  --is-linux
```

---

## 🌐 Create a Web App

```bash
az webapp create \
  --resource-group my-resource-group \
  --plan my-app-service-plan \
  --name <UNIQUE_APP_NAME> \
  --runtime "NODE:20-lts"
```

> Replace `<UNIQUE_APP_NAME>` with a globally unique application name.

---

## 📋 List Web Apps

```bash
az webapp list -o table
```

---

## 🔍 View Web App Details

```bash
az webapp show \
  --resource-group my-resource-group \
  --name <APP_NAME> \
  -o table
```

---

## 📈 Scaling Concept

```text
Low Traffic
    │
    ▼
🖥️ 1 Instance

High Traffic
    │
    ▼
🖥️ 🖥️ 🖥️ Multiple Instances
```

---

## 🧠 What I Learned

* Understanding Azure App Service
* Understanding App Service Plans
* Creating a Web App using Azure CLI
* Hosting web applications in Azure
* Understanding basic application scaling

---

## 🔐 Security & Best Practices

* Use secure authentication methods
* Store secrets outside application source code
* Configure HTTPS for web applications
* Apply appropriate access controls
* Monitor application performance and logs

---

## ✅ Result

Successfully documented the basic workflow for creating and managing an Azure Web App using Azure App Service.

> 🚀 **Learn → Practice → Verify → Document**
