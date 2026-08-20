🔹 Azure Subnet
📌 Overview

A Subnet is a smaller network created inside an Azure Virtual Network (VNet).

Subnets help organize and separate Azure resources within a Virtual Network.

🎯 Why Use a Subnet?

Azure Subnets help with:

🧩 Dividing a Virtual Network into smaller networks
🔐 Isolating different workloads
🛡️ Applying security rules to specific resources
🔗 Organizing Azure resources efficiently
🧪 Hands-on Practice

Created a subnet inside the Azure Virtual Network using Azure CLI.

⚙️ Subnet Configuration
Property	Value
🌐 VNet Name	vnet-practice
🔹 Subnet Name	subnet-web
📍 Address Prefix	10.0.1.0/24
📦 Resource Group	<RESOURCE_GROUP_NAME>

🚀 Create a Subnet
az network vnet subnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  --name subnet-web \
  --address-prefix 10.0.1.0/24
```
🔍 Verify the Subnet

List all subnets inside the VNet:

az network vnet subnet list \
  --resource-group <RESOURCE_GROUP_NAME> \
  --vnet-name vnet-practice \
  -o table
```
🏗️ Network Structure
🌐 Virtual Network: vnet-practice
│
└── 🔹 Subnet: subnet-web
    │
    └── 📍 Address Prefix: 10.0.1.0/24

🧠 What I Learned
Understanding the purpose of Azure Subnets
Creating a subnet inside a Virtual Network
Assigning an IP address range
Organizing network resources
Verifying subnet configuration using Azure CLI

✅ Result

The subnet was successfully created inside the Azure Virtual Network.

Next Step
VNet
  ↓
Subnet ✅
  ↓
Network Security Group (NSG)

🚀 Learn → Practice → Verify → Document
