# Azure VM Static Website - Commands

## 1. Azure VM

```bash
az vm list -d -o table
az vm show --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD -o table
az vm list-ip-addresses --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD -o table
