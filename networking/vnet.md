🌐 Azure Virtual Network (VNet)

Hands-on practice with Microsoft Azure Networking and Azure CLI.

📌 Overview

An Azure Virtual Network (VNet) is the foundation of networking in Microsoft Azure. It provides an isolated network environment where Azure resources such as Virtual Machines can communicate securely.

🎯 Hands-on Practice

As part of my Azure Networking practice, I created and verified a Virtual Network using Azure CLI.

🔹 VNet Configuration
Property	Value
Resource Group	<RESOURCE_GROUP_NAME>
VNet Name	vnet-practice
Location	<AZURE_REGION>
Address Space	10.0.0.0/16

🚀 Create a Virtual Network
az network vnet create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name vnet-practice \
  --address-prefix 10.0.0.0/16
```
💡 Replace <RESOURCE_GROUP_NAME> and <AZURE_REGION> with your own Azure environment values.

🔍 Verify the VNet
az network vnet list -o table

You can also inspect a specific VNet:

az network vnet show \
  --resource-group <RESOURCE_GROUP_NAME> \
  --name vnet-practice \
  -o table
```

🏗️ Network Structure
Azure Resource Group
│
└── 🌐 Virtual Network
    │
    ├── Name: vnet-practice
    ├── Address Space: 10.0.0.0/16
    └── Region: <AZURE_REGION>

🧠 What I Learned
What an Azure Virtual Network is
Why VNets are important in Azure networking
How to create a VNet using Azure CLI
How IP address spaces are assigned
How to verify Azure networking resources
How to document cloud infrastructure securely
🔐 Security & Privacy

Sensitive Azure-specific information such as subscription IDs, personal resource-group names, and resource IDs is intentionally excluded from this documentation.

🌱 Learn the concept. Practice the command. Build the skill.
