# 📊 Azure Monitor

## 📌 Overview

**Azure Monitor** is a monitoring service that helps you collect, analyze, and respond to telemetry from Azure resources and applications.

It helps you understand the **performance, health, and availability** of your cloud environment.

---

## 🎯 Why Use Azure Monitor?

Azure Monitor helps you:

* 📈 Track resource performance
* 🔍 Collect logs and metrics
* 🚨 Create alerts for important events
* 🩺 Monitor resource health
* 📊 Analyze application and infrastructure data

---

## 🏗️ Monitoring Flow

```text
Azure Resources & Applications
            │
            ▼
      📊 Azure Monitor
            │
     ┌──────┴──────┐
     ▼             ▼
  Metrics         Logs
     │             │
     └──────┬──────┘
            ▼
        🚨 Alerts
            │
            ▼
         Action
```

---

## 🔹 Key Components

| Component         | Purpose                                    |
| ----------------- | ------------------------------------------ |
| **Metrics**       | Collect numerical performance data         |
| **Logs**          | Store and analyze detailed event data      |
| **Alerts**        | Notify you when defined conditions are met |
| **Activity Log**  | Tracks subscription-level events           |
| **Log Analytics** | Helps query and analyze collected logs     |

---

## 📋 View Azure Monitor Metrics

You can explore metrics for supported Azure resources through the Azure Portal or Azure CLI.

Example:

```bash
az monitor metrics list \
  --resource <RESOURCE_ID> \
  --metric <METRIC_NAME>
```

---

## 🚨 Create an Alert Rule

Example structure for creating a metric alert:

```bash
az monitor metrics alert create \
  --name high-cpu-alert \
  --resource-group my-resource-group \
  --scopes <RESOURCE_ID> \
  --condition "avg Percentage CPU > 80"
```

---

## 📝 View Activity Logs

```bash
az monitor activity-log list -o table
```

---

## 🧠 What I Learned

* Understanding Azure Monitor
* Difference between metrics and logs
* Monitoring Azure resource performance
* Viewing activity logs
* Understanding alerts and monitoring workflows

---

## 🔐 Security & Best Practices

* Monitor critical Azure resources regularly
* Configure alerts for unusual activity
* Avoid exposing sensitive log data publicly
* Use appropriate access controls for monitoring resources

---

## ✅ Result

Successfully explored the fundamentals of **Azure Monitor** and learned how Azure resources can be monitored using metrics, logs, activity data, and alerts.

> 🚀 **Learn → Practice → Verify → Document**
