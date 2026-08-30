# 🚀 Azure VM Static Website Hosting

A hands-on Azure project demonstrating how to deploy and host a static website on an Azure Virtual Machine using the Nginx web server.

## 📌 Project Overview

This project demonstrates the deployment of a custom static website on an Ubuntu-based Azure Virtual Machine.

The VM is connected to a public IP and secured using an Azure Network Security Group (NSG). Nginx is installed and configured to serve the website over HTTP.

## 🏗️ Architecture

```text
User / Internet
       |
       v
   Public IP
       |
       v
Network Security Group
       |
   HTTP : 80
       |
       v
Azure Virtual Machine
   Ubuntu 24.04
       |
       v
      Nginx
       |
       v
 Static Website
