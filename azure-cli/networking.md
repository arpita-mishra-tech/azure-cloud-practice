# Azure Networking

## List Virtual Networks

```bash
az network vnet list -o table
az network vnet subnet list --resource-group <resource-group-name> --vnet-name <vnet-name> -o table
az network nsg list -o table
az network public-ip list -o table

