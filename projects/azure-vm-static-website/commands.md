# Azure VM Static Website - Commands

## 1. Azure VM

```bash
az vm list -d -o table
az vm show --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD -o table
az vm list-ip-addresses --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD -o table
az vm show --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD --query osProfile.adminUsername -o tsv
az vm show --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD --query networkProfile.networkInterfaces[0].id -o tsv
```

## 2. SSH Configuration

```bash
az vm show --name vm-static-website --resource-group KML_RG_MAIN-577F8C6B04C24BCD --query osProfile.linuxConfiguration.ssh.publicKeys -o json
ls -la ~/.ssh
ssh-keygen -t rsa -b 4096 -f ~/.ssh/azure_vm_key -N ""
az vm user update --resource-group KML_RG_MAIN-577F8C6B04C24BCD --name vm-static-website --username azureuser --ssh-key-value "$(cat ~/.ssh/azure_vm_key.pub)"
ssh -i ~/.ssh/azure_vm_key azureuser@135.237.97.119
```

## 3. Nginx Installation

```bash
sudo apt update
sudo apt install nginx -y
nginx -v
```

## 4. Start and Verify Nginx

```bash
sudo systemctl enable --now nginx
sudo systemctl status nginx --no-pager
```

## 5. Website Deployment

Website file location:

```text
/var/www/html/index.html
```

After updating the website:

```bash
sudo nginx -t
sudo systemctl reload nginx
```

## 6. Test Website Locally

```bash
curl localhost
```

## 7. Network Security Group

```bash
az network nsg list --resource-group KML_RG_MAIN-577F8C6B04C24BCD -o table
az network nsg rule list --resource-group KML_RG_MAIN-577F8C6B04C24BCD --nsg-name vm-static-website-nsg -o table
```

### Configured NSG Rules

| Rule | Port | Protocol | Access | Direction |
|------|------|----------|--------|-----------|
| SSH | 22 | TCP | Allow | Inbound |
| HTTP | 80 | TCP | Allow | Inbound |

## 8. Public Website

Website URL:

```text
http://135.237.97.119
```

## 9. Architecture

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
       |
       v
      Nginx
       |
       v
 Static Website
```

## 10. Verification

The deployment was verified using:

```bash
sudo systemctl status nginx --no-pager
curl localhost
```

The website was also successfully accessed through the Azure VM public IP.
