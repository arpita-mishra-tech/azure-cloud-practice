# Azure Virtual Machines

## List Virtual Machines

```bash
az vm list -o table
az vm show --name <vm-name> --resource-group <resource-group-name> -o table
az vm start --name <vm-name> --resource-group <resource-group-name>
az vm stop --name <vm-name> --resource-group <resource-group-name>

